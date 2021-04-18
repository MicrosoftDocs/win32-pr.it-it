---
title: Utilizzo di una funzione di callback per elaborare i messaggi del driver
description: Utilizzo di una funzione di callback per elaborare i messaggi del driver
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- audio Waveform, funzioni di callback
- blocchi di dati audio, funzioni di callback
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- waveInOpen (funzione)
- waveOutOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299730"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="9a9f8-110">Utilizzo di una funzione di callback per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="9a9f8-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="9a9f8-111">È possibile scrivere una funzione di callback personalizzata per elaborare i messaggi inviati dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="9a9f8-112">Per usare una funzione di callback, specificare il \_ flag della funzione di callback nel parametro *fdwOpen* e l'indirizzo del callback nel parametro *dwCallback* della funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="9a9f8-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="9a9f8-113">I messaggi inviati a una funzione di callback sono simili ai messaggi inviati a una finestra, con la differenza che hanno due parametri **DWORD** anziché **uint** e un parametro **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9a9f8-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="9a9f8-114">Per informazioni dettagliate su questi messaggi, vedere la pagina relativa alla [riproduzione di file di Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="9a9f8-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="9a9f8-115">Per passare i dati dell'istanza da un'applicazione a una funzione di callback, usare una delle tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a9f8-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="9a9f8-116">Passare i dati dell'istanza utilizzando il parametro *dwInstance* della funzione che apre il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="9a9f8-117">Passare i dati dell'istanza usando il membro **dwUser** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica un blocco di dati audio da inviare a un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="9a9f8-118">Se sono necessari più di 32 bit di dati dell'istanza, passare un puntatore a una struttura contenente le informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 