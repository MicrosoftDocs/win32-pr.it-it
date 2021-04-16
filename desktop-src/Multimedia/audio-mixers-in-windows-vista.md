---
title: Mixer audio in Windows Vista
description: Mixer audio in Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimediale, mixer audio di Windows Vista
- audio, mixer audio di Windows Vista
- mixer audio, Windows Vista
- mixer, Windows Vista
- Mixer audio di Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104560859"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="dc341-108">Mixer audio in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc341-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="dc341-109">A partire da Windows Vista, alcuni controlli mixer sono implementati nel software anziché nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="dc341-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="dc341-110">I controlli volume, ad esempio, vengono implementati mediante l'API di sessione audio di Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="dc341-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="dc341-111">Questi controlli non influiscono direttamente sulle impostazioni hardware.</span><span class="sxs-lookup"><span data-stu-id="dc341-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="dc341-112">Inoltre, sono associati a una sessione audio specifica del processo, quindi le modifiche interessano l'applicazione chiamante, ma non influiscono sulle altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dc341-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="dc341-113">Ogni dispositivo dell'endpoint audio ha un layout di mixer standard, implementato nel software.</span><span class="sxs-lookup"><span data-stu-id="dc341-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="dc341-114">Ogni endpoint di rendering audio contiene una riga di destinazione che contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc341-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="dc341-115">Controllo volume</span><span class="sxs-lookup"><span data-stu-id="dc341-115">Volume control</span></span>
    -   <span data-ttu-id="dc341-116">Disattiva controllo</span><span class="sxs-lookup"><span data-stu-id="dc341-116">Mute control</span></span>
    -   <span data-ttu-id="dc341-117">Origine riga: waveform-output audio.</span><span class="sxs-lookup"><span data-stu-id="dc341-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="dc341-118">Riga di origine: CD audio.</span><span class="sxs-lookup"><span data-stu-id="dc341-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="dc341-119">Ogni endpoint di acquisizione audio contiene una riga di destinazione che contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc341-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="dc341-120">Controllo volume</span><span class="sxs-lookup"><span data-stu-id="dc341-120">Volume control</span></span>
    -   <span data-ttu-id="dc341-121">Disattiva controllo</span><span class="sxs-lookup"><span data-stu-id="dc341-121">Mute control</span></span>
    -   <span data-ttu-id="dc341-122">Riga di origine: input audio.</span><span class="sxs-lookup"><span data-stu-id="dc341-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="dc341-123">Il tipo di componente dipende dal dispositivo di input, ad esempio un microfono.</span><span class="sxs-lookup"><span data-stu-id="dc341-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="dc341-124">Ogni riga di codice sorgente contiene un controllo del volume e un controllo di silenziamento.</span><span class="sxs-lookup"><span data-stu-id="dc341-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="dc341-125">Il diagramma seguente illustra i componenti degli endpoint di rendering e degli endpoint di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dc341-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![layout mixer predefiniti](images/mixer1.gif)

<span data-ttu-id="dc341-127">Tutti i controlli per un endpoint modificano lo stesso controllo software sottostante.</span><span class="sxs-lookup"><span data-stu-id="dc341-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="dc341-128">Se pertanto si modificano le impostazioni in un controllo, si riceverà una notifica di modifica del controllo sugli altri controlli.</span><span class="sxs-lookup"><span data-stu-id="dc341-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="dc341-129">(Vedere la pagina relativa alla [**\_ \_ \_ modifica del controllo MIXM mm**](mm-mixm-control-change.md)).</span><span class="sxs-lookup"><span data-stu-id="dc341-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="dc341-130">Questo layout standard viene fornito per la compatibilità con le applicazioni esistenti che usano le funzioni del mixer audio.</span><span class="sxs-lookup"><span data-stu-id="dc341-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="dc341-131">Le nuove applicazioni devono evitare di usare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="dc341-131">New applications should avoid using these functions.</span></span>

 

 




