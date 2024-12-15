1. Common Controls
Elemen-elemen antarmuka dasar yang digunakan dalam aplikasi:

TextBox untuk input NIK dan Nama:
csharp
Copy code
txtNIK.Text.Trim();
txtName.Text.Trim();
ComboBox untuk memilih jenis surat:
csharp
Copy code
cmbLetterType.Items.AddRange(new string[] { "Surat Domisili", "SKTM", "Surat Keterangan Usaha" });
ListBox untuk menampilkan daftar pengajuan:
csharp
Copy code
lstApplications.Items.Add(data);
Button untuk menambah, menghapus, mencetak, dan keluar:
csharp
Copy code
btnAdd, btnClear, btnPrint, btnExit
2. Container Controls
Kontainer yang digunakan untuk mengelompokkan elemen:

Form sebagai kontainer utama aplikasi:
csharp
Copy code
public partial class MainForm : Form
3. Button and Menu Events
Event-handler yang terhubung dengan tombol dan menu:

Tombol (Button Events):

btnAdd_Click untuk menambahkan data:
csharp
Copy code
private void btnAdd_Click(object sender, EventArgs e)
btnClear_Click untuk menghapus input:
csharp
Copy code
private void btnClear_Click(object sender, EventArgs e)
btnPrint_Click untuk mencetak data:
csharp
Copy code
private void btnPrint_Click(object sender, EventArgs e)
btnExit_Click untuk keluar dari aplikasi:
csharp
Copy code
private void btnExit_Click(object sender, EventArgs e)
Menu (Menu Events):

menuExit_Click untuk keluar melalui menu File > Exit:
csharp
Copy code
private void menuExit_Click(object sender, EventArgs e)
menuAbout_Click untuk menampilkan informasi aplikasi:
csharp
Copy code
private void menuAbout_Click(object sender, EventArgs e)
4. Message Box
Menampilkan pesan kepada pengguna:

Metode ShowMessage untuk pesan informasi, peringatan, dan kesalahan:

csharp
Copy code
MessageBox.Show(message, AppTitle, MessageBoxButtons.OK, icon);
Dialog konfirmasi untuk cetak surat:

csharp
Copy code
DialogResult result = MessageBox.Show("Do you want to print this application?", AppTitle, MessageBoxButtons.YesNo, MessageBoxIcon.Question);
5. Form
Form utama sebagai antarmuka aplikasi:

csharp
Copy code
public partial class MainForm : Form
6. Custom Dialog
Dialog konfirmasi untuk mencetak surat:

csharp
Copy code
DialogResult result = MessageBox.Show(
    $"Do you want to print this application?\\n\\n{selectedApplication}",
    AppTitle, 
    MessageBoxButtons.YesNo, 
    MessageBoxIcon.Question);
7. Variable
Variabel yang digunakan dalam aplikasi:

Variabel lokal:

Input data pengguna:
csharp
Copy code
string nik = txtNIK.Text.Trim();
string name = txtName.Text.Trim();
string letterType = cmbLetterType.Text;
Data pengajuan:
csharp
Copy code
string data = $"NIK: {nik}, Name: {name}, Letter Type: {letterType}";
Variabel global:

Daftar data aplikasi:
csharp
Copy code
private List<string> applicationData = new List<string>();
8. Konstanta
Konstanta untuk judul aplikasi:

csharp
Copy code
private const string AppTitle = "E-Government Application - Surat Keterangan";
9. Operator Aritmatika
Tidak ada perhitungan aritmatika langsung, namun dapat ditambahkan jika diperlukan, misalnya untuk menghitung usia berdasarkan tanggal lahir.

10. Tipe Enumeration
Enumeration untuk jenis pesan:

csharp
Copy code
private enum MessageType
{
    Info,
    Warning,
    Error
}
Jika ada yang ingin diperjelas atau diperluas lagi, silakan beri tahu! 😊
