---
title: Determinazione del supporto del formato non standard
description: Determinazione del supporto del formato non standard
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- audio Waveform, supporto del formato non standard
- audio ausiliario, supporto del formato non standard
- audio Waveform, supporto del formato standard
- audio ausiliario, supporto del formato standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046656"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="21c33-107">Determinazione del supporto del formato non standard</span><span class="sxs-lookup"><span data-stu-id="21c33-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="21c33-108">Per verificare se un dispositivo supporta un particolare formato (standard o non standard), è possibile chiamare la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con il \_ flag di query del formato Wave \_ .</span><span class="sxs-lookup"><span data-stu-id="21c33-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="21c33-109">L'esempio seguente usa questa tecnica per determinare se un dispositivo waveform-audio supporta un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="21c33-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



<span data-ttu-id="21c33-110">Questa tecnica per determinare il supporto del formato non standard si applica anche ai dispositivi di input audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="21c33-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="21c33-111">L'unica differenza è che la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) viene usata al posto di [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per eseguire una query per il supporto del formato.</span><span class="sxs-lookup"><span data-stu-id="21c33-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="21c33-112">Per determinare se un particolare formato di dati della forma d'onda-audio è supportato da uno qualsiasi dei dispositivi audio della forma d'onda in un sistema, usare la tecnica illustrata nell'esempio precedente, ma specificare la \_ costante di mapper wave per il parametro *uDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="21c33-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 