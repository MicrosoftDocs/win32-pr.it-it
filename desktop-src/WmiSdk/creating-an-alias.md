---
description: Un alias in WMI è un riferimento simbolico in una classe o in un'istanza di classe che si trova altrove in un file Managed Object Format (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Creazione di un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a4709cba6ba1fa1790c80ac8d8f52f5fa2105207f0094ec3168f62ba0fcc43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925622"
---
# <a name="creating-a-wmi-alias"></a>Creazione di un alias WMI

Un [*alias*](gloss-a.md) in WMI è un riferimento simbolico in una classe o in un'istanza di classe che si trova altrove in un file Managed Object Format (MOF). Il compilatore MOF usa alias per stabilire riferimenti tra classi e istanze. Il compilatore risolve gli alias nelle classi a cui fanno riferimento, quindi i nomi degli alias non sono disponibili nel codice compilato. Di conseguenza, le applicazioni client non possono fare riferimento a classi che usano alias.

> [!Note]  
> WMI supporta riferimenti in avanti, ma non alias circolari.

 

Un alias ha un ambito solo all'interno del file MOF in cui si dichiara l'alias. Pertanto, in genere si usa un alias come collegamento a un percorso di oggetto lungo.

**Per definire un alias**

1.  Aggiungere la frase "as $*aliasname"* all'istanza o alla dichiarazione di classe.
2.  I nomi alias seguono le stesse regole dei nomi di istanza e di classe, ad eccezione del fatto che i nomi di alias devono iniziare con un simbolo di dollaro ($). I caratteri di sottolineatura possono essere visualizzati in un nome alias dopo il carattere iniziale.

Nell'esempio di codice seguente viene descritto come utilizzare un alias in una definizione di classe.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

Negli esempi di codice seguenti viene descritto come utilizzare un alias come riferimento simbolico a un percorso di oggetto. Questi esempi dichiarano due classi per descrivere un disco: la classe Disk per indicare la lettera di unità e la classe DiskRef per indicare il percorso del disco. Viene definito un alias per l'istanza della classe Disk. Questo alias viene usato come valore per la proprietà PathToDisk nell'istanza di DiskRef.

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 



