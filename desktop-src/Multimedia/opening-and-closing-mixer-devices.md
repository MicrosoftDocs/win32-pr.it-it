---
title: Apertura e chiusura di dispositivi mixer
description: Apertura e chiusura di dispositivi mixer
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimediale, apertura di dispositivi mixer
- audio, apertura di dispositivi mixer
- mixer audio, apertura
- mixer, apertura
- audio multimediale, chiusura di dispositivi mixer
- audio, chiusura di dispositivi mixer
- mixer audio, chiusura
- mixer, chiusura
- apertura di dispositivi mixer
- chiusura di dispositivi mixer
- identificatori di dispositivo e handle del dispositivo
- mixer audio, identificatori di dispositivo e handle del dispositivo
- mixer, identificatori di dispositivo e handle del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046592"
---
# <a name="opening-and-closing-mixer-devices"></a>Apertura e chiusura di dispositivi mixer

Quando si vuole usare un dispositivo mixer, è sufficiente iniziare a usarlo oppure è possibile aprire il dispositivo in modo esplicito prima di usarlo. L'apertura esplicita di un dispositivo mixer offre due vantaggi principali:

-   Garantisce la continua esistenza del dispositivo mixer.
-   Consente di ricevere la notifica delle modifiche della riga audio e del controllo.

È possibile usare la funzione [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) per aprire in modo esplicito un dispositivo mixer. Questa funzione accetta come parametri un identificatore di dispositivo, un puntatore a una posizione di memoria e altri valori univoci per ogni tipo di dispositivo. La posizione di memoria viene riempita con un handle di dispositivo. Usare questo handle di dispositivo per identificare il dispositivo mixer aperto quando si chiamano altre funzioni del mixer audio. Fino a quando un handle di un dispositivo mixer esiste, il dispositivo continua a esistere nel sistema. Se viene apportata una modifica alla configurazione del dispositivo mixer e non è stata aperta in modo esplicito, l'applicazione potrebbe non essere in grado di accedervi improvvisamente.

> [!Note]  
> La differenza tra gli identificatori di dispositivo e gli handle del dispositivo è importante. Gli handle di dispositivo vengono restituiti quando si apre un driver di dispositivo usando **mixerOpen**. Gli identificatori di dispositivo sono determinati in modo implicito dal numero di dispositivi presenti in un sistema; Questo numero viene ottenuto tramite la funzione [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .

 

Per chiudere un dispositivo mixer, è possibile usare la funzione [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) . Dopo aver completato l'uso, è necessario chiudere il dispositivo.

 

 