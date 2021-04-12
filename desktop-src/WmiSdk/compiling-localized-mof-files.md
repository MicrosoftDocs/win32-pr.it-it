---
description: È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e dal linguaggio.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilazione di file MOF localizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346766"
---
# <a name="compiling-localized-mof-files"></a>Compilazione di file MOF localizzati

È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e dal linguaggio.

Digitare il comando seguente al prompt dei comandi per compilare un file MOF master.

**mofcomp-MOF: Lnmof. mof-MFL: Lsmof. mfl-emendamento: MS \_ 409 Mastermof. mof**

Quando si esegue questo comando, il compilatore MOF crea due file MOF dal file Mastermof. mof originale. Il compilatore MOF produce una versione indipendente dalla lingua, Lnmof. mof, in cui vengono rimossi tutti gli elementi specifici della lingua. Viene creata anche una seconda versione specifica del linguaggio, Lsmof. mof. Questo file contiene solo gli elementi contrassegnati con la versione del qualificatore [**modificata**](qualifier-flavors.md) nel file Mastermof. mof.

Nell'esempio di codice seguente viene illustrato il contenuto del file MOF indipendente dalla lingua (Lnmof. MOF) generato.

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

Nell'esempio di codice seguente viene illustrato il contenuto del file MOF specifico del linguaggio (Lsmof. mfl) generato.

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

La compilazione di un file MOF con il qualificatore [**modificato**](qualifier-flavors.md) genera solo file MOF indipendenti dalla lingua e dalla lingua specifici; il repository CIM non viene aggiornato con le informazioni sulla nuova classe. È necessario utilizzare il compilatore MOF per compilare i due file MOF creati dalla prima compilazione prima che tutte le informazioni sulle classi siano disponibili per WMI.

Quando si compila un file MOF Master, solo i qualificatori con la [**versione modificata**](qualifier-flavors.md) vengono spostati nel file MOF specifico della lingua. I qualificatori che non dispongono della **versione modificata** non sono localizzati e sono presenti solo nella definizione della classe di base nel file MOF indipendente dalla lingua. Se non sono disponibili descrizioni localizzate, è possibile usare i qualificatori non localizzati per le descrizioni predefinite.

È possibile usare il comando [pragma emendation](pragma-amendment.md) anziché specificare [**emendato**](qualifier-flavors.md) come passaggio al compilatore MOF. Una di queste opzioni equivale a richiedere versioni specifiche della lingua e indipendenti dalla lingua di un file MOF. Se si usa il comando di modifica pragma o l'opzione della riga di comando **modificata** , è necessario specificare il nome dei file di output usando le opzioni **-MFL** e **-MOF** al prompt dei comandi.

> [!Note]  
> Il file MOF indipendente dalla lingua generato dal compilatore MOF contiene l'equivalente decimale dell'ID delle impostazioni locali, anche se questo valore è stato immesso in formato esadecimale. Nell'esempio precedente il compilatore ha convertito il valore 0x409 nel numero decimale 1033 per il file di output Lnmof. mof.

 

 

 



