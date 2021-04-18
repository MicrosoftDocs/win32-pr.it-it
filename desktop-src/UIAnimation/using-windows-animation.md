---
title: Attività di animazione Windows
description: Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che utilizzano Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animazione Windows Animation Windows, attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298705"
---
# <a name="windows-animation-tasks"></a>Attività di animazione Windows

Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che utilizzano Windows Animation Manager.

Queste attività, in ordine, includono:

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creare gli oggetti animazione principali](adding-animation-to-an-application.md)<br/>               | Per utilizzare l'animazione Windows nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti animazione principali.<br/>                                                                                                                                                                           |
| [Creare variabili di animazione](create-animation-variables.md)<br/>                              | Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando l'animazione di Windows.<br/>                                                                                                                                                            |
| [Aggiornare gestione animazioni e creare frame](introducing-windows-animation-manager.md)<br/> | Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione. L'ora corrente è necessaria anche quando si indica al gestore delle animazioni di aggiornare lo stato e impostare tutte le variabili di animazione sui valori interpolati appropriati.<br/> |
| [Leggere i valori delle variabili di animazione](updating---application-driven-animation.md)<br/>         | Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.<br/>                                                                                                                                  |
| [Creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md)<br/>          | Per creare un'animazione, un'applicazione deve costruire uno storyboard.<br/>                                                                                                                                                                                                                        |
| [Pianificare uno storyboard](scheduling-a-storyboard.md)<br/>                                      | Dopo la creazione di uno storyboard, questo viene pianificato dal gestore dell'animazione.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sull'animazione Windows](scenic-animation-api-overview.md)
</dt> <dt>

[Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)
</dt> <dt>

[Esempi di animazioni Windows](windows-animation-samples.md)
</dt> </dl>

 

 





