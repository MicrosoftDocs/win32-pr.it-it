---
description: Un alias in WMI è un riferimento simbolico in una classe o in un'istanza di classe situata altrove in un file di Managed Object Format (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Creazione di un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310391"
---
# <a name="creating-a-wmi-alias"></a>Creazione di un alias WMI

Un [*alias*](gloss-a.md) in WMI è un riferimento simbolico in una classe o in un'istanza di classe situata altrove in un file di Managed Object Format (MOF). Il compilatore MOF USA alias per stabilire riferimenti tra classi e istanze. Il compilatore risolve gli alias nelle classi a cui fanno riferimento, quindi i nomi di alias non sono disponibili nel codice compilato. Di conseguenza, le applicazioni client non possono fare riferimento alle classi che usano gli alias.

> [!Note]  
> WMI supporta il riferimento in diretta ma non gli alias circolari.

 

Un alias ha un ambito solo nel file MOF in cui si dichiara l'alias. Pertanto, in genere si usa un alias come collegamento a un percorso di oggetto lungo.

**Per definire un alias**

1.  Aggiungere la frase "As $*aliasname*" alla dichiarazione dell'istanza o della classe.
2.  I nomi di alias seguono le stesse regole dei nomi di istanza e di classe, ad eccezione del fatto che i nomi di alias devono iniziare con un segno di dollaro ($). I caratteri di sottolineatura possono essere visualizzati in un nome di alias che segue il carattere iniziale.

Nell'esempio di codice seguente viene descritto come utilizzare un alias in una definizione di classe.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

Gli esempi di codice seguenti descrivono come usare un alias come riferimento simbolico a un percorso dell'oggetto. Questi esempi dichiarano due classi per descrivere un disco: la classe del disco per indicare la lettera di unità e la classe DiskRef per indicare il percorso del disco. Per l'istanza della classe disco è definito un alias. Questo alias viene usato come valore per la proprietà PathToDisk nell'istanza di DiskRef.

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

 

 



