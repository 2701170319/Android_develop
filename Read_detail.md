### ch02
```
//对于资源ID总是int，而非String
//引入一段代码
 protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_quiz);

        mQuestionTextView = (TextView) findViewById(R.id.question_text_view);
        //updateQuestion()封装以下两行
        int question = mQuestionBank[mCurrentIndex].getTextResId();
        mQuestionTextView.setText(question);

        mTrueButton = (Button) findViewById(R.id.true_button);
 }
 /**
 findViewById(id...)根据id找到View，传给TextView || Button...对象
 setText(int resId...)
 */
```

