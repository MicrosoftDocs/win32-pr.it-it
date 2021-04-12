---
title: Plug-in di Windows Media Player DSP
description: Plug-in di Windows Media Player DSP
ms.assetid: 1c7202c4-ca66-491d-9a5f-26032cad1dcc
keywords:
- Windows Media Player, plug-in
- Windows Media Player, plug-in DSP
- Plug-in di Windows Media Player, elaborazione dei segnali digitali (DSP)
- plug-in, elaborazione di segnali digitali (DSP)
- plug-in per l'elaborazione di segnali digitali, informazioni
- Plug-in DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755088bce89530350997d2f543e30872f630e882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471446"
---
# <a name="windows-media-player-dsp-plug-ins"></a><span data-ttu-id="ca989-109">Plug-in di Windows Media Player DSP</span><span class="sxs-lookup"><span data-stu-id="ca989-109">Windows Media Player DSP Plug-ins</span></span>

<span data-ttu-id="ca989-110">Microsoft Windows Media Player offre un'architettura che consente all'utente di installare e attivare programmi plug-in che aggiungono la funzionalità di elaborazione dei segnali digitali (DSP).</span><span class="sxs-lookup"><span data-stu-id="ca989-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add digital signal processing (DSP) functionality.</span></span> <span data-ttu-id="ca989-111">Un plug-in DSP è un Microsoft DirectX Media Object (DMO) o una trasformazione Media Foundation (MFT) che si connette al lettore usando le interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="ca989-111">A DSP plug-in is a Microsoft DirectX Media Object (DMO) or a Media Foundation Transform (MFT) that connects to the Player by using COM interfaces.</span></span> <span data-ttu-id="ca989-112">Un plug-in standard di DSP potrebbe essere un equalizzatore audio o un controllo di tinta video.</span><span class="sxs-lookup"><span data-stu-id="ca989-112">A typical DSP plug-in might be an audio equalizer or a video tint control.</span></span> <span data-ttu-id="ca989-113">Questa sezione dell'SDK fornisce le informazioni di programmazione necessarie per creare un plug-in DSP personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ca989-113">This section of the SDK provides the programming information you need to create your own DSP plug-in.</span></span>

<span data-ttu-id="ca989-114">La documentazione del plug-in DSP è divisa nelle tre sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca989-114">The DSP plug-in documentation is divided into the following three sections.</span></span>



| <span data-ttu-id="ca989-115">Sezione</span><span class="sxs-lookup"><span data-stu-id="ca989-115">Section</span></span>                                                                      | <span data-ttu-id="ca989-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca989-116">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca989-117">Informazioni sui plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="ca989-117">About DSP Plug-ins</span></span>](about-dsp-plug-ins.md)                                 | <span data-ttu-id="ca989-118">Viene fornita una panoramica dell'architettura utilizzata per i plug-in DSP. Leggere questa sezione per informazioni sui concetti generali relativi a questa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="ca989-118">Provides an overview of the architecture used for DSP plug-ins. Read this section to learn the general concepts involved with this technology.</span></span>  |
| [<span data-ttu-id="ca989-119">Guida alla programmazione di plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="ca989-119">DSP Plug-ins Programming Guide</span></span>](dsp-plug-ins-programming-guide.md)         | <span data-ttu-id="ca989-120">Vengono illustrate le operazioni necessarie per creare un plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="ca989-120">Explains what you need to do to create a DSP plug-in.</span></span> <span data-ttu-id="ca989-121">In questa sezione sono contenuti esempi di codice e procedure dettagliate.</span><span class="sxs-lookup"><span data-stu-id="ca989-121">This section contains example code and step-by-step procedures.</span></span>                           |
| [<span data-ttu-id="ca989-122">Guida di riferimento alla programmazione di plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="ca989-122">DSP Plug-ins Programming Reference</span></span>](dsp-plug-ins-programming-reference.md) | <span data-ttu-id="ca989-123">Fornisce un riferimento dettagliato per le interfacce COM, i metodi e i tipi enumerati supportati dai plug-in di Windows Media Player SDK per DSP.</span><span class="sxs-lookup"><span data-stu-id="ca989-123">Provides a detailed reference for the COM interfaces, methods, and enumerated types supported by the Windows Media Player SDK for DSP plug-ins.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ca989-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca989-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca989-125">**Plug-in di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="ca989-125">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




