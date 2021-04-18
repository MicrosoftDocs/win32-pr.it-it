---
title: Opzioni del plug-in dell'interfaccia utente
description: Opzioni del plug-in dell'interfaccia utente
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Plug-in di Windows Media Player, opzioni
- plug-in, opzioni
- plug-in dell'interfaccia utente, opzioni
- Plug-in dell'interfaccia utente, opzioni
- plug-in area impostazioni
- plug-in in background
- plug-in di finestra distinti
- plug-in dell'area dei metadati
- plug-in area di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297931"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="011f8-112">Opzioni del plug-in dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="011f8-112">UI Plug-in Options</span></span>

<span data-ttu-id="011f8-113">Uno dei cinque tipi di plug-in dell'interfaccia utente può avere una pagina delle proprietà in cui l'utente può modificare le impostazioni del plug-in.</span><span class="sxs-lookup"><span data-stu-id="011f8-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="011f8-114">Questa pagina delle proprietà può essere impostata in modo da essere visualizzata automaticamente quando un plug-in viene caricato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="011f8-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="011f8-115">È anche possibile accedervi dalla scheda plug-in della finestra di dialogo Opzioni.</span><span class="sxs-lookup"><span data-stu-id="011f8-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="011f8-116">Un plug-in dell'interfaccia utente può essere impostato per il caricamento automatico dopo l'installazione quando viene avviato Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="011f8-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="011f8-117">Se non viene avviato automaticamente, l'utente può caricarlo selezionandola dall'elenco dei **plug-** in nel menu **strumenti** .</span><span class="sxs-lookup"><span data-stu-id="011f8-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="011f8-118">Un plug-in dell'area di visualizzazione può avere più set di impostazioni, ovvero visualizzazioni diverse che il plug-in può rendere disponibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="011f8-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="011f8-119">L'utente può modificare il set di impostazioni selezionando una voce diversa dall'elenco visualizzazioni **e visualizzazioni** del menu **Visualizza** oppure usando i pulsanti freccia disponibili nella parte inferiore del riquadro **Now Play** appena sopra il messaggio di stato e i controlli di trasporto.</span><span class="sxs-lookup"><span data-stu-id="011f8-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="011f8-120">I plug-in background e separati dell'interfaccia utente della finestra possono essere programmati per accettare un elemento multimediale o una playlist inviata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="011f8-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="011f8-121">Se un plug-in supporta questa funzionalità, il relativo nome verrà visualizzato nell'elenco **Invia a** disponibile dal menu di scelta rapida del controllo playlist o della libreria.</span><span class="sxs-lookup"><span data-stu-id="011f8-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="011f8-122">Un plug-in dell'interfaccia utente può essere programmato per intercettare i tasti di scelta rapida quando dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="011f8-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="011f8-123">Lo stato attivo della tastiera è necessario per evitare conflitti quando vengono caricati più plug-in dell'interfaccia utente che intercettano lo stesso tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="011f8-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="011f8-124">Sebbene questo impedisca conflitti, può anche causare confusione agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="011f8-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="011f8-125">Per questo motivo, non è consigliabile usare i tasti di scelta rapida con i plug-in dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="011f8-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="011f8-126">Quando vengono usati, tuttavia, non devono intercettare alcun tasto di scelta rapida utilizzato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="011f8-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="011f8-127">Per un elenco completo dei tasti di scelta rapida usati dal lettore, vedere la Guida di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="011f8-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="011f8-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="011f8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="011f8-129">**Panoramica del plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="011f8-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




