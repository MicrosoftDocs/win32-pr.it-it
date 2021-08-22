---
title: Serializzazione incrementale
description: Quando si usa la serializzazione in stile incrementale, si forniscono tre routine per modificare il buffer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf559e94b4476d5dfabdfbb8f040ce8323bc202f4111e9eae95aa257f8e2b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929049"
---
# <a name="incremental-serialization"></a>Serializzazione incrementale

Quando si usa la serializzazione in stile incrementale, si forniscono tre routine per modificare il buffer. Queste routine sono: Alloc, Read e Write. La routine Alloc alloca un buffer delle dimensioni richieste. La routine Write scrive i dati nel buffer e la routine Read recupera un buffer che contiene dati sottoposti a marshalling. Una singola chiamata di serializzazione può effettuare diverse chiamate a queste routine.

Lo stile incrementale della serializzazione usa le routine seguenti:

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

I prototipi per le funzioni Alloc, Read e Write che è necessario fornire sono indicati di seguito:

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

L'input State un parametro per tutte e tre le funzioni è il puntatore definito dall'applicazione associato all'handle dei servizi di codifica. L'applicazione può usare questo puntatore per accedere alla struttura contenente informazioni specifiche dell'applicazione, ad esempio un handle di file o un puntatore di flusso. Si noti che gli stub non modificano il puntatore State se non per passarlo alle funzioni Alloc, Read e Write. Durante la codifica, viene chiamato Alloc per ottenere un buffer in cui vengono serializzati i dati. Viene quindi chiamato Write per consentire all'applicazione di controllare quando e dove vengono archiviati i dati serializzati. Durante la decodifica, read viene chiamato per restituire il numero richiesto di byte di dati serializzati da dove sono stati archiviati dall'applicazione.

Una funzionalità importante dello stile incrementale è che l'handle mantiene il puntatore di stato per l'utente. Questo puntatore mantiene lo stato e non viene mai toccato dalle funzioni RPC, tranne quando si passa il puntatore alla funzione Alloc, Write o Read. L'handle mantiene anche uno stato interno che consente di codificare e decodificare diverse istanze del tipo nello stesso buffer aggiungendo spaziatura interna in base alle esigenze di allineamento. La [**funzione MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) reimposta un handle sullo stato iniziale per consentire la lettura o la scrittura dall'inizio del buffer.

Le funzioni Alloc e Write, insieme a un puntatore definito dall'applicazione, sono associate a un handle dei servizi di codifica da una chiamata alla funzione [**MesEncodeIncrementalHandleCreate.**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) **MesEncodeIncrementalHandleCreate** alloca la memoria necessaria per l'handle e quindi la inizializza.

L'applicazione può chiamare [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) per creare un handle di decodifica, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) per reinizializzare l'handle o [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle. La funzione Read, insieme a un parametro definito dall'applicazione, è associata a un handle di decodifica da una chiamata alla routine **MesDecodeIncrementalHandleCreate.** La funzione crea l'handle e lo inizializza.

I parametri UserState, Alloc, Write e Read di [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) possono essere **NULL** per indicare nessuna modifica.

 

 




