---
title: Definizioni di tipi, dichiarazioni di costrutti e importazioni
description: Le definizioni dei tipi, le dichiarazioni di costrutti e le importazioni possono verificarsi all'esterno del corpo dell'interfaccia.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfacce MIDL, definizioni dei tipi
- interfacce MIDL, dichiarazioni di costrutto
- interfacce MIDL , importazioni
- definizioni di tipo MIDL
- dichiarazioni di costrutto MIDL
- importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829221"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definizioni di tipi, dichiarazioni di costrutti e importazioni

Le definizioni dei tipi, le dichiarazioni di costrutti e le importazioni possono verificarsi all'esterno del corpo dell'interfaccia. Tutte le definizioni del file IDL principale verranno visualizzate nel file di intestazione generato e tutte le procedure di tutte le interfacce nel file IDL principale genereranno routine stub. Ciò consente alle applicazioni che supportano più interfacce di unire i file IDL in un singolo file IDL combinato.

Di conseguenza, richiede meno tempo per compilare i file e consente anche a MIDL di ridurre gli esuberi negli stub generati. Ciò può migliorare significativamente [**le interfacce**](object.md) oggetto tramite la possibilità di condividere codice comune per le interfacce di base e le interfacce derivate. Per le interfacce non **a** oggetti, i nomi delle procedure devono essere univoci in tutte le interfacce. Per **le interfacce** a oggetti, i nomi delle procedure devono essere univoci solo all'interno di un'interfaccia. Si noti che non sono consentite più interfacce quando si usa [**l'opzione /osf.**](-osf.md)

## <a name="declarative-constructs"></a>Costrutti dichiarativi

La sintassi per i costrutti dichiarativi nel file IDL è simile a quella per C. MIDL supporta tutti i costrutti dichiarativi Microsoft C/C++, ad eccezione dei seguenti:

-   Dichiaratori di stile meno recenti che consentono di specificare un dichiaratore senza un identificatore di tipo, ad esempio:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Dichiarazioni con inizializzatori (MIDL accetta solo dichiarazioni conformi alla sintassi [**const**](const.md) MIDL).

La parola chiave [**import**](import.md) specifica i nomi di uno o più file IDL da importare. La direttiva import è simile alla direttiva [**include**](include.md) C, ad eccezione del fatto che solo i tipi di dati vengono inclusi nel file IDL di importazione.

## <a name="constant-declaration"></a>Dichiarazione di costanti

La dichiarazione di costante specifica [**costanti booleane,**](boolean.md)integer, carattere, caratteri wide, stringa e **void \** _. Per altre informazioni, vedere [_ *const* *](const.md).

## <a name="general-declaration"></a>Dichiarazione generale

Una dichiarazione generale è simile all'istruzione [**typedef**](typedef.md) C con l'aggiunta di attributi di tipo IDL. Ad eccezione [**della modalità /osf,**](-osf.md) il compilatore MIDL consente anche una dichiarazione implicita sotto forma di definizione di variabile.

## <a name="function-declaration"></a>Dichiarazione di funzione

Il dichiaratore di funzione è un caso speciale della dichiarazione generale. È possibile usare gli attributi IDL per specificare il comportamento del tipo restituito della funzione e di ognuno dei parametri.

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

 

 




