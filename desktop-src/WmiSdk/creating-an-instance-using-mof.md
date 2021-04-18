---
description: È possibile dichiarare un'istanza di base di una classe nel servizio di gestione Windows utilizzando Managed Object Format (MOF). È inoltre possibile eseguire l'override dei valori predefiniti per un'istanza di. Per ulteriori informazioni, vedere Impostazione di un valore della proprietà dell'istanza.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Creazione di un'istanza mediante MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310392"
---
# <a name="creating-an-instance-using-mof"></a>Creazione di un'istanza mediante MOF

È possibile dichiarare un'istanza di base di una classe nel servizio di gestione Windows utilizzando Managed Object Format (MOF). È inoltre possibile eseguire l'override dei valori predefiniti per un'istanza di. Per ulteriori informazioni, vedere [impostazione di un valore della proprietà dell'istanza](#setting-an-instance-property-value).

Nella procedura riportata di seguito viene descritto come dichiarare un'istanza di base di una classe utilizzando il codice MOF.

**Per dichiarare un'istanza di base di una classe usando il codice MOF**

1.  Utilizzare l' **istanza di** parole chiave seguite dal nome della classe, dalle parentesi graffe e da un punto e virgola.

    Nell'esempio di codice riportato di seguito viene illustrato come dichiarare un'istanza di una classe.

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Al termine, inserire il codice MOF nel repository WMI utilizzando il compilatore MOF.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Un'istanza di una classe include tutte le proprietà della classe. Se la classe è una classe derivata, le istanze includono le proprietà che appartengono a tutte le classi di livello superiore nella gerarchia. Ogni classe da cui viene creata un'istanza ha una o più proprietà chiave. Non è possibile creare un'istanza con più di 256 di chiavi.

## <a name="setting-an-instance-property-value"></a>Impostazione del valore della proprietà di un'istanza

Poiché WMI esegue fortemente la tipizzazione delle proprietà, non è possibile modificare i tipi di proprietà. È tuttavia possibile impostare i valori delle proprietà nelle istanze di. Quando una classe assegna un valore predefinito a una proprietà, WMI assegna il valore predefinito a ogni istanza. È possibile eseguire l'override di questo valore nella dichiarazione dell'istanza.

Nella procedura riportata di seguito viene descritto come impostare un valore di proprietà o sovrascrivere un valore predefinito utilizzando il codice MOF.

**Per impostare un valore di proprietà o sovrascrivere un valore predefinito utilizzando il codice MOF**

1.  Inserire un'istruzione di assegnazione tra le parentesi graffe della dichiarazione dell'istanza.

    Nell'esempio di codice riportato di seguito viene illustrato come impostare un valore della proprietà.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI non richiede l'impostazione di alcuna proprietà durante la creazione dell'istanza. L'eccezione è rappresentata da qualsiasi proprietà contrassegnata con il qualificatore della [**chiave**](key-qualifier.md) . Poiché WMI utilizza proprietà chiave per identificare in modo univoco le istanze, è necessario impostare tutte le proprietà chiave quando vengono rilevate. Non è invece necessario impostare una proprietà di sistema in una dichiarazione di istanza. Al contrario, WMI assegna i valori appropriati a una proprietà di sistema, se necessario.

2.  Al termine, inserire il codice MOF nel repository WMI con una chiamata al compilatore MOF.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Negli esempi di codice seguenti viene illustrato il modo in cui un'istanza specifica i dati per le proprietà definite da una classe.

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

Nell'esempio precedente la classe definisce tre proprietà: una stringa di caratteri, un Signed Integer a 32 bit e un Unsigned Integer a 32 bit. L'istanza fornisce i valori dei dati per ognuna di queste proprietà.

 

 



