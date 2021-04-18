---
title: Costanti notifiche e messaggi di input del puntatore
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per i messaggi di input del puntatore e le costanti di notifica.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334398"
---
# <a name="pointer-input-messages-and-notifications-constants"></a>Costanti notifiche e messaggi di input del puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per [i messaggi di input del puntatore e](messages-and-notifications-portal.md) le costanti di notifica.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stato del tasto di modifica**](modifier-key-states-constants.md)<br/>            | Indica i tasti di modifica della tastiera che sono stati premuti al momento della generazione dell'input.<br/>                                                                                                       |
| [**Flag di penna**](pen-flags-constants.md)<br/>                               | Valori che possono essere visualizzati nel campo **penFlags** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                         |
| [**Maschera di penna**](pen-mask-constants.md)<br/>                                 | Valori che possono essere visualizzati nel campo **penMask** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                          |
| [**Modifica dispositivo puntatore**](pointer-device-change-constants.md)<br/>       | Valori che possono essere passati nel parametro *wParam* del messaggio di [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .<br/>                                                                    |
| [**Flag puntatore**](pointer-flags-contants.md)<br/>                        | Valori che possono essere visualizzati nel campo **pointerFlags** della struttura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                              |
| [**Flag messaggi puntatore**](pointer-message-flags.md)<br/>                 | Valori utilizzati in diverse macro del puntatore (vedere [macro](macros.md)).<br/>                                                                                                                       |
| [**Flag tocco**](touch-flags-constants.md)<br/>                           | Valori che possono essere visualizzati nel campo **touchFlags** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                   |
| [**Finestra hit testing tocco**](touch-hit-testing-window-constants.md)<br/> | Indica la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .<br/> |
| [**Touch mask**](touch-mask-constants.md)<br/>                             | Valori che possono essere visualizzati nel campo **touchMask** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al messaggio di input del puntatore](wmpointer-reference.md)
</dt> </dl>

 

