---
title: Avvio, sospensione e ripresa della riproduzione
description: Avvio, sospensione e ripresa della riproduzione
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay (macro)
- MCIWndPause (macro)
- MCIWndResume (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222058"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="dfa12-106">Avvio, sospensione e ripresa della riproduzione</span><span class="sxs-lookup"><span data-stu-id="dfa12-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="dfa12-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) è la macro di riproduzione più generale.</span><span class="sxs-lookup"><span data-stu-id="dfa12-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="dfa12-108">Questa macro consente di riprodurre un file o un dispositivo dalla posizione di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfa12-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="dfa12-109">La riproduzione continua fino alla fine del contenuto a meno che non venga interrotta.</span><span class="sxs-lookup"><span data-stu-id="dfa12-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="dfa12-110">È possibile interrompere temporaneamente un dispositivo che sta eseguendo usando la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="dfa12-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="dfa12-111">Per riprendere la riproduzione dalla posizione sospesa, usare la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="dfa12-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="dfa12-112">Alcuni dispositivi non supportano i comandi Sospendi e Riprendi.</span><span class="sxs-lookup"><span data-stu-id="dfa12-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="dfa12-113">Questi dispositivi in genere mappano **MCIWndPause** alla macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , che interrompe la riproduzione o la registrazione.</span><span class="sxs-lookup"><span data-stu-id="dfa12-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="dfa12-114">È possibile riavviare un dispositivo che non supporta la sospensione o la ripresa usando **MCIWndPlay**, che avvia la riproduzione dalla posizione di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfa12-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




