# assignment
作业
public class MainActivity extends AppCompatActivity {

    private ImageView mImgHead;
    private EditText mEtUsername;
    private EditText mEtPassword;
    private Button mBtnLogin;
    private Toolbar toolbar;
    @SuppressLint("MissingInflatedId")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        mImgHead = findViewById(R.id.imageView);
        mEtPassword = findViewById(R.id.editText);
        mEtUsername = findViewById(R.id.editText2);
        mBtnLogin = findViewById(R.id.button);
        mBtnLogin.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                login();
            }
        });
    }





    private void login(){
        String username = mEtUsername.getText().toString();
        String password = mEtPassword.getText().toString();
        if (username.equals("123456") && password.equals("123456")) {
            Toast.makeText(MainActivity.this,"登录成功",Toast.LENGTH_SHORT).show();
            Intent intent = new Intent(this, MainActivity2.class);
            startActivity(intent);

        }else Toast.makeText(MainActivity.this,"登录失败",Toast.LENGTH_SHORT).show();
    }
}
