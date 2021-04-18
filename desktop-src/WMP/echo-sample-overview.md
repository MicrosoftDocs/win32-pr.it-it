---
title: Panoramica dell'esempio Echo
description: Panoramica dell'esempio Echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-in di Windows Media Player, panoramica dell'esempio Echo
- plug-in, Panoramica di esempio Echo
- plug-in di elaborazione dei segnali digitali, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298558"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="a4e9f-108">Panoramica dell'esempio Echo</span><span class="sxs-lookup"><span data-stu-id="a4e9f-108">Echo Sample Overview</span></span>

<span data-ttu-id="a4e9f-109">Questa guida compila un plug-in Windows Media Player DSP che crea un effetto eco nell'audio PCM durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="a4e9f-110">Gli obiettivi per il plug-in sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4e9f-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="a4e9f-111">Il plug-in elabora solo l'audio PCM a 8 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="a4e9f-112">Supporta un tempo di ritardo compreso tra 10 millisecondi (MS) e 2000 ms (2 secondi).</span><span class="sxs-lookup"><span data-stu-id="a4e9f-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="a4e9f-113">Rappresenta un intervallo pratico per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="a4e9f-114">Supporta la combinazione del segnale originale con il segnale di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="a4e9f-115">Fornisce un'implementazione della pagina delle proprietà che consente all'utente di fornire un valore per il tempo di ritardo e un valore per la percentuale del segnale di ritardo rispetto al livello di segnale audio complessivo.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="a4e9f-116">Il codice viene creato modificando l'esempio di plug-in di Windows Media Player Wizard audio DSP.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="a4e9f-117">L'esempio Echo non è incluso in Windows Media Player SDK. si tratta di un esempio creato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="a4e9f-118">Per creare l'esempio Echo, è necessario iniziare con il progetto predefinito dalla procedura guidata plug-in di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="a4e9f-119">È possibile assegnare il nome desiderato al progetto. in questa documentazione si presuppone che il progetto sia denominato Echo.</span><span class="sxs-lookup"><span data-stu-id="a4e9f-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="a4e9f-120">Per informazioni dettagliate sull'uso della procedura guidata, vedere [compilazione di un plug-in DSP](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="a4e9f-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="a4e9f-121">Nella sezione seguente viene fornita una panoramica del modo in cui l'esempio crea un effetto eco:</span><span class="sxs-lookup"><span data-stu-id="a4e9f-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="a4e9f-122">Funzionamento del campione Echo</span><span class="sxs-lookup"><span data-stu-id="a4e9f-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="a4e9f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4e9f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e9f-124">**Esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="a4e9f-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




