---
title: Player. uiMode
description: La proprietà uiMode specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode Windows Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327063"
---
# <a name="playeruimode"></a><span data-ttu-id="da398-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="da398-104">Player.uiMode</span></span>

<span data-ttu-id="da398-105">La proprietà **uiMode** specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="da398-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="da398-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da398-106">Syntax</span></span>

<span data-ttu-id="da398-107">*Player* . **uiMode**</span><span class="sxs-lookup"><span data-stu-id="da398-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="da398-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="da398-108">Possible Values</span></span>

<span data-ttu-id="da398-109">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="da398-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="da398-110">Valore</span><span class="sxs-lookup"><span data-stu-id="da398-110">Value</span></span>     | <span data-ttu-id="da398-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da398-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="da398-112">Esempio di audio</span><span class="sxs-lookup"><span data-stu-id="da398-112">Audio Example</span></span>                                          | <span data-ttu-id="da398-113">Esempio video</span><span class="sxs-lookup"><span data-stu-id="da398-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="da398-114">invisibile</span><span class="sxs-lookup"><span data-stu-id="da398-114">invisible</span></span> | <span data-ttu-id="da398-115">Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).</span><span class="sxs-lookup"><span data-stu-id="da398-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="da398-116">Non viene visualizzato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="da398-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="da398-117">Non viene visualizzato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="da398-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="da398-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da398-118">none</span></span>      | <span data-ttu-id="da398-119">Windows Media Player viene incorporato senza controlli e con solo la finestra video o visualizzazione visualizzata.</span><span class="sxs-lookup"><span data-stu-id="da398-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | !["None" con audio](images/uimode-none-audio-v11.png) | !["None" con video](images/uimode-none-video-v11.png) |
| <span data-ttu-id="da398-122">minima</span><span class="sxs-lookup"><span data-stu-id="da398-122">mini</span></span>      | <span data-ttu-id="da398-123">Windows Media Player è incorporato con la finestra di stato, i controlli di riproduzione, sospensione, arresto, silenziamento e volume visualizzati oltre alla finestra video o visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="da398-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con video](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="da398-126">completi</span><span class="sxs-lookup"><span data-stu-id="da398-126">full</span></span>      | <span data-ttu-id="da398-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="da398-127">Default.</span></span> <span data-ttu-id="da398-128">Windows Media Player viene incorporato con la finestra di stato, la barra di ricerca, i controlli di riproduzione, pausa, arresto, silenziamento, avanti, precedente, avanzamento rapido, Reverse veloce e volume, oltre alla finestra visualizzazione o video.</span><span class="sxs-lookup"><span data-stu-id="da398-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | !["completo" con audio](images/uimode-full-audio-v11.png) | !["completo" con video](images/uimode-full-video-v11.png) |
| <span data-ttu-id="da398-131">custom</span><span class="sxs-lookup"><span data-stu-id="da398-131">custom</span></span>    | <span data-ttu-id="da398-132">Windows Media Player è incorporato con un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="da398-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="da398-133">Può essere usato solo nei programmi C++.</span><span class="sxs-lookup"><span data-stu-id="da398-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="da398-134">Viene visualizzata l'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="da398-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="da398-135">Viene visualizzata l'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="da398-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="da398-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="da398-136">Remarks</span></span>

<span data-ttu-id="da398-137">Questa proprietà specifica l'aspetto della Media Player Windows incorporata.</span><span class="sxs-lookup"><span data-stu-id="da398-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="da398-138">Quando **uiMode** è impostato su "None", "mini" o "full", per la visualizzazione di clip video e visualizzazioni audio è presente una finestra.</span><span class="sxs-lookup"><span data-stu-id="da398-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="da398-139">Questa finestra può essere nascosta in modalità mini o full impostando l'attributo **Height** del tag **Object** su 40, che viene misurato dalla parte inferiore e lascia visibile la parte Controls dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="da398-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="da398-140">Se non si desidera alcuna interfaccia incorporata, impostare gli attributi **Width** e **Height** su zero.</span><span class="sxs-lookup"><span data-stu-id="da398-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="da398-141">Se **uiMode** è impostato su "invisibile", non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato in **larghezza** e **altezza**.</span><span class="sxs-lookup"><span data-stu-id="da398-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="da398-142">Questa operazione è utile per mantenere il layout di pagina quando è possibile modificare **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="da398-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="da398-143">Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.</span><span class="sxs-lookup"><span data-stu-id="da398-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="da398-144">Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="da398-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="da398-145">Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="da398-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="da398-146">Se la finestra è visibile e il contenuto audio viene riprodotto, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="da398-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="da398-147">Se **uiMode** è impostato su "Custom" in un programma C++ che implementa **IWMPRemoteMediaServices**, viene visualizzato il file dell'interfaccia indicato da **IWMPRemoteMediaServices:: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="da398-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="da398-148">Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".</span><span class="sxs-lookup"><span data-stu-id="da398-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="da398-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="da398-149">Examples</span></span>

<span data-ttu-id="da398-150">Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare l'interfaccia utente per un oggetto **Player** incorporato.</span><span class="sxs-lookup"><span data-stu-id="da398-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="da398-151">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="da398-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="da398-152">Windows Media Player 10 Mobile: questa proprietà accetta o restituisce solo i valori "None" o "full".</span><span class="sxs-lookup"><span data-stu-id="da398-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="da398-153">Nei dispositivi smartphone vengono visualizzati solo lo stato della riproduzione e un contatore quando *uiMode* è impostato su "full".</span><span class="sxs-lookup"><span data-stu-id="da398-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="da398-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da398-154">Requirements</span></span>



| <span data-ttu-id="da398-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="da398-155">Requirement</span></span> | <span data-ttu-id="da398-156">Valore</span><span class="sxs-lookup"><span data-stu-id="da398-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da398-157">Versione</span><span class="sxs-lookup"><span data-stu-id="da398-157">Version</span></span><br/> | <span data-ttu-id="da398-158">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="da398-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="da398-159">Windows Media Player 9 Series o versione successiva per "invisibile" o "personalizzato".</span><span class="sxs-lookup"><span data-stu-id="da398-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="da398-160">DLL</span><span class="sxs-lookup"><span data-stu-id="da398-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="da398-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da398-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="da398-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da398-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da398-163">**Interfaccia IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="da398-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="da398-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span><span class="sxs-lookup"><span data-stu-id="da398-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="da398-165">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="da398-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





