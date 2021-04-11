---
description: La classe del dispositivo wave/out è costituita da dispositivi audio per l'output audio Wave di basso livello.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885821"
---
# <a name="waveout"></a><span data-ttu-id="f0e3e-103">Wave/out</span><span class="sxs-lookup"><span data-stu-id="f0e3e-103">wave/out</span></span>

<span data-ttu-id="f0e3e-104">La classe del dispositivo wave/out è costituita da dispositivi audio per l'output audio Wave di basso livello.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-104">The wave/out device class consists of audio devices for low-level wave audio output.</span></span> <span data-ttu-id="f0e3e-105">Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="f0e3e-106">I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="f0e3e-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="f0e3e-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="f0e3e-108">Il membro **DeviceID** è l'identificatore di un dispositivo audio chiuso.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="f0e3e-109">Questo identificatore viene usato in una chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire il dispositivo per l'output.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-109">You use this identifier in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="f0e3e-110">È possibile usare l'handle del dispositivo risultante per riprodurre dati audio digitalizzati sulla linea o sul dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="f0e3e-111">Sebbene esista anche una classe di dispositivo "Wave" per i dispositivi audio Wave di basso livello, è consigliabile usare sempre la classe del dispositivo wave/out per l'output wave di basso livello.</span><span class="sxs-lookup"><span data-stu-id="f0e3e-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/out device class for low-level wave output.</span></span>

<span data-ttu-id="f0e3e-112">Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f0e3e-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
