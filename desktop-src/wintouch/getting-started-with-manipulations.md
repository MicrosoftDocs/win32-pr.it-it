---
title: Modifiche
description: Questa sezione illustra la manipolazione degli oggetti per Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Tocco, manipolazioni
- manipolazioni, informazioni
- manipolazioni, differenze di movimento
- movimenti, differenze di manipolazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5368b39de1f35cc9a547bc240fc3c984fc1f10f658972b0f845a965e09bb29c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435986"
---
# <a name="manipulations"></a>Modifiche

Questa sezione illustra la manipolazione degli oggetti per Windows Touch.

## <a name="manipulation-overview"></a>Panoramica della manipolazione

Un modo pratico per pensare alle manipolazioni è considerarle come un superset di movimenti. Le operazioni che è possibile eseguire con i movimenti sono più flessibili e con precisione più fine usando le manipolazioni. La differenza tra manipolazioni e movimenti è illustrata meglio con un semplice esempio. È possibile espandere un oggetto e contemporaneamente tradurlo usando le modifiche; con i movimenti, è possibile eseguire una sola operazione alla volta. Questa possibilità di modificare un oggetto in tempo reale rende le applicazioni più intuitive per gli utenti consentendo un'esperienza più realistica.

Le API di manipolazione vengono usate per semplificare le operazioni di trasformazione sugli oggetti per le applicazioni abilitate per il tocco. Le modifiche vengono eseguite nella Windows 7 tramite l'oggetto COM di manipolazione. Usando le modifiche, gli sviluppatori possono supportare più facilmente l'inerzia (fisica degli oggetti) e possono eseguire facilmente trasformazioni sugli oggetti in modo coerente con altre applicazioni. Le sezioni seguenti illustrano vari modi in cui è possibile eseguire modifiche.



| Sezione                                                                                            | Descrizione                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aggiunta del supporto di manipolazione al codice non gestito](adding-manipulation-support-in-unmanaged-code.md) | Viene illustrato come implementare un sink di evento per [**\_ l'interfaccia IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) e aggiungere gestori eventi al codice. |
| [Modifiche avanzate](advanced-manipulations.md)                                               | Viene illustrato come eseguire modifiche complesse.                                                                                                       |
| [Rotazione di un dito singolo](single-finger-rotation.md)                                               | Viene illustrato come ruotare un oggetto usando un punto pivot e il processore di manipolazione.                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche e inerzia](manipulation-and-inertia.md)
</dt> </dl>

 

 




