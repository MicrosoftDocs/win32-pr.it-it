---
title: Serializzazione incrementale
description: Quando si usa la serializzazione dello stile incrementale, si forniscono tre routine per modificare il buffer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516018"
---
# <a name="incremental-serialization"></a>Serializzazione incrementale

Quando si usa la serializzazione dello stile incrementale, si forniscono tre routine per modificare il buffer. Queste routine sono: Alloc, Read e Write. La routine Alloc alloca un buffer della dimensione richiesta. La routine Write scrive i dati nel buffer e la routine Read recupera un buffer che contiene i dati di cui è stato effettuato il marshalling. Una singola chiamata di serializzazione può effettuare diverse chiamate a queste routine.

Lo stile di serializzazione incrementale usa le routine seguenti:

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

I prototipi per le funzioni Alloc, Read e Write che è necessario fornire sono illustrati di seguito:

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

L'input di stato un parametro per tutte e tre le funzioni è il puntatore definito dall'applicazione associato all'handle dei servizi di codifica. L'applicazione può utilizzare questo puntatore per accedere alla struttura contenente informazioni specifiche dell'applicazione, ad esempio un handle di file o un puntatore di flusso. Si noti che gli stub non modificano il puntatore di stato diverso da per passarlo alle funzioni Alloc, Read e Write. Durante la codifica, viene chiamato Alloc per ottenere un buffer in cui vengono serializzati i dati. Viene quindi chiamata la scrittura per consentire all'applicazione di controllare quando e dove vengono archiviati i dati serializzati. Durante la decodifica, viene chiamato Read per restituire il numero richiesto di byte di dati serializzati dalla posizione in cui l'applicazione lo ha archiviato.

Una funzionalità importante dello stile incrementale è che l'handle mantiene automaticamente il puntatore di stato. Questo puntatore mantiene lo stato e non viene mai toccato dalle funzioni RPC, tranne quando il puntatore viene passato a una funzione di allocazione, scrittura o lettura. L'handle gestisce anche uno stato interno che consente di codificare e decodificare diverse istanze di tipo nello stesso buffer aggiungendo spaziatura interna in base alle esigenze per l'allineamento. La funzione [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) Reimposta un handle sullo stato iniziale per consentire la lettura o la scrittura dall'inizio del buffer.

Le funzioni Alloc e Write, insieme a un puntatore definito dall'applicazione, sono associate a un handle di servizi di codifica tramite una chiamata alla funzione [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) . **MesEncodeIncrementalHandleCreate** alloca la memoria necessaria per l'handle, quindi la Inizializza.

L'applicazione può chiamare [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) per creare un handle di decodifica, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) per reinizializzare l'handle o [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle. La funzione Read, insieme a un parametro definito dall'applicazione, è associata a un handle di decodifica mediante una chiamata alla routine **MesDecodeIncrementalHandleCreate** . La funzione crea l'handle e lo inizializza.

I parametri UserState, Alloc, Write e Read di [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) possono essere **null** per indicare che non sono state apportate modifiche.

 

 




