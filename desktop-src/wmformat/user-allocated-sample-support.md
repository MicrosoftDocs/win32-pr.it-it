---
title: Supporto di esempio allocato dall'utente
description: Supporto di esempio allocato dall'utente
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK, supporto di esempio allocato dall'utente
- ASF (Advanced Systems Format), supporto di esempio allocato dall'utente
- ASF (Advanced Systems Format), supporto di esempio allocato dall'utente
- supporto di esempio allocato dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044473"
---
# <a name="user-allocated-sample-support"></a>Supporto di esempio allocato dall'utente

In circostanze normali, sia l'oggetto Reader che l'oggetto Reader sincrono creano un nuovo oggetto buffer per ogni esempio recapitato all'applicazione. Questo è dovuto al fatto che l'oggetto di lettura non è in grado di conoscere il funzionamento dell'applicazione con gli esempi dopo averlo ottenuto. Sebbene molte applicazioni leggano esempi solo per eseguirne il rendering immediatamente, è possibile che alcune applicazioni debbano gestire i campioni per un lungo periodo di tempo. L'oggetto di lettura non può, pertanto, riutilizzare i buffer allocati; li recapita all'applicazione, che quindi ne ha il controllo.

Il problema di questo approccio è che un file può contenere un numero immenso di esempi. Se ognuno di essi richiede la creazione di un nuovo oggetto buffer, l'allocazione e il rilascio della memoria di una quantità eccessiva di tempo del processore. In applicazioni sensibili al tempo, ad esempio lettori multimediali, questo overhead può essere molto dannoso per le prestazioni.

Per attenuare i problemi di prestazioni degli esempi allocati dal lettore, sia il Reader che il lettore sincrono supportano gli esempi allocati dall'utente. Per usare gli esempi allocati dall'applicazione, l'oggetto di lettura effettua chiamate a un metodo di callback di allocazione di esempio che viene implementato. La logica utilizzata dal callback per recapitare i buffer all'oggetto di lettura dipende interamente dall'utente. È possibile utilizzare un pool di buffer per l'intero file o utilizzare più pool di buffer, uno per ogni output o flusso o qualsiasi altro schema che funziona per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Allocazione di buffer per la lettura di file**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Funzionalità di lettura file**](file-reading-features.md)
</dt> </dl>

 

 




