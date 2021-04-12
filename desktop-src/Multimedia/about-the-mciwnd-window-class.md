---
title: Informazioni sulla classe della finestra MCIWnd
description: Informazioni sulla classe della finestra MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Classe della finestra MCIWnd, informazioni
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396070"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="9fcc9-105">Informazioni sulla classe della finestra MCIWnd</span><span class="sxs-lookup"><span data-stu-id="9fcc9-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="9fcc9-106">La classe della finestra MCIWnd è facile da usare.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="9fcc9-107">Con una singola funzione, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) l'applicazione può creare un controllo che riproduce qualsiasi dispositivo che usa l'interfaccia di controllo multimediale (MCI).</span><span class="sxs-lookup"><span data-stu-id="9fcc9-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="9fcc9-108">Questi dispositivi includono CD audio, Waveform-Audio, MIDI e dispositivi video.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="9fcc9-109">L'automazione della riproduzione è anche rapida e semplice.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="9fcc9-110">Usando solo una funzione e due macro, un'applicazione può creare una finestra MCIWnd con il dispositivo multimediale appropriato, riprodurre il dispositivo e chiudere sia il dispositivo che la finestra al termine della riproduzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="9fcc9-111">Alcuni dispositivi riproducono contenuto archiviato in file.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="9fcc9-112">Altri dispositivi, ad esempio i dispositivi audio CD, riproducono contenuto archiviato in un altro supporto.</span><span class="sxs-lookup"><span data-stu-id="9fcc9-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="9fcc9-113">Per motivi di chiarezza, questa panoramica si riferisce a entrambe le circostanze come "riproduzione del dispositivo".</span><span class="sxs-lookup"><span data-stu-id="9fcc9-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




