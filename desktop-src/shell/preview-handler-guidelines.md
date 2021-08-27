---
description: Quando si fornisce un'anteprima, è necessario seguire le linee guida seguenti.
title: Linee guida per i gestori di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719629"
---
# <a name="preview-handler-guidelines"></a>Linee guida per i gestori di anteprima

Quando si fornisce un'anteprima, è necessario seguire le linee guida seguenti.

-   Un'anteprima deve contenere un'interfaccia utente minima, ma è semplicemente un'anteprima. Dovrebbe visualizzare solo il contenuto del file. Non deve visualizzare finestre di dialogo, schermate iniziali, barre degli strumenti o riquadri attività. Il riquadro di lettura verrà in genere usato insieme alla ricerca per identificare rapidamente un file. È consigliabile evitare qualsiasi elemento che ingombra il riquadro di lettura o che in altro modo sminera il contenuto del file o causa ritardi nella visualizzazione in anteprima.
-   L'anteprima deve consentire all'utente di spostarsi nel documento. L'utente deve anche essere in grado di selezionare e copiare il testo.
-   L'anteprima non deve essere a elevato utilizzo di memoria, deve utilizzare risorse minime e deve avere un tempo di avvio rapido.
-   L'esecuzione di tutti gli script e le macro nel file visualizzato in anteprima deve essere bloccata per motivi di sicurezza e privacy.
-   L'anteprima deve supportare i tasti di scelta rapida per la navigazione e la selezione, come supportato dall'applicazione. Dovrebbe anche visualizzare un menu di scelta rapida quando si fa clic con il pulsante destro del mouse.
-   Quando un file viene visualizzato come anteprima, l'anteprima non deve bloccare il file stesso. Un file può essere visualizzato in anteprima e aperto contemporaneamente nell'applicazione associata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprima e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Compilazione di gestori di anteprima](building-preview-handlers.md)
</dt> </dl>

 

 



