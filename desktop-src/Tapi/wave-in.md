---
description: La classe del dispositivo wave/in è costituita da dispositivi audio per l'input audio Wave di basso livello.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233254"
---
# <a name="wavein"></a><span data-ttu-id="8a365-103">Wave/in</span><span class="sxs-lookup"><span data-stu-id="8a365-103">wave/in</span></span>

<span data-ttu-id="8a365-104">La classe del dispositivo wave/in è costituita da dispositivi audio per l'input audio Wave di basso livello.</span><span class="sxs-lookup"><span data-stu-id="8a365-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="8a365-105">Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8a365-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="8a365-106">I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="8a365-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="8a365-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="8a365-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="8a365-108">Il membro **DeviceID** è l'identificatore di un dispositivo audio chiuso.</span><span class="sxs-lookup"><span data-stu-id="8a365-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="8a365-109">Questo identificatore viene usato in una chiamata alla funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire il dispositivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="8a365-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="8a365-110">È possibile usare l'handle del dispositivo risultante per registrare i dati audio digitati dalla linea o dal dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="8a365-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="8a365-111">Sebbene esista anche una classe di dispositivo "Wave" per i dispositivi audio Wave di basso livello, è consigliabile usare sempre la classe del dispositivo wave/in per l'input wave di basso livello.</span><span class="sxs-lookup"><span data-stu-id="8a365-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="8a365-112">Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8a365-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
