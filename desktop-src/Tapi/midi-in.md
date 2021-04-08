---
description: La classe del dispositivo MIDI/in è costituita da sequencer MIDI usati per l'input. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749538"
---
# <a name="midiin"></a><span data-ttu-id="2fc70-104">MIDI/in</span><span class="sxs-lookup"><span data-stu-id="2fc70-104">midi/in</span></span>

<span data-ttu-id="2fc70-105">La classe del dispositivo MIDI/in è costituita da sequencer MIDI usati per l'input.</span><span class="sxs-lookup"><span data-stu-id="2fc70-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="2fc70-106">Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2fc70-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2fc70-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="2fc70-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="2fc70-108">Il membro **DeviceID** è l'identificatore di un dispositivo MIDI chiuso.</span><span class="sxs-lookup"><span data-stu-id="2fc70-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="2fc70-109">Questo identificatore viene usato in una chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) per aprire il dispositivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="2fc70-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="2fc70-110">È possibile usare l'handle del dispositivo risultante per registrare i dati MIDI dalla linea o dal dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="2fc70-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="2fc70-111">Per altre informazioni sulle funzioni MIDI, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2fc70-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
