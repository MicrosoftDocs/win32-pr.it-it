---
title: Esecuzione di query sui dispositivi di input Waveform-Audio
description: Esecuzione di query sui dispositivi di input Waveform-Audio
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio Waveform, esecuzione di query sui dispositivi di input
- waveform-interfaccia audio, esecuzione di query sui dispositivi di input
- registrazione audio Waveform, esecuzione di query sui dispositivi di input
- esecuzione di query su dispositivi di input audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963021"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="4a295-107">Esecuzione di query sui dispositivi di input Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="4a295-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="4a295-108">Prima di registrare l'audio della forma d'onda, è necessario chiamare la funzione [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) per determinare le funzionalità di input dell'audio e della forma d'onda del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a295-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="4a295-109">Questa funzione riempie una struttura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con informazioni sulle funzionalità di un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="4a295-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="4a295-110">Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a295-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="4a295-111">Inoltre, la struttura **WAVEINCAPS** fornisce informazioni sui formati audio e di forma d'onda standard supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a295-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a295-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a295-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a295-113">Registrazione dell'audio della forma d'onda</span><span class="sxs-lookup"><span data-stu-id="4a295-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 