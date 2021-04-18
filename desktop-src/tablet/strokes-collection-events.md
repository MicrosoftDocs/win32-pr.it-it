---
description: La tabella seguente descrive i thread sui quali è possibile attivare gli eventi di raccolta Strokes. EventThreadsStrokesAddedFires sul thread dell'input penna o sul thread del chiamante. Un evento StrokesAdded generato dall'interazione dell'utente con l'oggetto InkCollector, l'oggetto InkOverlay o il controllo InkPicture viene attivato nel thread di input penna. StrokesRemovedFires sul thread dell'input penna o sul thread del chiamante. Un evento StrokesRemoved generato dall'interazione dell'utente con l'oggetto InkCollector, l'oggetto InkOverlay o il controllo InkPicture viene attivato nel thread di input penna.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventi raccolta Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319142"
---
# <a name="strokes-collection-events"></a>Eventi raccolta Strokes

La tabella seguente descrive i thread sui quali è possibile attivare gli eventi di raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .



| Evento                                               | Thread                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Generato sul thread dell'input penna o sul thread del chiamante.<br/> Un evento [**StrokesAdded**](inkstrokes-strokesadded.md) generato dall'interazione dell'utente con l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) viene attivato nel thread di input penna.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Generato sul thread dell'input penna o sul thread del chiamante.<br/> Un evento [**StrokesRemoved**](inkstrokes-strokesremoved.md) generato dall'interazione dell'utente con l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) viene attivato nel thread di input penna.<br/> |



 

 

 
