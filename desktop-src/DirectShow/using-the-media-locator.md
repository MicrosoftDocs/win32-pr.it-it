---
description: Uso del localizzatore multimediale
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Uso del localizzatore multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be064a375f121f7c4e3dad54c2615bf8d6f7df489e119ec9cbb2c6f4b4294628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633131"
---
# <a name="using-the-media-locator"></a>Uso del localizzatore multimediale

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Il localizzatore multimediale è un oggetto helper che verifica i nomi dei file e cerca i file mancanti nelle directory locali o di rete. Il rilevatore multimediale mantiene una cache dei percorsi di directory in cui sono stati trovati correttamente i file nelle ricerche precedenti. Per individuare un file, esegue la ricerca nelle directory nella cache. In caso contrario, media detector può visualizzare una finestra di dialogo Apri file in cui l'utente può individuare un file manualmente. Supponendo che l'utente individua il file, il localizzatore multimediale aggiunge la nuova directory alla cache. Il localizzatore multimediale espone [**l'interfaccia IMediaLocator.**](imedialocator.md)

In genere, l'applicazione non crea direttamente un'istanza del localizzatore multimediale. Al contrario, la sequenza temporale e il motore di rendering forniscono i metodi seguenti per convalidare i nomi di file usando il rilevatore multimediale.

-   Per convalidare i nomi di file nella sequenza temporale, chiamare [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md). Facoltativamente, questo metodo aggiorna anche gli oggetti di origine con i nomi di file corretti.
-   Per convalidare i nomi dei file quando viene eseguito il rendering del progetto, chiamare [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Entrambi i metodi accettano flag che controllano il comportamento del localizzatore multimediale. Ad esempio, è possibile limitare la ricerca alle directory locali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle origini](working-with-sources.md)
</dt> </dl>

 

 



