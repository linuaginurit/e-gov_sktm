1. Common Controls
   - TextBox untuk input NIK dan Nama
   - ComboBox untuk memilih jenis surat
   - ListBox untuk menampilkan daftar pengajuan
   - Button untuk menambah, menghapus, mencetak, dan keluar
2. Container controls
   - Form sebagai kontainer utama aplikasi
3. Button and Menu Events
   - Tombol (Button Events)
      - btnAdd_Click
      - btnClear_Click
      - btnExit_Click
    - Menu (Menu Events)
       - menuExit_Click
       - menuAbout_Click 
4. Message Box
   - Metode ShowMessage untuk pesan informasi, peringatan, dan kesalahan
   - Dialog konfirmasi untuk cetak surat
5. Form
   ```public partial class MainForm : Form```
6. Custom Dialog
   ```
   DialogResult result = MessageBox.Show(
    $"Do you want to print this application?\\n\\n{selectedApplication}",
    AppTitle, 
    MessageBoxButtons.YesNo, 
    MessageBoxIcon.Question);
   ```
7. Variable
   - Variabel lokal:
      - Input data pengguna
        ```
        string nik = txtNIK.Text.Trim();
        string name = txtName.Text.Trim();
        string letterType = cmbLetterType.Text;
        ```
      - Data pengajuan
        ```string data = $"NIK: {nik}, Name: {name}, Letter Type: {letterType}";```
  - Variabel global:
    - Daftar data aplikasi:
      ```private List<string> applicationData = new List<string>();```
      
    

