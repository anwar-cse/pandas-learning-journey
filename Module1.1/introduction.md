# Pandas কি + Install + Import
 Pandas কি?

    Pandas হলো Python-এর একটি লাইব্রেরি, যা দিয়ে আমরা—

                            Data read করতে পারি (CSV, Excel)
                            Data clean করতে পারি
                            Data analyze করতে পারি

 সহজভাবে:
    Pandas = Data নিয়ে কাজ করার টুল

 Install করা

    যদি install না থাকে, তাহলে:  
                            pip install pandas

 pip কী?

    pip হলো Python-এর একটি package manager।
    Python-এ নতুন library বা package install করার জন্য pip ব্যবহার করা হয়।

 pip এর কাজ কী?

    pip দিয়ে তুমি—

     library install করতে পারো
     library update করতে পারো
     library uninstall করতে পারো

 আরও কিছু pip কমান্ড

    pip install numpy      # numpy install
    pip uninstall pandas   # pandas delete
    pip list               # সব installed package দেখাবে
    pip install --upgrade pandas  # update করবে

 pip কোথা থেকে package আনে?

    pip package download করে PyPI (Python Package Index) থেকে
     এটা একটা online store এর মতো, যেখানে হাজার হাজার Python library আছে।

 pip = Python এর App store


 Import করা
    import pandas as pd

     এখানে pd হচ্ছে shortcut (সবাই এটা ব্যবহার করে)

 Pandas এর ২টা main data structure
    1. Series (1D)

        একটা লিস্টের মতো

            import pandas as pd
            data = [10, 20, 30, 40]
            s = pd.Series(data)
            print(s)

            output:
                    0    10
                    1    20
                    2    30
                    3    40

        What is a Series in pandas?

        Series হলো Pandas এর একটি 1-dimensional (এক লাইনের) data structure।
         এটা একটা list + index এর combination
        
         এখানে কী হচ্ছে?
                    data → একটি list
                    pd.Series(data) → list কে Series বানাচ্ছে
                    left side (0,1,2,3) → index
                    right side (10,20,30,40) → data/value

             Series এর গঠন:
                             Series = Index + Value
            
             নিজের index দিতে পারো:
                    s = pd.Series(data, index=['a', 'b', 'c', 'd'])
                    print(s)
                output:
                        a    10
                        b    20
                        c    30
                        d    40

    2. DataFrame (2D)  

    Excel table এর মতো

            data = {
                "Name": ["Anwar", "Rahim", "Karim"],
                "Age": [22, 25, 23]
            }

            df = pd.DataFrame(data)

            print(df)

         Output:
                        Name  Age
                    0  Anwar   22
                    1  Rahim   25
                    2  Karim   23

 DataFrame কী?

    DataFrame হলো Pandas এর সবচেয়ে গুরুত্বপূর্ণ data structure।

     এটা হলো 2-dimensional (row + column) টেবিল
     অনেকটা Excel sheet এর মতো

             এখানে কী হচ্ছে?
                        "Name" → একটি column
                        "Age" → আরেকটি column
                        প্রতিটি row = একজন person
                         index (0,1,2) → row number
                         column (Name, Age) → data category

             কিছু useful কাজ
                    print(df["Name"])   # শুধু Name column
                    print(df.head())   # প্রথম ৫টা row
                    print(df.shape)    # row, column count

                    Explain:
                         1. df["Name"] কী?
                             এটা দিয়ে **Pandas DataFrame থেকে একটি নির্দিষ্ট column নেওয়া হয়।
                         2. df.head() কী?
                             এটা DataFrame এর প্রথম ৫টা row দেখায়
                             default = ৫টা row
                             চাইলে তুমি নিজে দিতে পারো:
                                            df.head(2)   # প্রথম ২টা row
                         3. df.shape কী?
                            এটা DataFrame এর size (row, column) দেখায়


     Summary
                Pandas = Data handling library
                Series = 1D data
                DataFrame = 2D table (সবচেয়ে বেশি ব্যবহার হয়)