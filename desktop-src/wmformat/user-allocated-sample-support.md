---
title: Supporto di esempio allocato dall'utente
description: Supporto di esempio allocato dall'utente
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK, supporto di esempio allocato dall'utente
- Advanced Systems Format (ASF), supporto di esempio allocato dall'utente
- ASF (Advanced Systems Format), supporto di esempio allocato dall'utente
- Supporto dell'esempio allocato dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8cba2d20586cc47845d961e5c92a0138a37d5d0db07feb23dbb68dda1b72eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845255"
---
# <a name="user-allocated-sample-support"></a>Supporto di esempio allocato dall'utente

In circostanze normali, sia l'oggetto lettore che l'oggetto lettore sincrono creano un nuovo oggetto buffer per ogni esempio recapitato all'applicazione. Ciò è dovuto al fatto che l'oggetto di lettura non ha modo di sapere cosa fa l'applicazione con gli esempi dopo averli raccolti. Anche se molte applicazioni leggono gli esempi solo per eseguirne immediatamente il rendering, alcune applicazioni potrebbero dover mantenere gli esempi per molto tempo. L'oggetto di lettura non può pertanto riutilizzare i buffer allocati. li recapita all'applicazione, che ha quindi il controllo su di essi.

Il problema di questo approccio è che un file può contenere un numero elevato di esempi. Se ognuno di essi richiede la creazione di un nuovo oggetto buffer, molto tempo del processore viene sprecato per l'allocazione e il rilascio della memoria. Nelle applicazioni sensibili al tempo, ad esempio i lettori multimediali, questo sovraccarico può essere molto dannoso per le prestazioni.

Per ridurre i problemi di prestazioni degli esempi allocati dal lettore, sia il lettore che il lettore sincrono supportano gli esempi allocati dall'utente. Per usare gli esempi allocati dall'applicazione, l'oggetto di lettura effettua chiamate a un metodo di callback di allocazione di esempio implementato dall'utente. La logica usata dal callback per recapitare buffer all'oggetto di lettura dipende interamente dall'utente. È possibile usare un pool di buffer per l'intero file o più pool di buffer, uno per ogni output o flusso o qualsiasi altro schema compatibile con l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Allocazione di buffer per la lettura di file**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Funzionalità di lettura file**](file-reading-features.md)
</dt> </dl>

 

 




