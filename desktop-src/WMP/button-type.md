---
title: Tipo di pulsante
description: Tipo di pulsante
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Interfacce di Windows Media Player Mobile, tipi di pulsanti
- interfacce, tipi di pulsanti
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855682"
---
# <a name="button-type"></a><span data-ttu-id="da0cf-107">Tipo di pulsante</span><span class="sxs-lookup"><span data-stu-id="da0cf-107">Button Type</span></span>

<span data-ttu-id="da0cf-108">I pulsanti sono disponibili in due tipi generali: località e area.</span><span class="sxs-lookup"><span data-stu-id="da0cf-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="da0cf-109">Ogni tipo generale è costituito da tre tipi specifici, rendendo tutti sei tipi di pulsante in tutti.</span><span class="sxs-lookup"><span data-stu-id="da0cf-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="da0cf-110">I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="da0cf-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="da0cf-111">Tipi di pulsante location</span><span class="sxs-lookup"><span data-stu-id="da0cf-111">Location Button Types</span></span>

<span data-ttu-id="da0cf-112">I pulsanti percorso utilizzano le coordinate per definire le rispettive posizioni rispetto allo sfondo.</span><span class="sxs-lookup"><span data-stu-id="da0cf-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="da0cf-113">La tabella seguente illustra i valori validi per i tipi di pulsante location.</span><span class="sxs-lookup"><span data-stu-id="da0cf-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="da0cf-114">Non è necessario definire i valori per i tipi che non verranno usati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="da0cf-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="da0cf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="da0cf-115">Value</span></span>  | <span data-ttu-id="da0cf-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da0cf-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0cf-117">Push</span><span class="sxs-lookup"><span data-stu-id="da0cf-117">Push</span></span>   | <span data-ttu-id="da0cf-118">Definisce un pulsante che attiva un evento una sola volta.</span><span class="sxs-lookup"><span data-stu-id="da0cf-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="da0cf-119">È necessario eseguire il push del pulsante ogni volta per attivare ulteriori eventi.</span><span class="sxs-lookup"><span data-stu-id="da0cf-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="da0cf-120">Un esempio potrebbe essere un pulsante che passa all'elemento successivo nella playlist.</span><span class="sxs-lookup"><span data-stu-id="da0cf-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="da0cf-121">Il percorso del pulsante è definito dalle relative coordinate.</span><span class="sxs-lookup"><span data-stu-id="da0cf-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="da0cf-122">Toggle</span><span class="sxs-lookup"><span data-stu-id="da0cf-122">Toggle</span></span> | <span data-ttu-id="da0cf-123">Definisce un pulsante che attiva un evento che modifica uno stato.</span><span class="sxs-lookup"><span data-stu-id="da0cf-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="da0cf-124">Lo stato rimane fino a quando non viene nuovamente premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="da0cf-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="da0cf-125">Un esempio è un pulsante che mischia la playlist.</span><span class="sxs-lookup"><span data-stu-id="da0cf-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="da0cf-126">Quando la playlist è in uno stato casuale, rimarrà casuale fino a quando non si preme di nuovo il pulsante.</span><span class="sxs-lookup"><span data-stu-id="da0cf-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="da0cf-127">Il percorso del pulsante è definito dalle relative coordinate.</span><span class="sxs-lookup"><span data-stu-id="da0cf-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="da0cf-128">2Push</span><span class="sxs-lookup"><span data-stu-id="da0cf-128">2Push</span></span>  | <span data-ttu-id="da0cf-129">Definisce un pulsante che attiva un evento, quindi passa a uno stato pronto per attivare un evento diverso.</span><span class="sxs-lookup"><span data-stu-id="da0cf-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="da0cf-130">I due stati vengono spostati ogni volta che viene premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="da0cf-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="da0cf-131">Un esempio è un pulsante che usa la funzione **come playpause** per passare dalla riproduzione alla sospensione dell'elemento multimediale corrente e viceversa.</span><span class="sxs-lookup"><span data-stu-id="da0cf-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="da0cf-132">Quando si preme il pulsante per la prima volta, viene attivato lo stato di riproduzione principale e viene visualizzata un'immagine secondaria per indicare che è possibile attivare un evento di **sospensione** .</span><span class="sxs-lookup"><span data-stu-id="da0cf-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="da0cf-133">Quando si preme di nuovo il pulsante, viene attivato lo stato di sospensione e viene visualizzata l'immagine originale per indicare che è possibile attivare un evento di **riproduzione** .</span><span class="sxs-lookup"><span data-stu-id="da0cf-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="da0cf-134">Il percorso del pulsante è definito dalle relative coordinate.</span><span class="sxs-lookup"><span data-stu-id="da0cf-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="da0cf-135">Tipi di pulsante Region</span><span class="sxs-lookup"><span data-stu-id="da0cf-135">Region Button Types</span></span>

<span data-ttu-id="da0cf-136">I pulsanti area usano aree dei colori nell'immagine dell'area per definire dove verranno elaborati i rubinetti per un pulsante specifico.</span><span class="sxs-lookup"><span data-stu-id="da0cf-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="da0cf-137">La tabella seguente illustra i valori validi per i tipi di pulsante Region.</span><span class="sxs-lookup"><span data-stu-id="da0cf-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="da0cf-138">Non è necessario definire i valori per i tipi che non verranno usati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="da0cf-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="da0cf-139">Valore</span><span class="sxs-lookup"><span data-stu-id="da0cf-139">Value</span></span>     | <span data-ttu-id="da0cf-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da0cf-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0cf-141">PushHit</span><span class="sxs-lookup"><span data-stu-id="da0cf-141">PushHit</span></span>   | <span data-ttu-id="da0cf-142">Simile al valore del pulsante di push, tranne per il fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area.</span><span class="sxs-lookup"><span data-stu-id="da0cf-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="da0cf-143">ToggleHit</span><span class="sxs-lookup"><span data-stu-id="da0cf-143">ToggleHit</span></span> | <span data-ttu-id="da0cf-144">Simile al valore dell'interruttore, ad eccezione del fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area.</span><span class="sxs-lookup"><span data-stu-id="da0cf-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="da0cf-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="da0cf-145">2PushHit</span></span>  | <span data-ttu-id="da0cf-146">Simile al valore del pulsante 2Push, tranne per il fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area.</span><span class="sxs-lookup"><span data-stu-id="da0cf-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="da0cf-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da0cf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0cf-148">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="da0cf-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




