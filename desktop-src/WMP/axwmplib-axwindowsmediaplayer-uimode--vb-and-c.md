---
title: Proprietà AxWindowsMediaPlayer. uiMode
description: La proprietà uiMode Ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Finestra delle proprietà di uiMode Media Player
- Proprietà uiMode Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330899"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="bcab2-106">Proprietà AxWindowsMediaPlayer. uiMode</span><span class="sxs-lookup"><span data-stu-id="bcab2-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="bcab2-107">La proprietà uiMode Ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bcab2-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcab2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcab2-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="bcab2-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bcab2-109">Property value</span></span>

<span data-ttu-id="bcab2-110">System. String che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bcab2-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="bcab2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="bcab2-111">Value</span></span>     | <span data-ttu-id="bcab2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcab2-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="bcab2-113">Esempio di audio</span><span class="sxs-lookup"><span data-stu-id="bcab2-113">Audio example</span></span>                                                   | <span data-ttu-id="bcab2-114">Esempio video</span><span class="sxs-lookup"><span data-stu-id="bcab2-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bcab2-115">invisibile</span><span class="sxs-lookup"><span data-stu-id="bcab2-115">invisible</span></span> | <span data-ttu-id="bcab2-116">Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).</span><span class="sxs-lookup"><span data-stu-id="bcab2-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="bcab2-117">Non viene visualizzato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="bcab2-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="bcab2-118">Non viene visualizzato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="bcab2-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="bcab2-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bcab2-119">none</span></span>      | <span data-ttu-id="bcab2-120">Windows Media Player viene incorporato senza controlli e con solo la finestra video o visualizzazione visualizzata.</span><span class="sxs-lookup"><span data-stu-id="bcab2-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![uiMode =' none ' con audio](images/uimode-none-audio-v11.png) | ![uiMode =' none ' con video](images/uimode-none-video-v11.png) |
| <span data-ttu-id="bcab2-123">minima</span><span class="sxs-lookup"><span data-stu-id="bcab2-123">mini</span></span>      | <span data-ttu-id="bcab2-124">Windows Media Player è incorporato con la finestra di stato, i controlli di riproduzione, sospensione, arresto, silenziamento e volume visualizzati oltre alla finestra video o visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bcab2-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![uiMode =' mini ' con audio](images/uimode-mini-audio-v11.png) | ![uiMode =' mini ' con video](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="bcab2-127">completi</span><span class="sxs-lookup"><span data-stu-id="bcab2-127">full</span></span>      | <span data-ttu-id="bcab2-128">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bcab2-128">Default.</span></span> <span data-ttu-id="bcab2-129">Windows Media Player viene incorporato con la finestra di stato, la barra di ricerca, i controlli di riproduzione, pausa, arresto, silenziamento, avanti, precedente, avanzamento rapido, Rewind e volume oltre alla finestra video o visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bcab2-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![uiMode =' Full ' con audio](images/uimode-full-audio-v11.png) | ![uiMode =' Full ' con video](images/uimode-full-video-v11.png) |
| <span data-ttu-id="bcab2-132">custom</span><span class="sxs-lookup"><span data-stu-id="bcab2-132">custom</span></span>    | <span data-ttu-id="bcab2-133">Windows Media Player è incorporato con un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bcab2-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="bcab2-134">Può essere usato solo nei programmi C++.</span><span class="sxs-lookup"><span data-stu-id="bcab2-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="bcab2-135">Viene visualizzata l'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bcab2-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="bcab2-136">Viene visualizzata l'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bcab2-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="bcab2-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcab2-137">Remarks</span></span>

<span data-ttu-id="bcab2-138">Questa proprietà specifica l'aspetto della Media Player Windows incorporata.</span><span class="sxs-lookup"><span data-stu-id="bcab2-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="bcab2-139">Quando **uiMode** è impostato su "None", "mini" o "full", per la visualizzazione di clip video e visualizzazioni audio è presente una finestra.</span><span class="sxs-lookup"><span data-stu-id="bcab2-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="bcab2-140">Questa finestra può essere nascosta in modalità mini o full impostando l'attributo **Height** del tag **Object** su 40, che viene misurato dalla parte inferiore e lascia visibile la parte Controls dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bcab2-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="bcab2-141">Se non si desidera alcuna interfaccia incorporata, impostare gli attributi **Width** e **Height** su zero.</span><span class="sxs-lookup"><span data-stu-id="bcab2-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="bcab2-142">Se **uiMode** è impostato su "invisibile", non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato in **larghezza** e **altezza**.</span><span class="sxs-lookup"><span data-stu-id="bcab2-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="bcab2-143">Questa operazione è utile per mantenere il layout di pagina quando è possibile modificare **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="bcab2-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="bcab2-144">Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.</span><span class="sxs-lookup"><span data-stu-id="bcab2-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="bcab2-145">Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bcab2-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="bcab2-146">Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bcab2-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="bcab2-147">Se la finestra è visibile e il contenuto audio viene riprodotto, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bcab2-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="bcab2-148">Se **uiMode** è impostato su "Custom" in un programma C++ che implementa **IWMPRemoteMediaServices**, viene visualizzato il file dell'interfaccia indicato da **IWMPRemoteMediaServices. GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="bcab2-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="bcab2-149">Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".</span><span class="sxs-lookup"><span data-stu-id="bcab2-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="bcab2-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="bcab2-150">Examples</span></span>

<span data-ttu-id="bcab2-151">Nell'esempio seguente viene creata una casella di riepilogo che consente all'utente di modificare la modalità di interfaccia utente per un oggetto Windows Media Player incorporato.</span><span class="sxs-lookup"><span data-stu-id="bcab2-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="bcab2-152">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="bcab2-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bcab2-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcab2-153">Requirements</span></span>



| <span data-ttu-id="bcab2-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcab2-154">Requirement</span></span> | <span data-ttu-id="bcab2-155">Valore</span><span class="sxs-lookup"><span data-stu-id="bcab2-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcab2-156">Versione</span><span class="sxs-lookup"><span data-stu-id="bcab2-156">Version</span></span><br/>   | <span data-ttu-id="bcab2-157">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="bcab2-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="bcab2-158">Windows Media Player 9 Series o versione successiva per "invisibile" o "personalizzato"</span><span class="sxs-lookup"><span data-stu-id="bcab2-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="bcab2-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcab2-159">Namespace</span></span><br/> | <span data-ttu-id="bcab2-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="bcab2-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bcab2-161">Assembly</span><span class="sxs-lookup"><span data-stu-id="bcab2-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bcab2-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bcab2-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcab2-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcab2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcab2-164">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bcab2-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bcab2-165">**AxWindowsMediaPlayer. enableContextMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bcab2-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





