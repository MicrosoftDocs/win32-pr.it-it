---
title: Creazione di una finestra di dialogo per la selezione di un formato per il salvataggio
description: Creazione di una finestra di dialogo per la selezione di un formato per il salvataggio
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Gestione compressione audio (ACM), creazione di finestre di dialogo
- ACM (Gestione compressione audio), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- acmFormatChoose (funzione)
- Gestione compressione audio (ACM), selezione del formato per il salvataggio
- ACM (Gestione compressione audio), selezione del formato per il salvataggio
- Esempi di ACM, selezione del formato per il salvataggio
- selezione del formato per il salvataggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "104398692"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="2676d-112">Creazione di una finestra di dialogo per la selezione di un formato per il salvataggio</span><span class="sxs-lookup"><span data-stu-id="2676d-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="2676d-113">Potrebbe essere necessario che un'applicazione salvi i dati audio della forma d'onda esistenti in un altro formato.</span><span class="sxs-lookup"><span data-stu-id="2676d-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="2676d-114">Ad esempio, un editor di audio Waveform può salvare un file di forma d'onda-audio come file compresso.</span><span class="sxs-lookup"><span data-stu-id="2676d-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="2676d-115">Per elencare solo i formati di destinazione suggeriti per un formato di origine specificato nella finestra di dialogo creata dalla funzione [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , specificare il formato di origine nel membro **pwfxEnum** e il \_ flag FORMATENUMF suggest di ACM \_ nel membro **fdwEnum** della struttura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="2676d-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="2676d-116">Analogamente, per elencare i formati di destinazione validi per un formato specificato, usare il \_ flag ACM FORMATENUMF \_ Convert anziché il \_ flag ACM FORMATENUMF \_ suggest.</span><span class="sxs-lookup"><span data-stu-id="2676d-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




