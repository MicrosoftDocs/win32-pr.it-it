---
description: È possibile localizzare le proprietà statiche usando mappe di valori parziali.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizzazione di proprietà statiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c51999c68a05e8d7b8cf3fd8c5218bc171931303d86a50c04f32c5d80efb308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050729"
---
# <a name="localizing-static-properties"></a>Localizzazione di proprietà statiche

È possibile localizzare le proprietà statiche usando mappe di valori parziali.

La procedura seguente descrive come è possibile localizzare le proprietà statiche usando mappe di valori parziali con espressioni regolari.

**Per usare i mapping dei valori per localizzare le proprietà statiche**

1.  Creare un file MOF master (Mastervm.mof).

    L'esempio di codice seguente può essere usato per creare un file MOF master (Mastervm.mof).

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  Creare le versioni indipendenti dalla lingua e specifiche della lingua del file MOF.

    Digitare il comando seguente al prompt dei comandi per creare le versioni indipendenti dalla lingua e specifiche della lingua del file MOF.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    Il compilatore MOF genera i file MOF specifici del linguaggio e indipendenti dal linguaggio, LnVm.mof e LsVm.mfl. I valori dell'inglese americano per [la proprietà Numbers](numbers.md) vengono inseriti nel file con estensione mfl per lo spazio dei nomi dell'inglese americano.

    Nell'esempio di codice seguente viene illustrato il contenuto del file LsVm.mfl.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  Compilare i due file MOF e archiviare le informazioni sulla classe nel repository CIM.

    Digitare il comando seguente al prompt dei comandi per compilare i due file MOF.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Localizzare il file MFL per altre impostazioni locali.

    Nell'esempio di codice seguente viene illustrato il contenuto di un file MFL per lo spazio dei nomi francese.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

Il risultato finale è che sia il nome visualizzato che il valore della proprietà [Numbers](numbers.md) dipendono dalle impostazioni locali dell'utente connesso. Se l'utente specifica impostazioni locali non fornite, i dati del qualificatore predefinito provengono dallo spazio dei nomi inglese (ms \_ 409).

L'implicazione di questa progettazione è che ogni valore stringa viene usato come identificatore di ricerca, che non può essere localizzato. Quando si definisce questo schema, è necessario assicurarsi che il valore specificato dal provider sia indipendente dalle impostazioni locali.

> [!Note]  
> WMI attualmente non fornisce il supporto in fase di esecuzione per il mapping dei valori alle stringhe definite dai qualificatori. L'interpretazione della sintassi suggerita è responsabilità dell'applicazione.

 

 

 



