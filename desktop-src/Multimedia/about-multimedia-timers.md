---
title: Informazioni sui timer multimediali
description: Informazioni sui timer multimediali
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows Multimedia, timer
- Multimedia, timer
- input multimediale, timer
- timer multimediali, informazioni
- timer, informazioni
- timer multimediali, eventi di pianificazione
- timer, eventi di pianificazione
- pianificazione degli eventi del timer
- temporizzazione ad alta risoluzione
- Funzione setimer
- CreateWaitableTimer (funzione)
- Messaggi di WM_TIMER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046681"
---
# <a name="about-multimedia-timers"></a>Informazioni sui timer multimediali

I servizi timer multimediali consentono alle applicazioni di pianificare gli eventi del timer con la massima risoluzione (o accuratezza) possibile per la piattaforma hardware. Questi servizi timer multimediali consentono di pianificare gli eventi del timer a una risoluzione superiore rispetto ad altri servizi timer.

Questi servizi timer sono utili per le applicazioni che richiedono tempi di risoluzione elevata. Ad esempio, un sequencer MIDI richiede un timer ad alta risoluzione, perché deve mantenere la velocità degli eventi MIDI entro una risoluzione di 1 millisecondo.

Le applicazioni che non usano la temporizzazione ad alta risoluzione devono usare la funzione [setimer](/windows/win32/api/winuser/nf-winuser-settimer) anziché i servizi timer multimediali. I servizi timer forniti da **setimer** inviano messaggi del [ \_ timer WM](../winmsg/wm-timer.md) a una coda di messaggi, mentre i servizi timer multimediali chiamano una funzione di callback. Le applicazioni che vogliono un timer in attesa devono usare la funzione [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .

 

 