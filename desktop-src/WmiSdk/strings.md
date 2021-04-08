---
title: Stringhe MOF
description: Una stringa è un tipo di dati che contiene una stringa di caratteri generalmente intesa come testo leggibile.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880438"
---
# <a name="mof-strings"></a>Stringhe MOF

Una stringa è un tipo di dati che contiene una stringa di caratteri generalmente intesa come testo leggibile. MOF descrive due tipi di stringhe, che usano per ospitare uno o più caratteri. MOF dispone inoltre di una serie di regole che descrivono l'utilizzo delle virgolette all'interno di una stringa.

Nella tabella seguente sono elencati i tipi di dati stringa per MOF.



| Tipo di dati  | Tipo di automazione | Descrizione                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **\_I2 VT**      | Singolo carattere Unicode a 16 bit nel formato 2 (UCS-2) del set di caratteri universali<br/> |
| **string** | **\_BSTR VT**    | Stringa di caratteri Unicode<br/>                                                    |



 

Usare le linee guida seguenti per la scrittura di stringhe per MOF:

-   Racchiudere le costanti a carattere singolo con virgolette singole.

    Se non si utilizzano virgolette singole con costanti carattere singolo, è necessario utilizzare la rappresentazione Integer del valore del carattere Unicode. Facoltativamente, è possibile specificare il carattere letteralmente con la \\ sequenza di escape x dello standard American National Standards Institute (ANSI) C, come illustrato:

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Poiché MOF è basato su Unicode, è anche possibile specificare valori a 16 bit.

    Tenere presente che le costanti a carattere singolo nel formato ANSI C sono racchiuse tra virgolette doppie.

-   Racchiudere le stringhe di caratteri con virgolette doppie.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Concatena le stringhe di virgolette successive con uno o più spazi vuoti.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Usare una sequenza di escape che inizia con una barra rovesciata per incorporare le virgolette in una stringa.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

Nell'esempio seguente viene descritto come inizializzare le proprietà di stringa e un parametro di stringa:

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




