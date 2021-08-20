---
description: È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e specifici della lingua.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilazione di file MOF localizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d23c77fee8a745b6032848c124a24ffb8e7cf626b0ff3c87fecc7e05b14d372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556800"
---
# <a name="compiling-localized-mof-files"></a>Compilazione di file MOF localizzati

È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e specifici della lingua.

Digitare il comando seguente al prompt dei comandi per compilare un file MOF master.

**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

Quando si esegue questo comando, il compilatore MOF crea due file MOF dal file Mastermof.mof originale. Il compilatore MOF produce una versione indipendente dal linguaggio, Lnmof.mof, in cui vengono rimossi tutti gli elementi specifici del linguaggio. Viene creata anche una seconda versione specifica del linguaggio, Lsmof.mof. questo file contiene solo gli elementi contrassegnati con [**Amended**](qualifier-flavors.md) Qualifier Flavor nel file Mastermof.mof.

Nell'esempio di codice seguente viene illustrato il contenuto del file MOF indipendente dalla lingua (Lnmof.mof) generato.

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

Nell'esempio di codice seguente viene illustrato il contenuto del file MOF specifico del linguaggio (Lsmof.mfl) generato.

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

La compilazione di un file [](qualifier-flavors.md) MOF con il qualificatore corretto genera solo file MOF separati indipendenti dalla lingua e specifici della lingua. Il repository CIM non viene aggiornato con le nuove informazioni sulla classe. È necessario usare il compilatore MOF per compilare i due file MOF generati dalla prima compilazione prima che le informazioni sulla classe sono disponibili per WMI.

Quando si compila un file MOF master, solo i qualificatori con la versione modificata vengono spostati nel file MOF specifico della lingua. [](qualifier-flavors.md) I qualificatori che  non hanno la versione modificata non sono localizzati e sono presenti solo nella definizione di classe di base nel file MOF indipendente dalla lingua. Se le descrizioni localizzate non sono disponibili, è possibile usare qualificatori non localizzati per le descrizioni predefinite.

È possibile usare il [comando pragma amendment](pragma-amendment.md) anziché specificare [**Amended**](qualifier-flavors.md) come opzione per il compilatore MOF. Una di queste opzioni equivale a richiedere versioni specifiche della lingua e indipendenti dalla lingua di un file MOF. Se si usa il comando pragma amendment o l'opzione della riga di comando **Amended,** è necessario specificare il nome dei file di output usando le opzioni **-MFL** e **-MOF** al prompt dei comandi.

> [!Note]  
> Il file MOF indipendente dalla lingua generato dal compilatore MOF contiene l'equivalente decimale dell'ID delle impostazioni locali, anche se questo valore è stato immesso in formato esadecimale. Nell'esempio precedente il compilatore ha convertito il valore 0x409 nel numero decimale 1033 per il file di output Lnmof.mof.

 

 

 



