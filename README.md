<h1 <p align="center"><b>Praktikum 4</b></p></h1> 

**Nama: Rini Ariza**

**NIM: 312210337**

**Kelas: TI.22.A3**

---

# Praktikum 10 | PHP OOP

## Langkah langkah praktikum

### 1. Buat file baru dengan nama mobil.php
#### Kode nya seperti dibawah ini :
```

```php
<?php
/**
* Program sederhana pendefinisian class dan pemanggilan class.
**/
class Mobil
{
    private $warna;
    private $merk;
    private $harga;
    public function __construct()
{
        $this->warna = "Biru";
        $this->merk = "BMW";
        $this->harga = "10000000";
}
    public function gantiWarna ($warnaBaru)
{
        $this->warna = $warnaBaru;
}
public function tampilWarna ()
{
        echo "Warna mobilnya : " . $this->warna;
}
}
// membuat objek mobil
$a = new Mobil();
$b = new Mobil();
// memanggil objek
echo "<b>Mobil pertama</b><br>";
$a->tampilWarna();
echo "<br>Mobil pertama ganti warna<br>";
$a->gantiWarna("Merah");

$a->tampilWarna();
// memanggil objek
echo "<br><b>Mobil kedua</b><br>";
$b->gantiWarna("Hijau");
$b->tampilWarna();
?>
```
- Output :
![Screenshot (528)](https://github.com/rniarzz/lab10web/assets/115542704/d1e5e26a-4ecf-443d-a919-9c5b9e6426da)


### 2. Buat file baru dengan nama form.php
#### Kode nya seperti dibawah ini :
```

```php
<?php
/**
* Nama Class: Form
* Deskripsi: CLass untuk membuat form inputan text sederhana
**/
class Form
{
    private $fields = array();
    private $action;
    private $submit = "Submit Form";
    private $jumField = 0;

    public function __construct($action, $submit)
    {
        $this->action = $action;
        $this->submit = $submit;
    }

    public function displayForm()
    {
        echo "<form action='".$this->action."' method='POST'>";
        echo '<table width="100%" border="0">';
        for ($j=0; $j<count($this->fields); $j++) {
            echo "<tr><td
            align='right'>".$this->fields[$j]['label']."</td>";
            echo "<td><input type='text'
            name='".$this->fields[$j]['name']."'></td></tr>";
        }
        echo "<tr><td colspan='2'>";
        echo "<input type='submit' value='".$this->submit."'></td></tr>";
        echo "</table>";
    }

    public function addField($name, $label)
    {
        $this->fields [$this->jumField]['name'] = $name;
        $this->fields [$this->jumField]['label'] = $label;
        $this->jumField ++;
    }
}
?>
```

### 3. Buat file baru dengan nama form_input.php
#### Kode nya seperti dibawah ini
```

```php
<?php
/**
* Program memanfaatkan Program 10.2 untuk membuat form inputan sederhana.
**/
include "form.php";
echo "<html><head><title>Mahasiswa</title></head><body>";
$form = new Form("","Input Form");
$form->addField("txtnim", "Nim");
$form->addField("txtnama", "Nama");
$form->addField("txtalamat", "Alamat");
echo "<h3>Silahkan isi form berikut ini :</h3>";
$form->displayForm();
echo "</body></html>";
?>
```

- Output
![Screenshot (529)](https://github.com/rniarzz/lab10web/assets/115542704/30ba43bd-d063-4b34-a301-09a90ed92d59)

<h1 <p align="center"><b>======== Sekian Terima Kasih ==========</b></p></h1>
