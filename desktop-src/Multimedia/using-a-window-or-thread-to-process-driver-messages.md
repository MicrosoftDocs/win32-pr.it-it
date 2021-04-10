---
title: Uso di una finestra o di un thread per elaborare i messaggi dei driver
description: Uso di una finestra o di un thread per elaborare i messaggi dei driver
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio Waveform, callback finestra
- blocchi di dati audio, callback della finestra
- audio Waveform, callback di thread
- blocchi di dati audio, callback di thread
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- waveInOpen (funzione)
- waveOutOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963077"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="7672a-112">Uso di una finestra o di un thread per elaborare i messaggi dei driver</span><span class="sxs-lookup"><span data-stu-id="7672a-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="7672a-113">Per usare una funzione di callback della finestra, specificare il \_ flag della finestra di callback nel parametro *fdwOpen* e un handle di finestra nella parola di ordine inferiore del parametro *dwCallback* della funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="7672a-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="7672a-114">I messaggi del driver verranno inviati alla routine della finestra per la finestra identificata dall'handle in *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="7672a-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="7672a-115">Analogamente, per usare un callback del thread, specificare \_ il thread di callback e un handle di thread nella chiamata a **waveInOpen** o **waveOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="7672a-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="7672a-116">In questo caso, i messaggi vengono inviati al thread specificato anziché a una finestra.</span><span class="sxs-lookup"><span data-stu-id="7672a-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="7672a-117">I messaggi inviati al callback della finestra o del thread sono specifici del tipo di dispositivo audio usato.</span><span class="sxs-lookup"><span data-stu-id="7672a-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="7672a-118">Per ulteriori informazioni su questi messaggi, vedere la pagina relativa alla [riproduzione di file di Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="7672a-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 