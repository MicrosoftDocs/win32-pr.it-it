---
description: "Nella tabella seguente vengono descritti i thread che gli eventi dell'oggetto InkOverlay possono generare. EventThreadsCursorButtonDownFires sull'input penna threadCursorButtonUpFires sull'input penna threadCursorDownFires sull'input penna threadCursorInRangeFires sull'input penna threadCursorOutOfRangeFires sull'input penna threadDoubleClick (solo automazione). Generato sull'interfaccia utente (UI) threadDoubleClick dell'applicazione (solo libreria gestita). Viene attivato sul threadGestureFires dell'interfaccia utente dell'applicazione nel threadMouseDownFires di input penna sull'interfaccia utente dell'applicazione threadMouseMoveFires sull'interfaccia utente dell'applicazione threadMouseUpFires sull'interfaccia utente dell'applicazione threadMouseWheelFires sull'interfaccia utente dell'applicazione threadNewInAirPacketsFires sull'input penna threadNewPacketsFires sull'input penna threadPaintedFires sull'interfaccia utente dell'applicazione threadPaintingFires sull'interfaccia utente dell'applicazione threadSelectionChangedFires sul thread dell'input penna, o sul thread che aggiorna la selezione dell'oggetto InkOverlay propertySelectionChangingFires sull'input penna threadSelectionMovedFires sull'input penna threadSelectionMovingFires sull'input penna threadSelectionResizedFires sull'input penna threadSelectionResizingFires on input penna threadStrokeFires sull'input penna threadStrokesDeletedFires sull'input penna threadStrokesDeletingFires sull'input penna threadSystemGestureFires sull'input penna threadTabletAddedFires sull'input penna threadTabletRemovedFires sul thread di input penna "
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventi oggetto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316844"
---
# <a name="inkoverlay-object-events"></a>Eventi oggetto InkOverlay

Nella tabella seguente vengono descritti i thread che gli eventi dell'oggetto [**InkOverlay**](inkoverlay-class.md) possono generare.



| Evento                                                                             | Thread                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (solo automazione).                  | Generato nel thread dell'interfaccia utente dell'applicazione<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (solo libreria gestita). | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Movimento**](inkoverlay-gesture.md)                                             | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**MouseDown**](inkoverlay-mousedown.md)                                         | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**MouseMove**](inkoverlay-mousemove.md)                                         | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**MouseWheel**](inkoverlay-mousewheel.md)                                       | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**Dipinto**](inkoverlay-painted.md)                                             | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**Disegno**](inkoverlay-painting.md)                                           | Generato sul thread dell'interfaccia utente dell'applicazione<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Generato sul thread di input penna o sul thread che aggiorna la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) dell'oggetto [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**Stroke**](inkoverlay-stroke.md)                                               | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Generato nel thread di input penna<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Generato nel thread di input penna<br/>                                                                                                                                        |



 

 

