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
# <a name="waveinout"></a><span data-ttu-id="6c1a9-103">Wave/in/out</span><span class="sxs-lookup"><span data-stu-id="6c1a9-103">wave/in/out</span></span>

<span data-ttu-id="6c1a9-104">La classe del dispositivo wave/in/out è costituita da dispositivi audio duplex completi.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-104">The wave/in/out device class consists of full duplex audio devices.</span></span> <span data-ttu-id="6c1a9-105">Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="6c1a9-106">I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="6c1a9-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo due membri aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="6c1a9-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending two additional members:</span></span>

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

<span data-ttu-id="6c1a9-108">I membri **DeviceInId** e **DeviceOutId** sono identificatori di un dispositivo audio chiuso.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-108">The **DeviceInId** and **DeviceOutId** members are identifiers of a closed audio device.</span></span> <span data-ttu-id="6c1a9-109">Questi identificatori vengono usati in una chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire il dispositivo per l'output.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-109">You use these identifiers in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="6c1a9-110">È possibile usare l'handle del dispositivo risultante per riprodurre dati audio digitalizzati sulla linea o sul dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="6c1a9-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="6c1a9-111">Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6c1a9-111">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
