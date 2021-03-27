---
description: Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.
title: Linee guida per il gestore di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882797"
---
# <a name="preview-handler-guidelines"></a>Linee guida per il gestore di anteprime

Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.

-   Un'anteprima dovrebbe contenere un'interfaccia utente minima: è semplicemente un'anteprima. Dovrebbe visualizzare solo il contenuto del file. Non devono essere visualizzate finestre di dialogo, schermate iniziali, barre degli strumenti o riquadri attività. Il riquadro di lettura verrà usato in genere insieme alla ricerca per identificare rapidamente un file. È consigliabile evitare qualsiasi elemento che ingombra il riquadro di lettura o altrimenti si sottrae dal contenuto del file o causa un ritardo nella visualizzazione dell'anteprima.
-   L'anteprima dovrebbe consentire all'utente di spostarsi nel documento. L'utente deve inoltre essere in grado di selezionare e copiare il testo.
-   L'anteprima non deve essere a elevato utilizzo di memoria, deve utilizzare risorse minime e deve avere un tempo di avvio rapido.
-   L'esecuzione di tutti gli script e le macro nel file visualizzato in anteprima dovrebbe essere bloccata a scopo di sicurezza e privacy.
-   L'anteprima deve supportare tasti di scelta rapida per la navigazione e la selezione come supportato dall'applicazione. Deve inoltre visualizzare un menu di scelta rapida quando si fa clic con il pulsante destro del mouse.
-   Quando un file viene visualizzato come anteprima, l'anteprima non deve bloccare il file stesso. Un file può essere visualizzato in anteprima e aperto nell'applicazione associata nello stesso momento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprime e host di anteprima della shell](preview-handlers.md)
</dt> <dt>

[Compilazione di gestori di anteprime](building-preview-handlers.md)
</dt> </dl>

 

 



