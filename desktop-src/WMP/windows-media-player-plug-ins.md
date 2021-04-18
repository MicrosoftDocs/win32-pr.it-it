---
title: Plug-in di Windows Media Player
description: Plug-in di Windows Media Player
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player, plug-in
- Plug-in di Windows Media Player, informazioni
- plug-in, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300193"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="28e07-106">Plug-in di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="28e07-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="28e07-107">Microsoft Windows Media Player espone interfacce che consentono di estendere le funzionalità in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="28e07-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="28e07-108">Le sezioni seguenti descrivono le architetture di plug-in supportate e il processo di creazione di un plug-in:</span><span class="sxs-lookup"><span data-stu-id="28e07-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="28e07-109">Sezione</span><span class="sxs-lookup"><span data-stu-id="28e07-109">Section</span></span>                                                                                                         | <span data-ttu-id="28e07-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28e07-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28e07-111">Creazione di un plug-in</span><span class="sxs-lookup"><span data-stu-id="28e07-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="28e07-112">È possibile creare diversi tipi di plug-in usando Visual Studio e la creazione guidata plug-in di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="28e07-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="28e07-113">Visualizzazioni personalizzate di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="28e07-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="28e07-114">Le visualizzazioni di Windows Media Player sono oggetti Component Object Model (COM) usati per visualizzare immagini visive sincronizzate con la parte audio della riproduzione multimediale del lettore.</span><span class="sxs-lookup"><span data-stu-id="28e07-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="28e07-115">È possibile creare visualizzazioni personalizzate usando Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="28e07-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="28e07-116">Plug-in di interfaccia utente di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="28e07-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="28e07-117">I plug-in di interfaccia utente di Windows Media Player aggiungono nuove funzionalità al riquadro **Now Playing** del lettore in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="28e07-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="28e07-118">È possibile creare plug-in che usano l'area di visualizzazione, una finestra separata, l'area delle impostazioni, l'area dei metadati o plug-in in background che non espongono alcuna interfaccia utente visibile.</span><span class="sxs-lookup"><span data-stu-id="28e07-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="28e07-119">Plug-in di Windows Media Player DSP</span><span class="sxs-lookup"><span data-stu-id="28e07-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="28e07-120">I plug-in di Windows Media Player DSP modificano o elaborano i dati audio e video prima del rendering da parte del lettore.</span><span class="sxs-lookup"><span data-stu-id="28e07-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="28e07-121">I plug-in DSP sono gli oggetti DMO (DirectX Media Objects) che si connettono al lettore tramite interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="28e07-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="28e07-122">[Plug-in per il rendering di Windows Media Player (deprecato)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28e07-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="28e07-123">I plug-in per il rendering di Windows Media Player decodificano (se necessario) ed eseguono il rendering di dati personalizzati contenuti in un flusso di formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="28e07-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="28e07-124">I plug-in per il rendering sono gli oggetti DMO (DirectX Media Objects) che si connettono al lettore tramite interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="28e07-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="28e07-125">Plug-in di conversione di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="28e07-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="28e07-126">I plug-in di conversione di Windows Media Player convertono i file multimediali digitali creati usando le tecnologie non fornite da Microsoft, in formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="28e07-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="28e07-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28e07-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28e07-128">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="28e07-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 