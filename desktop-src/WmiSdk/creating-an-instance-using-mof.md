---
description: È possibile dichiarare un'istanza di base di una classe nel servizio Windows Management usando Managed Object Format (MOF). È anche possibile eseguire l'override dei valori predefiniti per un'istanza di . Per altre informazioni, vedere Impostazione del valore di una proprietà dell'istanza.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Creazione di un'istanza tramite MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05290fd02de80a905e74eeddeb1a04f316901209a97e0e298d038ac2f8888552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097321"
---
# <a name="creating-an-instance-using-mof"></a>Creazione di un'istanza tramite MOF

È possibile dichiarare un'istanza di base di una classe nel servizio Windows Management usando Managed Object Format (MOF). È anche possibile eseguire l'override dei valori predefiniti per un'istanza di . Per altre informazioni, vedere [Impostazione del valore di una proprietà dell'istanza.](#setting-an-instance-property-value)

Nella procedura seguente viene descritto come dichiarare un'istanza di base di una classe usando il codice MOF.

**Per dichiarare un'istanza di base di una classe usando il codice MOF**

1.  Usare le **parole chiave Istanza di** seguite dal nome della classe, dalle parentesi graffe e da un punto e virgola.

    Nell'esempio di codice seguente viene illustrato come dichiarare un'istanza di una classe .

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Al termine, inserire il codice MOF nel repository WMI usando il compilatore MOF.

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

Un'istanza di una classe include tutte le proprietà della classe. Se la classe è una classe derivata, le istanze includono le proprietà appartenenti a tutte le classi superiori nella gerarchia. Ogni classe da cui viene creata un'istanza ha una o più proprietà chiave. Non è possibile creare un'istanza con più di 256 chiavi.

## <a name="setting-an-instance-property-value"></a>Impostazione del valore di una proprietà di istanza

Poiché WMI tipizzato in modo fortemente le proprietà, non è possibile modificare i tipi di proprietà. È tuttavia possibile impostare i valori delle proprietà nelle istanze di . Quando una classe assegna un valore predefinito a una proprietà, WMI assegna il valore predefinito a ogni istanza. È possibile eseguire l'override di questo valore nella dichiarazione di istanza.

La procedura seguente descrive come impostare un valore di proprietà o sovrascrivere un valore predefinito usando il codice MOF.

**Per impostare un valore della proprietà o sovrascrivere un valore predefinito usando il codice MOF**

1.  Inserire un'istruzione di assegnazione tra le parentesi graffe della dichiarazione di istanza.

    Nell'esempio di codice seguente viene illustrato come impostare il valore di una proprietà .

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI non richiede l'impostazione di alcuna proprietà durante la creazione dell'istanza. L'eccezione è qualsiasi proprietà contrassegnata con il [**qualificatore**](key-qualifier.md) Key. Poiché WMI usa le proprietà chiave per identificare in modo univoco le istanze, è necessario impostare tutte le proprietà chiave non appena vengono individuate. Al contrario, non è necessario impostare una proprietà di sistema in una dichiarazione di istanza. Wmi assegna invece i valori appropriati a una proprietà di sistema quando necessario.

2.  Al termine, inserire il codice MOF nel repository WMI con una chiamata al compilatore MOF.

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

Negli esempi di codice seguenti viene illustrato come un'istanza specifica i dati per le proprietà definite da una classe .

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

Nell'esempio precedente la classe definisce tre proprietà: una stringa di caratteri, un intero con segno a 32 bit e un intero senza segno a 32 bit. L'istanza fornisce valori di dati per ognuna di queste proprietà.

 

 



