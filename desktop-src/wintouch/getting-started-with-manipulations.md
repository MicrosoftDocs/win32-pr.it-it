---
title: Modifiche
description: In questa sezione viene illustrata la manipolazione degli oggetti per Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, modifiche
- modifiche, informazioni
- manipolazioni, differenze di movimento
- movimenti, differenze di manipolazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328615"
---
# <a name="manipulations"></a>Modifiche

In questa sezione viene illustrata la manipolazione degli oggetti per Windows Touch.

## <a name="manipulation-overview"></a>Panoramica della manipolazione

Un modo pratico per considerare le manipolazioni consiste nel considerare un superset dei movimenti. Che cosa è possibile fare con i movimenti, è possibile farlo con una maggiore flessibilità e con precisione maggiore usando le manipolazioni. La differenza tra le modifiche e i movimenti è illustrata in modo ottimale con un semplice esempio. È possibile espandere un oggetto e allo stesso tempo convertirlo utilizzando le modifiche. con i movimenti è possibile eseguire una sola operazione alla volta. La possibilità di modificare un oggetto in tempo reale rende le applicazioni più intuitive per gli utenti, consentendo un'esperienza più realistica.

Le API di manipolazione vengono usate per semplificare le operazioni di trasformazione sugli oggetti per le applicazioni abilitate per il tocco. Le modifiche vengono eseguite in Windows 7 tramite l'oggetto COM di manipolazione. Utilizzando le modifiche, gli sviluppatori possono supportare più facilmente l'inerzia (fisica degli oggetti) e possono eseguire facilmente trasformazioni sugli oggetti in modo coerente con altre applicazioni. Nelle sezioni seguenti vengono illustrati i vari modi in cui è possibile eseguire le modifiche.



| Sezione                                                                                            | Descrizione                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aggiunta del supporto per la manipolazione a codice non gestito](adding-manipulation-support-in-unmanaged-code.md) | Viene illustrato come implementare un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) e aggiungere gestori di eventi al codice. |
| [Manipolazioni avanzate](advanced-manipulations.md)                                               | Viene illustrato come eseguire manipolazioni complesse.                                                                                                       |
| [Rotazione di un singolo dito](single-finger-rotation.md)                                               | Viene illustrato come ruotare un oggetto utilizzando un punto pivot e il processore di manipolazione.                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche e inerzia](manipulation-and-inertia.md)
</dt> </dl>

 

 




