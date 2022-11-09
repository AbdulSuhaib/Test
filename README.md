 public dynamic GetData1()
        {
            //1st process

            List<dynamic> Return = new List<dynamic>();

            string[] array = { "A", "A", "Q", "Q", "6" };
            string[] array1 = { "J", "6", "3", "10", "8" };
            string[] array2 = { "K", "7", "3", "9", "3" };
            string[] array3 = { "K", "9", "10", "J", "Q" };
            string[] array4 = { "3", "5", "5", "5", "5" };

            var duplicates = array4.GroupBy(p => p).Where(g => g.Count() > 1).Select(g => g.Key);

            if (duplicates.Count() > 0)
            {
                string Char = duplicates.FirstOrDefault();
                
                Return.Add(true);
                Return.Add(Char);
                
                return Return;
            }
            else
            {
                return false;
            }

            //2nd Process

            //List<dynamic> HighestPair = new List<dynamic>();

            //HighestPair.Add("A");
            //HighestPair.Add("A");
            //HighestPair.Add("B");
            //HighestPair.Add("C");
            //HighestPair.Add("D");

            //if (HighestPair.Count > 0)
            //{
            //    var High = HighestPair.GroupBy(p => p).Select(g => g.FirstOrDefault()).FirstOrDefault();

            //    if (High.Count() > 0)
            //    {
            //        string Char = High.FirstOrDefault();

            //        Return.Add(true);
            //        Return.Add(Char);

            //        return Return;
            //    }
            //    else
            //    {
            //        return false;
            //    }
            //}

        }
