---
description: La classe del dispositivo wave/in/out è costituita da dispositivi audio duplex completi.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314120"
---
# <a name="waveinout"></a>Wave/in/out

La classe del dispositivo wave/in/out è costituita da dispositivi audio duplex completi. Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma. I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo due membri aggiuntivi:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

I membri **DeviceInId** e **DeviceOutId** sono identificatori di un dispositivo audio chiuso. Questi identificatori vengono usati in una chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire il dispositivo per l'output. È possibile usare l'handle del dispositivo risultante per riprodurre dati audio digitalizzati sulla linea o sul dispositivo telefonico.

Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
