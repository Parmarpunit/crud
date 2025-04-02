# crud
       private void submitBtn_Click(object sender, EventArgs e)
       {

           String query = "INSERT INTO firstTable values('" + nameText.Text + "','" + branchText.Text + "')";
           SqlDataAdapter da = new SqlDataAdapter(query, con);
           DataTable dt = new DataTable();
           da.Fill(dt);
           MessageBox.Show("Registered...😁");

       }

       private void showAllUser_Click(object sender, EventArgs e)
       {

           String query = "SELECT * FROM firstTable";
           SqlDataAdapter sda = new SqlDataAdapter(query, con);
           DataTable dt = new DataTable();
           sda.Fill(dt);
           dataGridView1.DataSource = dt;


       }

       private void updateBtn_Click(object sender, EventArgs e)
       {
           int sem;
           int id;
           string query = "UPDATE firstTable SET name = '" + nameText.Text + "', sem = '" + sem + "', branch = '" + branchText.Text + "' WHERE id =" + id;
           SqlDataAdapter da = new SqlDataAdapter(query, con);
           DataTable dt = new DataTable();
           da.Fill(dt);
           MessageBox.Show("Updated...😁");

       }
       private void deleteBtn_Click(object sender, EventArgs e)
       {

           string query = "DELETE FROM firstTable WHERE id = @id";
           SqlDataAdapter da = new SqlDataAdapter(query, con);
           DataTable dt = new DataTable();
           da.Fill(dt);
           MessageBox.Show("Deleted...😁");

       }
