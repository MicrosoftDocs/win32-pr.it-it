---
title: Chiavi che terminano l'acquisizione
description: Chiavi che terminano l'acquisizione
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- Struttura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140051"
---
# <a name="keys-ending-capture"></a>Chiavi che terminano l'acquisizione

È possibile consentire all'utente di interrompere una sessione di acquisizione premendo un tasto o una combinazione di tasti dalla tastiera o premendo il pulsante destro o sinistro del mouse. Se l'utente interrompe una sessione di acquisizione in tempo reale, il contenuto del file di acquisizione viene eliminato. Se l'utente interrompe una sessione di acquisizione step-frame, il contenuto del file di acquisizione fino al punto di interruzione dell'acquisizione viene salvato.

È possibile recuperare le impostazioni per l'interruzione di una sessione di acquisizione usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) L'impostazione corrente della sequenza di tasti viene archiviata nel membro **vKeyAbort** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) le impostazioni correnti del mouse vengono archiviate nei **membri fAbortLeftMouse** e **fAbortRightMouse.** È possibile impostare una nuova combinazione di tasti o combinazione di tasti specificando la combinazione keycode o keycode (come in una combinazione di tasti CTRL o MAIUSC) come valore di **vKeyAbort** oppure impostare il pulsante sinistro o destro del mouse come tasto di interruzione specificando il membro **fAbortLeftMouse** o **fAbortRightMouse.** Dopo aver impostato questi membri, inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Il valore predefinito di **vKeyAbort** è VK \_ ESCAPE. È necessario chiamare la [funzione RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) prima di specificare una sequenza di tasti che può interrompere una sessione di acquisizione. I valori predefiniti **di fAbortLeftMouse** e **fAbortRightMouse** sono **TRUE.**

 

 