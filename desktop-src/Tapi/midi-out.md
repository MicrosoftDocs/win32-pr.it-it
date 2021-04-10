---
description: La classe del dispositivo MIDI/out è costituita da sequencer MIDI usati per l'output. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225863"
---
# <a name="midiout"></a><span data-ttu-id="e400e-104">MIDI/out</span><span class="sxs-lookup"><span data-stu-id="e400e-104">midi/out</span></span>

<span data-ttu-id="e400e-105">La classe del dispositivo MIDI/out è costituita da sequencer MIDI usati per l'output.</span><span class="sxs-lookup"><span data-stu-id="e400e-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="e400e-106">Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e400e-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="e400e-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="e400e-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="e400e-108">Il membro **DeviceID** è l'identificatore di un dispositivo MIDI chiuso.</span><span class="sxs-lookup"><span data-stu-id="e400e-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="e400e-109">Questo identificatore viene usato in una chiamata alla funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) per aprire il dispositivo per l'output.</span><span class="sxs-lookup"><span data-stu-id="e400e-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="e400e-110">È possibile usare l'handle del dispositivo risultante per riprodurre dati MIDI alla riga o al dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="e400e-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="e400e-111">Per altre informazioni sulle funzioni MIDI, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e400e-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
