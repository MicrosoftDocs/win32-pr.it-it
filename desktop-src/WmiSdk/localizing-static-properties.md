---
description: È possibile localizzare le proprietà statiche usando le mappe di valori parziali.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizzazione di proprietà statiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356164"
---
# <a name="localizing-static-properties"></a>Localizzazione di proprietà statiche

È possibile localizzare le proprietà statiche usando le mappe di valori parziali.

Nella procedura riportata di seguito viene descritto il modo in cui le proprietà statiche possono essere localizzate mediante mapping di valori parziali con espressioni regolari

**Per usare le mappe del valore per localizzare le proprietà statiche**

1.  Creare un file MOF Master (Mastervm. MOF).

    L'esempio di codice seguente può essere utilizzato per creare un file MOF Master (Mastervm. MOF).

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

2.  Creare le versioni indipendente dalla lingua e dalla lingua del file MOF.

    Digitare il comando seguente al prompt dei comandi per creare le versioni del file MOF indipendenti dalla lingua e dal linguaggio.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    Il compilatore MOF genera i file MOF specifici del linguaggio e della lingua, LnVm. mof e LsVm. mfl. I valori della lingua inglese (Stati Uniti) per la proprietà [numbers](numbers.md) vengono inseriti nel file con estensione MFL per lo spazio dei nomi American English.

    Nell'esempio di codice seguente viene illustrato il contenuto del file LsVm. mfl.

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

Il risultato finale è che il nome visualizzato e il valore della proprietà [numbers](numbers.md) dipendono dalle impostazioni locali dell'utente connesso. Se l'utente specifica le impostazioni locali che non sono state specificate, i dati di qualificatore predefiniti provengono dallo \_ spazio dei nomi inglese (ms 409).

L'implicazione di questa progettazione è che ogni valore di stringa viene utilizzato come identificatore di ricerca, che non può essere localizzato. Quando si definisce questo schema, è necessario assicurarsi che il valore inserito dal provider sia indipendente dalle impostazioni locali.

> [!Note]  
> In WMI non è attualmente disponibile il supporto in fase di esecuzione per il mapping di valori a stringhe definite da qualificatori. L'interpretazione della sintassi suggerita è responsabilità dell'applicazione.

 

 

 



