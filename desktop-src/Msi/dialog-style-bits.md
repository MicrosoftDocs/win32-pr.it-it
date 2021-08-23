---
description: Lo stile di una finestra di dialogo viene specificato nella colonna Attributi della tabella Finestra di dialogo da una parola a 32 bit composta da flag di bit di stile.
ms.assetid: aad719e8-86b3-4b2b-b417-db55013f8d3a
title: Bit di stile della finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43742c61c8dfe0827d0d51c7f9c8a2de60116500b6fdca3e404a08e120ac4348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947443"
---
# <a name="dialog-style-bits"></a>Bit di stile della finestra di dialogo

Lo stile di una finestra di dialogo [](dialog-table.md) viene specificato nella colonna Attributi della tabella Finestra di dialogo da una parola a 32 bit composta da flag di bit di stile.

Nell'elenco seguente vengono forniti i collegamenti alle descrizioni dei bit di stile della finestra di dialogo riservata.



| Nome                                                      | Decimal | Valore esadecimale | Costante                                                                                                                                       |
|-----------------------------------------------------------|---------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visible](visible-dialog-style-bit.md)                   | 1       | 0x00000001  | **msidbDialogAttributesVisible**                                                                                                               |
| [Modale](modal-dialog-style-bit.md)                       | 2       | 0x00000002  | **MsidbDialogAttributesModal**                                                                                                                 |
| [Riduci](minimize-dialog-style-bit.md)                 | 4       | 0x00000004  | **msidbDialogAttributesMinimize**                                                                                                              |
| [SysModal](sysmodal-dialog-style-bit.md)                 | 8       | 0x00000008  | **msidbDialogAttributesSysModal**                                                                                                              |
| [KeepModeless](keepmodeless-dialog-style-bit.md)         | 16      | 0x00000010  | **msidbDialogAttributesKeepModeless**                                                                                                          |
| [TrackDiskSpace](trackdiskspace-dialog-style-bit.md)     | 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace**                                                                                                        |
| [UseCustomPalette](usecustompalette-dialog-style-bit.md) | 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette**                                                                                                      |
| [RTLRO](rtlro-dialog-style-bit.md)                       | 128     | 0x00000080  | **msidbDialogAttributesRTLRO**                                                                                                                 |
| [RightAligned](rightaligned-dialog-style-bit.md)         | 256     | 0x00000100  | **msidbDialogAttributesRightAligned**                                                                                                          |
| [LeftScroll](leftscroll-dialog-style-bit.md)             | 512     | 0x00000200  | **msidbDialogAttributesLeftScroll**                                                                                                            |
| [Bidi](bidi-dialog-style-bit.md)                         | 896     | 0x00000380  | **msidbDialogAttributesBiDi**  =  **msidbDialogAttributesRTLRO** \| **msidbDialogAttributesRightAligned** \| **msidbDialogAttributesLeftScroll** |
| [Error (Errore) (Error (Errore)e)](error-dialog-style-bit.md)                       | 65536   | 0x00010000  | **MsidbDialogAttributesError**                                                                                                                 |



 

 

 



