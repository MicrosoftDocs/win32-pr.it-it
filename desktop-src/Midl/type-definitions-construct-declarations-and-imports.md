---
title: Definizioni dei tipi, creazione di dichiarazioni e importazioni
description: Le definizioni dei tipi, le dichiarazioni di costrutto e le importazioni possono essere eseguite all'esterno del corpo dell'interfaccia.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfacce MIDL, definizioni di tipi
- interfacce MIDL, costrutti di dichiarazioni
- interfacce MIDL, Imports
- definizioni dei tipi MIDL
- costruire dichiarazioni MIDL
- Importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297911"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definizioni dei tipi, creazione di dichiarazioni e importazioni

Le definizioni dei tipi, le dichiarazioni di costrutto e le importazioni possono essere eseguite all'esterno del corpo dell'interfaccia. Tutte le definizioni del file IDL principale verranno visualizzate nel file di intestazione generato e tutte le procedure di tutte le interfacce del file IDL principale genereranno routine stub. Ciò consente alle applicazioni che supportano più interfacce di unire file IDL in un unico file IDL combinato.

Di conseguenza, richiede meno tempo per la compilazione dei file e consente anche a MIDL di ridurre le ridondanze negli stub generati. Questo può migliorare significativamente le interfacce degli [**oggetti**](object.md) attraverso la possibilità di condividere codice comune per interfacce di base e interfacce derivate. Per le interfacce non **oggetto** , i nomi delle procedure devono essere univoci in tutte le interfacce. Per le interfacce di **oggetti** , i nomi delle procedure devono essere univoci solo all'interno di un'interfaccia. Si noti che non sono consentite più interfacce quando si usa l'opzione [**/OSF**](-osf.md) .

## <a name="declarative-constructs"></a>Costrutti dichiarativi

La sintassi per i costrutti dichiarativi nel file IDL è simile a quella per C. MIDL supporta tutti i costrutti dichiarativi di Microsoft C/C++ tranne i seguenti:

-   Dichiaratori di stile precedenti che consentono di specificare un dichiaratore senza un identificatore di tipo, ad esempio:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Dichiarazioni con inizializzatori (MIDL accetta solo le dichiarazioni conformi alla sintassi di MIDL [**const**](const.md) ).

La parola chiave [**Import**](import.md) specifica i nomi di uno o più file IDL da importare. La direttiva import è simile alla direttiva C [**include**](include.md) , ad eccezione del fatto che solo i tipi di dati vengono incorporati nel file IDL di importazione.

## <a name="constant-declaration"></a>Dichiarazione di costante

La dichiarazione di costante specifica le costanti [**booleane**](boolean.md), Integer, character, wide character, String **e \* void** . Per ulteriori informazioni, vedere [**const**](const.md).

## <a name="general-declaration"></a>Dichiarazione generale

Una dichiarazione generale è simile all'istruzione C [**typedef**](typedef.md) con l'aggiunta di attributi di tipo IDL. Fatta eccezione per la modalità [**/OSF**](-osf.md) , il compilatore MIDL consente anche una dichiarazione implicita sotto forma di definizione di variabile.

## <a name="function-declaration"></a>Dichiarazione di funzione

Il dichiaratore di funzione è un caso speciale della dichiarazione generale. È possibile utilizzare gli attributi IDL per specificare il comportamento del tipo restituito della funzione e di ognuno dei parametri.

## <a name="examples"></a>Esempi

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




