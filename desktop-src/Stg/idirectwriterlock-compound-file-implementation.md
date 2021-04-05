---
title: IDirectWriterLock-implementazione del file composto
description: L'implementazione del file composto di IDirectWriterLock fornisce un modo per aprire un file composto in modalità diretta con un solo Writer e più lettori.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861935a4c373ce03408c0e633e581e56d39623da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708452"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock-implementazione del file composto

L'implementazione del file composto di [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) fornisce un modo per aprire un file composto in modalità diretta con un solo Writer e più lettori.

I file composti possono essere aperti in modalità diretta usando il \_ flag diretto STGM. L'interfaccia [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) imposta il \_ flag STGM ReadWrite \| STGM \_ share \_ Deny \_ Write come valido in modalità diretta senza richiedere l'overhead di una copia snapshot.

Quando un file composto viene aperto in modalità transazionale usando il \_ flag transazionale STGM, è anche possibile avere più lettori e un singolo writer usando \_ il \| \_ flag di condivisione \_ Nega scrittura STGM ReadWrite STGM \_ . Tuttavia, in questo caso, viene creata una copia snapshot del file per i lettori. Spesso si verifica un sovraccarico di una copia Scratch.

## <a name="when-to-use"></a>Utilizzo

Usare l'implementazione fornita dal sistema di [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) quando si apre una risorsa di archiviazione in modalità diretta (STGM \_ Direct) con la \_ condivisione STGM ReadWrite \| STGM \_ \_ \_ flag Deny Write.

Per ottenere un puntatore a [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock), chiamare **QueryInterface** in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per ottenere l'oggetto di archiviazione radice per il file composto.

Chiamare [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) per ottenere l'accesso in scrittura esclusivo a un file composto. Chiamare [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) per rilasciare l'accesso in scrittura esclusivo.

[**IDirectWriterLock:: HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) indica se il file è attualmente bloccato.

## <a name="remarks"></a>Commenti

L'implementazione del file composto della funzionalità per più lettori a writer singolo è basata sul blocco di intervalli. Il writer Ottiene l'accesso esclusivo alla risorsa di archiviazione da scrivere dopo che tutti i lettori correnti hanno chiuso l'archiviazione. Mentre il writer è attivo, i lettori successivi non possono aprire lo spazio di archiviazione. Il writer chiama [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) per ottenere l'accesso in scrittura esclusivo. Il writer deve quindi chiamare [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) per rilasciare l'archiviazione.

La chiamata a [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) è obbligatoria prima di scrivere in questa modalità a singolo Reader e a più writer. Tenta di scrivere nel file senza chiamare **IDirectWriterLock:: WaitForWriteAccess** per primo risultato in STG \_ E \_ AccessDenied. Questo errore viene restituito anche se il writer ha aperto inizialmente il file e nessun lettore dispone attualmente del file aperto.

## <a name="marshaling-considerations"></a>Considerazioni sul marshalling

Il marshalling personalizzato viene in genere usato quando viene effettuato il marshalling di un file composto in un altro processo nello stesso computer. Quando si esegue il marshalling delle archiviazioni, i diritti di accesso non vengono considerati e il puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) viene passato al nuovo processo con le stesse modalità di accesso e diritti del processo di marshalling originale. Per altre informazioni sulle modalità di accesso, vedere [**costanti STGM**](stgm-constants.md). Durante il marshalling, non viene eseguito o verificato alcun blocco per garantire l'accesso in scrittura esclusivo. In questo caso, non è prevista l'applicazione dei criteri a writer singolo per i file composti aperti in modalità a singolo writer e a più lettori. L'imposizione viene invece gestita internamente dall'implementazione del file composto.

Poiché il puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) viene passato a un altro processo durante il marshalling, è possibile che due processi dispongano di accesso simultaneo allo stesso file composto. Anche se un chiamante potrebbe avere ottenuto l'accesso in scrittura esclusivo all'archiviazione chiamando [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), la versione di cui è stato effettuato il marshalling può anche avere accesso simultaneamente. Le versioni di cui è stato effettuato il marshalling non vengono forzate a chiudere mentre il writer singolo accede al file. In questo caso, l'implementazione del file composto Sincronizza internamente le Scritture.

Se un singolo writer Ottiene l'accesso esclusivo chiamando, [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), anche l'archiviazione con marshalling ha accesso in scrittura e non è necessario chiamare **IDirectWriterLock:: WaitForWriteAccess**. Entrambi i processi hanno accesso in scrittura e la sincronizzazione è controllata dall'implementazione del file composto interno.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




