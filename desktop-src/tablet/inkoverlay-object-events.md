---
description: "La tabella seguente descrive i thread in cui possono essere generati gli eventi dell'oggetto InkOverlay. EventThreadsCursorButtonDownFires sul thread di input pennaCursorButtonUpFires sul thread di input pennaCursorDownFires sul thread di input pennaCursorInRangeFires sul thread di input pennaCursorOutOfRangeFires nel thread inkDoubleClick (solo automazione). Viene generato sul thread dell'interfaccia utente dell'applicazioneDoubleClick (solo libreria gestita). Viene generato sul thread dell'interfaccia utente dell'applicazioneGestureFires sul thread di input pennaMouseDownFires nel thread ui dell'applicazioneMouseMoveFires nel thread ui dell'applicazioneMouseUpFires nel thread ui dell'applicazioneMouseWheelFires on thread UI dell'applicazioneNewInAirPacketsFires sul thread di input pennaNewPacketsFires sul thread di input pennaPaintedFires nel thread ui dell'applicazionePaintingFires nel thread ui dell'applicazioneSelectionChangedFires sul thread di input penna, o sul thread che aggiorna l'oggetto InkOverlay  Proprietà SelectionSelectionChangingFires sul thread di input pennaSelectionMovedFires sul thread di input pennaSelectionMovingFires nel thread di input pennaSelectionResizedFires sul thread di input pennaSelectionResizingFires sul thread di input pennaStrokesDeletedFires sul thread di input pennaStrokesDeletingFires sul thread di input pennaSystemGestureFires sul thread di input pennaTabletAddedFires sul thread di input pennaTabletRemovedFires sul thread di input penna "
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventi dell'oggetto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ee197a14edf3ce0aa8595bdbcdb3ea2937d9cf863dcc6e95690088ed8ee96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218964"
---
# <a name="inkoverlay-object-events"></a>Eventi dell'oggetto InkOverlay

La tabella seguente descrive i thread in cui possono essere generati [**gli eventi dell'oggetto InkOverlay.**](inkoverlay-class.md)



| Evento                                                                             | Thread                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**Cursorinrange**](inkoverlay-cursorinrange.md)                                 | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (solo Automazione).                  | Viene generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (solo libreria gestita). | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Movimento**](inkoverlay-gesture.md)                                             | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**Mousedown**](inkoverlay-mousedown.md)                                         | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Mousemove**](inkoverlay-mousemove.md)                                         | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Mouseup**](inkoverlay-mouseup.md)                                             | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Mousewheel**](inkoverlay-mousewheel.md)                                       | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**Dipinto**](inkoverlay-painted.md)                                             | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Pittura**](inkoverlay-painting.md)                                           | Viene generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Viene generato sul thread di input penna o sul thread che aggiorna la proprietà [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) dell'oggetto [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**Selectionchanging**](inkoverlay-selectionchanging.md)                         | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**Selectionresizing**](inkoverlay-selectionresizing.md)                         | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**infarto**](inkoverlay-stroke.md)                                               | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**TabletAggiunta**](inkoverlay-tabletadded.md)                                     | Viene generato sul thread di input penna<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Viene generato sul thread di input penna<br/>                                                                                                                                        |



 

 

