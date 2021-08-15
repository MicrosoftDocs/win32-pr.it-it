---
description: La classe di dispositivi wave/out è costituita da dispositivi audio per l'output audio wave di basso livello.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3e8a82b8345e8f50e1ad18f527c82f4ece241e03c0ea7cd083dd2d2ae79282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760176"
---
# <a name="waveout"></a>wave/out

La classe di dispositivi wave/out è costituita da dispositivi audio per l'output audio wave di basso livello. È possibile accedere a questi dispositivi usando le funzioni d'onda, descritte in Platform Software Development Kit (SDK). I dispositivi in questa classe sono associati a dispositivi line che supportano il tipo di supporto LINEMEDIAMODE AUTOMATEDVOICE, specificato nel membro \_ **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo line.

Le [**funzioni lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempiono una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Il **membro DeviceId** è l'identificatore di un dispositivo audio chiuso. Questo identificatore viene utilizzato in una chiamata alla [**funzione waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire il dispositivo per l'output. È possibile usare l'handle di dispositivo risultante per riprodurre dati audio digitalizzati nella linea o nel dispositivo telefonico.

Anche se esiste anche una classe di dispositivi "wave" per i dispositivi audio wave di basso livello, è consigliabile usare sempre la classe di dispositivi wave/out per l'output delle onde di basso livello.

Per altre informazioni sulle funzioni d'onda, vedere [**Funzioni multimediali.**](../multimedia/multimedia-functions.md)

 

 
