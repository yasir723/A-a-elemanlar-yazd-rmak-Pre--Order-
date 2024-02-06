# Ağaç Elemanları Yazdırmak (Pre-Order)
Genelde Ağaç veri yapısında bulunan elemanları yazdırmak için Pre-Order yöntemini kullanarak yazdırılır.
`Pre-Order gezinme algoritması: ` her bir düğümün değerini önce kendisi, ardından sol alt ağaç ve en sonunda sağ alt ağaç olarak sırayla yazdırır.


Bu C# sınıfı, binary ağaç veri yapısını oluşturmak için kullanılır
## `tree` Sınıfı

```csharp
class tree
{
    public int value;
    public tree right;
    public tree left;
}
```

### Özellikler

- `value`: Düğümün değerini temsil eder.
- `right`: Düğüme bağlı olan sağ alt düğümü belirtir.
- `left`: Düğüme bağlı olan sol alt düğümü belirtir.

## `yazdır` Metodu
```csharp
static void yazdır(tree node)
{
    if (node == null) return;

    Console.WriteLine(node.value);
    yazdır(node.left);
    yazdır(node.right);
}
```

## Parametreler

- `node`: Ağaçtaki mevcut düğüm.

## İşleyiş
