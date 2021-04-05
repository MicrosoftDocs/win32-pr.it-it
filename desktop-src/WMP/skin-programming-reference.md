---
title: Informazioni di riferimento sulla programmazione dell'interfaccia
description: Informazioni di riferimento sulla programmazione dell'interfaccia
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Windows Media Player, interfacce
- Windows Media Player Skin, riferimenti per la programmazione
- interfacce, riferimenti per la programmazione
- riferimento per le interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708188"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="7bb97-107">Informazioni di riferimento sulla programmazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="7bb97-107">Skin Programming Reference</span></span>

<span data-ttu-id="7bb97-108">Il riferimento per la programmazione dell'interfaccia illustra gli elementi seguenti e gli attributi, i metodi e gli eventi associati.</span><span class="sxs-lookup"><span data-stu-id="7bb97-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="7bb97-109">Gli elementi e gli attributi in questa sezione richiedono Windows Media Player 7,0 o versione successiva, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="7bb97-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="7bb97-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="7bb97-110">Element</span></span>                                                  | <span data-ttu-id="7bb97-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb97-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bb97-112">Attributi di ambiente</span><span class="sxs-lookup"><span data-stu-id="7bb97-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="7bb97-113">Attributi che si applicano a tutti gli elementi dell'interfaccia con le eccezioni indicate.</span><span class="sxs-lookup"><span data-stu-id="7bb97-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="7bb97-114">Gestori eventi di ambiente</span><span class="sxs-lookup"><span data-stu-id="7bb97-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="7bb97-115">Gestori di eventi che possono essere implementati dalla maggior parte degli elementi dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="7bb97-116">Attributi dell'evento di ambiente</span><span class="sxs-lookup"><span data-stu-id="7bb97-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="7bb97-117">Attributi che descrivono in dettaglio lo stato di Windows Media Player quando viene generato un evento.</span><span class="sxs-lookup"><span data-stu-id="7bb97-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="7bb97-118">MENU di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="7bb97-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="7bb97-119">Fornisce un modo per visualizzare il pannello di accesso rapido in un'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7bb97-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="7bb97-120">PULSANTE</span><span class="sxs-lookup"><span data-stu-id="7bb97-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="7bb97-121">Pulsante autonomo.</span><span class="sxs-lookup"><span data-stu-id="7bb97-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="7bb97-122">BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="7bb97-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="7bb97-123">Pulsante all'interno di un gruppo di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="7bb97-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="7bb97-124">BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="7bb97-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="7bb97-125">Gruppo di elementi Button.</span><span class="sxs-lookup"><span data-stu-id="7bb97-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="7bb97-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="7bb97-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="7bb97-127">Rappresenta una colonna all'interno di un controllo playlist.</span><span class="sxs-lookup"><span data-stu-id="7bb97-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="7bb97-128">CONTROLLI</span><span class="sxs-lookup"><span data-stu-id="7bb97-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="7bb97-129">Fornisce l'accesso all'oggetto [Controls](controls-object.md) dall'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="7bb97-130">CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="7bb97-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="7bb97-131">Controllo dispositivo di scorrimento personalizzabile.</span><span class="sxs-lookup"><span data-stu-id="7bb97-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="7bb97-132">CASELLA</span><span class="sxs-lookup"><span data-stu-id="7bb97-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="7bb97-133">Fornisce agli utenti un modo per immettere il testo all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="7bb97-134">EFFETTI</span><span class="sxs-lookup"><span data-stu-id="7bb97-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="7bb97-135">Elemento che contiene e controlla una raccolta di effetti.</span><span class="sxs-lookup"><span data-stu-id="7bb97-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="7bb97-136">EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="7bb97-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="7bb97-137">Elemento che consente la manipolazione dell'equalizzatore grafico.</span><span class="sxs-lookup"><span data-stu-id="7bb97-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="7bb97-138">ELEMENTO</span><span class="sxs-lookup"><span data-stu-id="7bb97-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="7bb97-139">Rappresenta un elemento in una casella di riepilogo o un controllo popup.</span><span class="sxs-lookup"><span data-stu-id="7bb97-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="7bb97-140">LISTBOX</span><span class="sxs-lookup"><span data-stu-id="7bb97-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="7bb97-141">Consente agli utenti di selezionare gli elementi da un elenco.</span><span class="sxs-lookup"><span data-stu-id="7bb97-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="7bb97-142">PLAYER</span><span class="sxs-lookup"><span data-stu-id="7bb97-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="7bb97-143">Consente di accedere all'oggetto [Player](player-object.md) dall'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="7bb97-144">PLAYLIST</span><span class="sxs-lookup"><span data-stu-id="7bb97-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="7bb97-145">Elemento per il controllo dell'aspetto di una playlist all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="7bb97-146">POPUP</span><span class="sxs-lookup"><span data-stu-id="7bb97-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="7bb97-147">Consente agli utenti di selezionare gli elementi da un elenco.</span><span class="sxs-lookup"><span data-stu-id="7bb97-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="7bb97-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="7bb97-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="7bb97-149">Fornisce un modo per visualizzare le informazioni sullo stato di avanzamento in un controllo orizzontale o verticale.</span><span class="sxs-lookup"><span data-stu-id="7bb97-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="7bb97-150">IMPOSTAZIONI</span><span class="sxs-lookup"><span data-stu-id="7bb97-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="7bb97-151">Consente di accedere all'oggetto [Settings](settings-object.md) dall'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="7bb97-152">CURSORE</span><span class="sxs-lookup"><span data-stu-id="7bb97-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="7bb97-153">Controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7bb97-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="7bb97-154">VISUALIZZAZIONE secondaria</span><span class="sxs-lookup"><span data-stu-id="7bb97-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="7bb97-155">Sottosezioni all'interno di una vista che può essere spostata o nascosta.</span><span class="sxs-lookup"><span data-stu-id="7bb97-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="7bb97-156">TESTO</span><span class="sxs-lookup"><span data-stu-id="7bb97-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="7bb97-157">Controllo contenente il testo.</span><span class="sxs-lookup"><span data-stu-id="7bb97-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="7bb97-158">TEMA</span><span class="sxs-lookup"><span data-stu-id="7bb97-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="7bb97-159">Elemento principale che identifica un file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bb97-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="7bb97-160">VIDEO</span><span class="sxs-lookup"><span data-stu-id="7bb97-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="7bb97-161">Elemento per specificare l'aspetto di una finestra video.</span><span class="sxs-lookup"><span data-stu-id="7bb97-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="7bb97-162">VIDEOSETTINGS</span><span class="sxs-lookup"><span data-stu-id="7bb97-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="7bb97-163">Elemento che consente il controllo di varie impostazioni video.</span><span class="sxs-lookup"><span data-stu-id="7bb97-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="7bb97-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="7bb97-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="7bb97-165">Specifica l'aspetto dell'interfaccia utente per ogni categoria di supporti.</span><span class="sxs-lookup"><span data-stu-id="7bb97-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="7bb97-166">Varie</span><span class="sxs-lookup"><span data-stu-id="7bb97-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="7bb97-167">Attributi specializzati e altri argomenti vari da usare per la creazione di interfacce.</span><span class="sxs-lookup"><span data-stu-id="7bb97-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="7bb97-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7bb97-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb97-169">**Interfacce di Media Player Windows**</span><span class="sxs-lookup"><span data-stu-id="7bb97-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




