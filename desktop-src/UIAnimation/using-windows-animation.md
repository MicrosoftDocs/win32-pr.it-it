---
title: Windows Attività di animazione
description: Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che usano Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows Animazione Windows animation ,tasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8f5116a6e36697e649ad81bfbad883c57aee50440c3ba80734419ce2fb372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058149"
---
# <a name="windows-animation-tasks"></a>Windows Attività di animazione

Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che usano Windows Animation Manager.

Queste attività, nell'ordine, includono:

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creare gli oggetti di animazione principali](adding-animation-to-an-application.md)<br/>               | Per usare Windows'animazione nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti di animazione principali.<br/>                                                                                                                                                                           |
| [Creare variabili di animazione](create-animation-variables.md)<br/>                              | Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando Windows Animation.<br/>                                                                                                                                                            |
| [Aggiornare Gestione animazioni e disegnare fotogrammi](introducing-windows-animation-manager.md)<br/> | Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione. L'ora corrente è necessaria anche quando il gestore dell'animazione deve aggiornare lo stato e impostare tutte le variabili di animazione ai valori interpolati appropriati.<br/> |
| [Leggere i valori delle variabili di animazione](updating---application-driven-animation.md)<br/>         | Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.<br/>                                                                                                                                  |
| [Creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md)<br/>          | Per creare un'animazione, un'applicazione deve costruire uno storyboard.<br/>                                                                                                                                                                                                                        |
| [Pianificare uno storyboard](scheduling-a-storyboard.md)<br/>                                      | Dopo la creazione, uno storyboard viene pianificato dal gestore dell'animazione.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Panoramica dell'animazione](scenic-animation-api-overview.md)
</dt> <dt>

[Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)
</dt> <dt>

[Windows Esempi di animazione](windows-animation-samples.md)
</dt> </dl>

 

 





