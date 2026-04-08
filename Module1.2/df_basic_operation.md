# DataFrame তৈরি + Basic Operations


     1. DataFrame তৈরি (Create)
         Dictionary থেকে (সবচেয়ে common)

            import pandas as pd

            data = {
                "Name": ["Anwar", "Rahim", "Karim", "Sakib"],
                "Age": [22, 25, 23, 24],
                "City": ["Dhaka", "Chittagong", "Khulna", "Rajshahi"]
            }

            df = pd.DataFrame(data)

            print(df)

     2. প্রথম কিছু row দেখা → head()
                        print(df.head())
                         Default: প্রথম ৫টা row দেখাবে

                        print(df.head(2))
                         শুধু ২টা row

     3. শেষের row দেখা → tail()
                        print(df.tail())
                         শেষের ৫টা row

     4. DataFrame এর shape (row, column)
                print(df.shape)
                 Output:
                        (4, 3)

                         4 rows, 3 columns

     5. Column নাম দেখা
                print(df.columns)
                 Output:
                        Index(['Name', 'Age', 'City'], dtype='object')
    
     6. Data type দেখা
            print(df.dtypes)
             কোন column string, কোনটা integer—সব দেখাবে


     7. পুরো summary → info()
                         df.info()

                     এতে পাবো:
                    কত row আছে
                    কোন column এ null আছে কিনা
                    data type

     8. Statistical summary → describe()
                        print(df.describe())

                         শুধু numeric column এর জন্য:
                                                    mean
                                                    min
                                                    max
                                                    std #std (standard deviation) = data কতটা ছড়ানো (spread out) তা মাপে
     Mini Practice

    এইটা নিজে run করো:

    import pandas as pd

    data = {
        "Product": ["Pen", "Book", "Bag", "Pencil"],
        "Price": [10, 50, 500, 5]
    }

    df = pd.DataFrame(data)

    print(df.head())
    print(df.shape)
    print(df.columns)


     Summary
                head() → শুরু দেখায়
                tail() → শেষ দেখায়
                shape → size
                columns → column নাম
                info() → full info
                describe() → statistics