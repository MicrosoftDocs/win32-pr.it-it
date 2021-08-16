---
description: La classe di dispositivi wave/in è costituita da dispositivi audio per l'input audio wave di basso livello.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002529"
---
# <a name="wavein"></a>wave/in

La classe di dispositivi wave/in è costituita da dispositivi audio per l'input audio wave di basso livello. È possibile accedere a questi dispositivi usando le funzioni d'onda, descritte in Platform Software Development Kit (SDK). I dispositivi in questa classe sono associati a dispositivi line che supportano il tipo di supporto LINEMEDIAMODE AUTOMATEDVOICE, specificato nel membro \_ **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo line.

Le [**funzioni lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempiono una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Il **membro DeviceId** è l'identificatore di un dispositivo audio chiuso. Questo identificatore viene utilizzato in una chiamata alla [**funzione waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire il dispositivo per l'input. È possibile usare l'handle del dispositivo risultante per registrare i dati audio digitalizzati dal dispositivo linea o telefono.

Anche se esiste una classe di dispositivi "wave" anche per i dispositivi audio wave di basso livello, è consigliabile usare sempre la classe di dispositivi wave/in per l'input delle onde di basso livello.

Per altre informazioni sulle funzioni d'onda, vedere [**Funzioni multimediali.**](../multimedia/multimedia-functions.md)

 

 
