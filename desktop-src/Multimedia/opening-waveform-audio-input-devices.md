---
title: Apertura di dispositivi di input Waveform-Audio
description: Apertura di dispositivi di input Waveform-Audio
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio Waveform, apertura di dispositivi di input
- waveform-interfaccia audio, apertura di dispositivi di input
- registrazione audio della forma d'onda, apertura di dispositivi di input
- apertura della forma d'onda-dispositivi di input audio
- waveInOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299676"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="28220-108">Apertura di dispositivi di input Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="28220-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="28220-109">Usare la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire un dispositivo di input della forma d'onda-audio per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="28220-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="28220-110">Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle di una posizione di memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="28220-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="28220-111">Alcuni computer multimediali hanno più dispositivi di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="28220-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="28220-112">A meno che non si sia certi di voler aprire un dispositivo di input della forma d'onda specifico in un sistema, è necessario usare la \_ costante di mapper wave per l'identificatore del dispositivo quando si apre un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28220-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="28220-113">La funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) sceglierà il dispositivo nel sistema più idoneo per la registrazione nel formato dati specificato.</span><span class="sxs-lookup"><span data-stu-id="28220-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28220-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28220-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28220-115">Registrazione dell'audio della forma d'onda</span><span class="sxs-lookup"><span data-stu-id="28220-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 