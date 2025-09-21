namespace WinFormsApp3
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            //Thêm thông tin danh sách sản phẩm 
            listBox1.Items.Add("Doraemon");
            listBox1.Items.Add("Kinh Van Hoa");
            listBox1.Items.Add("Harry Potter");

            //Thêm phương thức thanh toán 
            comboBox1.Items.Add("ATM");
            comboBox1.Items.Add("Tiền mặt");
            comboBox1.Items.Add("Chuyển khoản");


        }

        private void button1_Click(object sender, EventArgs e)
        {
            string khachhang = textBox1.Text;
            string dienthoai = textBox2.Text;
            string thanhtoan = comboBox1.SelectedItem?.ToString();

            //Lấy sản phẩm đã chọn
            string sanPham = "";
            foreach (var item in listBox1.SelectedItems)
            {
                sanPham += " " + item.ToString() + "\n";
            }

            //Hiển thị thông tin đặt hàng

            richTextBox1.Text = "Thông tin đơn hàng\n";
            richTextBox1.Text += "Khách hàng: " + khachhang + "\n";
            richTextBox1.Text += "Điện thoại: " + dienthoai + "\n";
            richTextBox1.Text += "Sản phẩm đặt mua: " + sanPham + "\n";
            richTextBox1.Text += "Cách thanh toán: " + thanhtoan + "\n";
        }
    }
}
