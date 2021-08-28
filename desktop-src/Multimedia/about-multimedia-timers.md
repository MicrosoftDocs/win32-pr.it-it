---
title: Informazioni sui timer multimediali
description: Informazioni sui timer multimediali
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows multimediali, timer
- multimediali, timer
- input multimediale, timer
- timer multimediali, informazioni
- timer, informazioni
- timer multimediali, pianificazione di eventi
- timer, pianificazione di eventi
- pianificazione di eventi timer
- temporizzazione ad alta risoluzione
- Funzione SetTimer
- Funzione CreateWaitableTimer
- WM_TIMER messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b5d899c93f0f292d7ef45e8584ae9e2b5e0e001037c456dcc4900f1c0d3f26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498211"
---
# <a name="about-multimedia-timers"></a>Informazioni sui timer multimediali

I servizi timer multimediali consentono alle applicazioni di pianificare gli eventi timer con la massima risoluzione (o accuratezza) possibile per la piattaforma hardware. Questi servizi timer multimediali consentono di pianificare gli eventi timer con una risoluzione più elevata rispetto ad altri servizi timer.

Questi servizi timer sono utili per le applicazioni che richiedono tempi ad alta risoluzione. Ad esempio, un sequencer MIDI richiede un timer ad alta risoluzione perché deve mantenere il ritmo degli eventi MIDI entro una risoluzione di 1 millisecondo.

Le applicazioni che non usano tempi ad alta risoluzione devono usare la [funzione SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) anziché i servizi timer multimediali. I servizi timer forniti da **SetTimer** pubblicano [messaggi WM \_ TIMER](../winmsg/wm-timer.md) in una coda di messaggi, mentre i servizi timer multimediali chiamano una funzione di callback. Le applicazioni che vogliono un timer waitable devono usare la [funzione CreateWaitableTimer.](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)

 

 