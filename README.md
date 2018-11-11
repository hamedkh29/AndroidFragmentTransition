# AndroidFragmentTransition
Transition between fragments

implementation 'com.github.hamedkh29:AndroidFragmentTransition:master'


Layout:

    <com.khosravi.fragment.transitionlibrary.SlidingRelativeLayout
        android:id="@+id/fragment_place"
        android:layout_marginLeft="10dp"
        android:layout_marginRight="10dp"
        android:layout_marginBottom="10dp"
        android:layout_marginTop="20dp"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
    </com.khosravi.fragment.transitionlibrary.SlidingRelativeLayout>
    
Code:

                android.support.v4.app.FragmentManager fm = getSupportFragmentManager();
                FragmentTransaction fragmentTransaction = fm.beginTransaction();
                if (fragment!=null) {
                    FragmentTransactionExtended fragmentTransactionExtended = new FragmentTransactionExtended(context, fragmentTransaction, firstFragment, secondFragment, R.id.fragment_place);
                    fragmentTransactionExtended.addTransition(FragmentTransactionExtended.SCALEY);
                    fragmentTransactionExtended.commit();
                }
