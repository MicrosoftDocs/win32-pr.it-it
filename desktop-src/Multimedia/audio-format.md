---
title: Formato audio
description: Formato audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- Messaggio WM_CAP_GET_AUDIOFORMAT
- capGetAudioFormat (macro)
- capGetAudioFormatSize (macro)
- Messaggio WM_CAP_SET_AUDIOFORMAT
- capSetAudioFormat (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872374"
---
# <a name="audio-format"></a><span data-ttu-id="27bee-108">Formato audio</span><span class="sxs-lookup"><span data-stu-id="27bee-108">Audio Format</span></span>

<span data-ttu-id="27bee-109">È possibile recuperare il formato di acquisizione corrente per i dati audio o le dimensioni della struttura del formato audio inviando il messaggio [**WM \_ Cap \_ get \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (o le macro [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="27bee-109">You can retrieve the current capture format for audio data or the size of the audio format structure by sending the [**WM\_CAP\_GET\_AUDIOFORMAT**](wm-cap-get-audioformat.md) message (or the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros) to a capture window.</span></span> <span data-ttu-id="27bee-110">Il formato di acquisizione audio predefinito è mono, a 8 bit, a 11 kHz PCM (Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="27bee-110">The default audio capture format is mono, 8-bit, 11 kHz PCM (Pulse Code Modulation).</span></span> <span data-ttu-id="27bee-111">Quando si recupera il formato usando WM \_ Cap \_ get \_ AUDIOFORMAT, usare sempre la struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="27bee-111">When you retrieve the format by using WM\_CAP\_GET\_AUDIOFORMAT, always use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure.</span></span>

<span data-ttu-id="27bee-112">È possibile impostare il formato di acquisizione per i dati audio inviando il messaggio [**WM \_ \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (o la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="27bee-112">You can set the capture format for audio data by sending the [**WM\_CAP\_SET\_AUDIOFORMAT**](wm-cap-set-audioformat.md) message (or the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro) to a capture window.</span></span> <span data-ttu-id="27bee-113">Quando si imposta il formato audio, è possibile passare un puntatore a una struttura [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX** o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , a seconda del formato audio specificato.</span><span class="sxs-lookup"><span data-stu-id="27bee-113">When setting the audio format, you can pass a pointer to a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX**, or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure, depending on the specified audio format.</span></span>

 

 