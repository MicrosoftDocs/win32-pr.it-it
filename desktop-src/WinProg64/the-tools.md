---
title: Strumenti
description: In questo argomento vengono descritti gli strumenti disponibili per la preparazione dell'applicazione a 64 bit. Windows 10 è disponibile sia per i processori x64 che per quelli basati su ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, strumenti
- strumenti per la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396563"
---
# <a name="the-tools"></a>Strumenti

In questo argomento vengono descritti gli strumenti disponibili per la preparazione dell'applicazione a 64 bit. Windows 10 è disponibile sia per i processori x64 che per quelli basati su ARM64.

## <a name="include-files"></a>File di inclusione

Gli elementi API sono praticamente identici tra le finestre a 32 e 64 bit. I file di intestazione di Windows sono stati modificati in modo che possano essere usati sia per il codice a 32 che per il codice a 64 bit. I nuovi tipi e macro a 64 bit sono definiti in un nuovo file di intestazione, Basetsd. h, che si trova nel set di file di intestazione incluso in Windows. h. Basetsd. h include le nuove definizioni dei tipi di dati che facilitano la creazione di codice sorgente indipendente dalla dimensione delle parole.

## <a name="new-data-types"></a>Nuovi tipi di dati

I file di intestazione di Windows contengono nuovi tipi di dati. Questi tipi sono principalmente per la compatibilità dei tipi con i tipi di dati a 32 bit. I nuovi tipi forniscono esattamente la stessa digitazione dei tipi esistenti, garantendo allo stesso tempo il supporto per le finestre a 64 bit. Per ulteriori informazioni, vedere [i nuovi tipi di dati](the-new-data-types.md) o il file di intestazione Basetsd. h.

## <a name="predefined-macros"></a>Macro predefinite

Il compilatore definisce le macro seguenti per identificare la piattaforma.



| Macro   | Significato                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Piattaforma A 64 bit. Sono inclusi sia x64 che ARM64.                                                        |
| \_WIN32 | Piattaforma A 32 bit. Questo valore è definito anche dal compilatore a 64 bit per la compatibilità con le versioni precedenti.<br/> |
| \_WIN16 | Piattaforma A 16 bit                                                                                           |



 

Le macro seguenti sono specifiche dell'architettura.



| Macro      | Significato                |
|------------|------------------------|
| \_M \_ ia64  | Piattaforma Intel Itanium |
| \_\_Ix86 M  | piattaforma x86           |
| \_M \_ x64   | piattaforma x64           |
| \_\_Arm64 M | Piattaforma ARM64         |



 

Non usare queste macro tranne che con codice specifico dell'architettura, invece, \_ se possibile, usare Win64, \_ Win32 e \_ Win16.

## <a name="helper-functions"></a>Funzioni di supporto

Le funzioni inline seguenti, definite in Basetsd. h, consentono di convertire in modo sicuro i valori da un tipo a un altro.

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
> **IntToPtr** Sign-estende il valore **int** , **UIntToPtr** zero-estende il valore **int senza segno** , **LongToPtr** Sign-estende il valore **Long** e **ULongToPtr** zero-estende il valore **Long senza segno** .

 

## <a name="64-bit-compiler"></a>Compilatore a 64 bit

I compilatori a 64 bit possono essere utilizzati per identificare il troncamento del puntatore, i cast di tipo non corretti e altri problemi specifici di 64 bit.

Quando il compilatore viene eseguito per la prima volta, probabilmente genererà molti avvisi di troncamento o di mancata corrispondenza del tipo, come i seguenti:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Usare questi avvisi come guida per rendere il codice più affidabile. È consigliabile eliminare tutti gli avvisi, in particolare gli avvisi di troncamento del puntatore.

## <a name="64-bit-compiler-switches-and-warnings"></a>commutatori e avvisi del compilatore a 64 bit

Si noti che questo compilatore Abilita il modello di dati LLP64.

È disponibile un'opzione di avviso per facilitare il porting a LLP64. L'opzione-Wp64 (-W3 Abilita gli avvisi seguenti:

-   C4305: avviso di troncamento. Ad esempio, "Return": troncamento da "unsigned int64" a "Long".
-   C4311: avviso di troncamento. Ad esempio, "cast di tipo": troncamento puntatore da "int \* \_ ptr64" a "int".
-   C4312: conversione a un avviso di dimensioni maggiori. Ad esempio, "Type cast": conversione da "int" a "int \* \_ ptr64" di dimensioni maggiori.
-   C4318: passaggio di lunghezza zero. Ad esempio, passando la costante zero come lunghezza alla funzione **memset** .
-   Operatore C4319: not. Ad esempio, "~": zero che estende "unsigned long" a "unsigned \_ Int64" of Greater size.
-   C4313: chiamata della famiglia **printf** di funzioni con identificatori e argomenti di tipo conversione in conflitto. Ad esempio, "printf": "% p" nella stringa di formato è in conflitto con l'argomento 2 di tipo " \_ Int64". Un altro esempio è la chiamata printf ("% x", il valore del puntatore \_ ); causa un troncamento dei bit 32 superiori. La chiamata corretta è printf ("% p", valore del puntatore \_ ).
-   C4244: uguale all'avviso C4242 esistente. Ad esempio, "Return": conversione da " \_ Int64" a "unsigned int", possibile perdita di dati.

## <a name="64-bit-linker-and-libraries"></a>Linker e librerie a 64 bit

Per compilare applicazioni, usare il linker e le librerie fornite dal Windows SDK. La maggior parte delle librerie a 32 bit ha una versione a 64 bit corrispondente, ma alcune librerie legacy sono disponibili solo nelle versioni a 32 bit. Il codice che effettua chiamate a queste librerie non verrà collegato quando l'applicazione viene compilata per Windows a 64 bit.

 

 





