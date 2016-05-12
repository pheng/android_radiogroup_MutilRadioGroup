# android MutilRadioGroup
android MutilRadioGroup：复杂样式的单选框，自定义RadioGroup实现radiobutton多行多列排列布局

![](https://github.com/pheng/MutilRadioGroup/blob/master/MutilRadioGrop.gif)

###根据RadioGroup源码修改而来，实现支持RadioGroup里面的RadioButton嵌套在其他布局里,从而实现复杂布局的单选框功能。
使用的时候只用把MyRadioGroup类拷到自己的工程里就可以引用。

1、使用与RadioGroup一样，MutilRadioGroup里的所有RadioButton（包括MutilRadioGroup里嵌套的子布局里面的所有RadioButton）属于同一组。

2、增加方法setCheckWithoutNotif(int id)，设置默认的RadioButton被选中，但是不响应监听事件。

###Layout示例
	<com.pheng.mutilradiogroup.MyRadioGroup
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical" >

        <LinearLayout
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal" >

            <RadioButton
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_margin="3dp"
                android:layout_weight="1"
                android:background="@drawable/rdobtn_selecter"
                android:button="@null"
                android:gravity="center"
                android:text="10元"
                android:textSize="25sp" />

            <RadioButton
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_margin="3dp"
                android:layout_weight="1"
                android:background="@drawable/rdobtn_selecter"
                android:button="@null"
                android:gravity="center"
                android:text="20元"
                android:textSize="25sp" />

           ...
        </LinearLayout>

        <LinearLayout
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal" >

            <RadioButton
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_margin="3dp"
                android:layout_weight="1"
                android:background="@drawable/rdobtn_selecter"
                android:button="@null"
                android:gravity="center"
                android:text="80元"
                android:textSize="25sp" />

           ...
        </LinearLayout>
    </com.pheng.mutilradiogroup.MyRadioGroup>
