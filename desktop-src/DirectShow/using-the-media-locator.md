---
description: Uso di media Locator
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Uso di media Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968851"
---
# <a name="using-the-media-locator"></a>Uso di media Locator

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il localizzatore multimediale è un oggetto helper che verifica i nomi di file e cerca i file mancanti nelle directory locali o di rete. Il rilevatore multimediale mantiene una cache dei percorsi di directory in cui i file sono stati trovati correttamente nelle ricerche precedenti. Per individuare un file, Cerca le directory nella relativa cache. In caso contrario, il rilevatore multimediale può visualizzare una finestra di dialogo Apri file in cui l'utente può individuare manualmente un file. Supponendo che l'utente trovi il file, il localizzatore multimediale aggiunge la nuova directory alla cache. Il localizzatore multimediale espone l'interfaccia [**IMediaLocator**](imedialocator.md) .

In genere, l'applicazione non crea direttamente un'istanza del localizzatore multimediale. Al contrario, la sequenza temporale e il motore di rendering forniscono i metodi seguenti per la convalida dei nomi di file tramite il rilevatore multimediale.

-   Per convalidare i nomi di file nella sequenza temporale, chiamare [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md). Facoltativamente, questo metodo aggiorna anche gli oggetti di origine con i nomi di file corretti.
-   Per convalidare i nomi di file quando viene eseguito il rendering del progetto, chiamare [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Entrambi i metodi accettano flag che controllano il comportamento del localizzatore multimediale. Ad esempio, è possibile limitare la ricerca alle directory locali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di origini](working-with-sources.md)
</dt> </dl>

 

 



