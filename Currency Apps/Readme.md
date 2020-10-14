# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp15.000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "INVALID" jika yang dimasukkan berupa text 

## How Does It Work?
Diawali dari method `MainWindow` pada class MainWindow.xaml.cs, kita  mendeklarasikannya sebagai berikut

```C#
public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```

Logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut cara kerjanya

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
