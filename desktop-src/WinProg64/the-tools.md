---
title: Strumenti
description: Questo argomento descrive gli strumenti disponibili per l'uso per rendere l'applicazione pronta a 64 bit. Windows 10 è disponibile per i processori basati su x64 e ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guida alla programmazione Windows a 64 bit Windows programmazione a 64 bit , strumenti
- strumenti a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28084c445d664e130a9bb6dc5c087f8421cdaa5746845308258662739ee9084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569891"
---
# <a name="the-tools"></a>Strumenti

Questo argomento descrive gli strumenti disponibili per l'uso per rendere l'applicazione pronta a 64 bit. Windows 10 è disponibile per i processori basati su x64 e ARM64.

## <a name="include-files"></a>File di inclusione

Gli elementi dell'API sono praticamente identici tra 32 e 64 bit Windows. I Windows di intestazione sono stati modificati in modo che possano essere usati sia per il codice a 32 che per il codice a 64 bit. I nuovi tipi e macro a 64 bit sono definiti in un nuovo file di intestazione, Basetsd.h, che si trova nel set di file di intestazione inclusi da Windows.h. Basetsd.h include le nuove definizioni del tipo di dati per rendere indipendenti le dimensioni delle parole del codice sorgente.

## <a name="new-data-types"></a>Nuovi tipi di dati

I Windows di intestazione contengono nuovi tipi di dati. Questi tipi sono principalmente per la compatibilità dei tipi con i tipi di dati a 32 bit. I nuovi tipi forniscono esattamente la stessa digitazione dei tipi esistenti, fornendo allo stesso tempo il supporto per i tipi a 64 bit Windows. Per altre informazioni, vedere [I nuovi tipi di dati o](the-new-data-types.md) il file di intestazione Basetsd.h.

## <a name="predefined-macros"></a>Macro predefinite

Il compilatore definisce le macro seguenti per identificare la piattaforma.



| Macro   | Significato                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Una piattaforma a 64 bit. Sono inclusi sia x64 che ARM64.                                                        |
| \_WIN32 | Una piattaforma a 32 bit. Questo valore è definito anche dal compilatore a 64 bit per la compatibilità con le versioni precedenti.<br/> |
| \_WIN16 | Una piattaforma a 16 bit                                                                                           |



 

Le macro seguenti sono specifiche dell'architettura.



| Macro      | Significato                |
|------------|------------------------|
| \_M \_ IA64  | Piattaforma Intel Itanium |
| \_M \_ IX86  | Piattaforma x86           |
| \_M \_ X64   | Piattaforma x64           |
| \_M \_ ARM64 | Piattaforma ARM64         |



 

Non usare queste macro tranne con codice specifico dell'architettura, invece, usare \_ WIN64, \_ WIN32 e \_ WIN16 quando possibile.

## <a name="helper-functions"></a>Funzioni di supporto

Le funzioni inline seguenti (definite in Basetsd.h) consentono di convertire in modo sicuro i valori da un tipo a un altro.

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> **IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.

 

## <a name="64-bit-compiler"></a>Compilatore a 64 bit

I compilatori a 64 bit possono essere usati per identificare il troncamento del puntatore, i cast di tipo non corretto e altri problemi specifici a 64 bit.

Quando il compilatore viene eseguito per la prima volta, probabilmente genererà molti avvisi di troncamento del puntatore o di mancata corrispondenza del tipo, ad esempio:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Usare questi avvisi come guida per rendere il codice più affidabile. È consigliabile eliminare tutti gli avvisi, in particolare gli avvisi di troncamento del puntatore.

## <a name="64-bit-compiler-switches-and-warnings"></a>Opzioni e avvisi del compilatore a 64 bit

Si noti che questo compilatore abilita il modello di dati LLP64.

È disponibile un'opzione di avviso per facilitare il porting a LLP64. L'opzione -Wp64 -W3 abilita gli avvisi seguenti:

-   C4305: avviso di troncamento. Ad esempio, "return": troncamento da "unsigned int64" a "long".
-   C4311: avviso di troncamento. Ad esempio, "type cast": troncamento del puntatore da "int \* \_ ptr64" a "int".
-   C4312: avviso di conversione in dimensioni maggiori. Ad esempio, "type cast": conversione da "int" a "int \* \_ ptr64" di dimensioni maggiori.
-   C4318: passaggio di lunghezza zero. Ad esempio, passando la costante zero come lunghezza alla **funzione memset.**
-   C4319: operatore Not. Ad esempio, "~": zero che estende "unsigned long" a "unsigned \_ int64" di dimensioni maggiori.
-   C4313: chiamata della famiglia di funzioni **printf** con argomenti e identificatori di tipo di conversione in conflitto. Ad esempio, "printf": "%p" nella stringa di formato è in conflitto con l'argomento 2 di tipo " \_ int64". Un altro esempio è la chiamata printf("%x", valore del puntatore). Ciò causa un troncamento \_ dei 32 bit superiori. La chiamata corretta è printf("%p", valore del \_ puntatore).
-   C4244: uguale all'avviso C4242 esistente. Ad esempio, "return": conversione da \_ "int64" a "unsigned int", possibile perdita di dati.

## <a name="64-bit-linker-and-libraries"></a>Linker e librerie a 64 bit

Per compilare applicazioni, usare il linker e le librerie fornite dal Windows SDK. La maggior parte delle librerie a 32 bit ha una versione a 64 bit corrispondente, ma alcune librerie legacy sono disponibili solo nelle versioni a 32 bit. Il codice che chiama in queste librerie non verrà collegata quando l'applicazione viene compilata per Windows a 64 bit.

 

 





