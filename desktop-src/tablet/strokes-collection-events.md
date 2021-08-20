---
description: La tabella seguente descrive i thread su cui possono essere generati gli eventi della raccolta Strokes. EventThreadsStrokesAddedFires sul thread di input penna o sul thread del chiamante. Un evento StrokesAdded generato dall'interazione dell'utente con l'oggetto InkCollector, l'oggetto InkOverlay o il controllo InkPicture viene generato sul thread di input penna. StrokesRemovedFires sul thread di input penna o sul thread del chiamante. Un evento StrokesRemoved generato dall'interazione dell'utente con l'oggetto InkCollector, l'oggetto InkOverlay o il controllo InkPicture viene generato sul thread di input penna.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventi della raccolta Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589781"
---
# <a name="strokes-collection-events"></a>Eventi della raccolta Strokes

La tabella seguente descrive i thread su cui possono essere generati gli eventi della raccolta [**Strokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))



| Event                                               | Thread                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Viene generato sul thread di input penna o sul thread del chiamante.<br/> Un [**evento StrokesAdded**](inkstrokes-strokesadded.md) generato dall'interazione dell'utente con l'oggetto [**InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) o il [controllo InkPicture](inkpicture-control-reference.md) viene generato sul thread di input penna.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Viene generato sul thread di input penna o sul thread del chiamante.<br/> Un [**evento StrokesRemoved**](inkstrokes-strokesremoved.md) generato dall'interazione dell'utente con l'oggetto [**InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) viene generato sul thread di input penna.<br/> |



 

 

 
