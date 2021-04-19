---
title: Proprietà frequenza IWMPSettings
description: La proprietà rate Ottiene o imposta la frequenza di riproduzione corrente per i video.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Media Player delle proprietà della frequenza
- Proprietà rate Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325963"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="d7506-106">Proprietà IWMPSettings:: rate</span><span class="sxs-lookup"><span data-stu-id="d7506-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="d7506-107">La proprietà **rate** Ottiene o imposta la frequenza di riproduzione corrente per i video.</span><span class="sxs-lookup"><span data-stu-id="d7506-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7506-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7506-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="d7506-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d7506-109">Property value</span></span>

<span data-ttu-id="d7506-110">**System. Double** che corrisponde alla frequenza di riproduzione, con un valore predefinito di 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7506-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7506-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7506-111">Remarks</span></span>

<span data-ttu-id="d7506-112">Il valore recuperato da questa proprietà funge da valore moltiplicatore che consente di riprodurre un elemento multimediale a una velocità più veloce o più lenta.</span><span class="sxs-lookup"><span data-stu-id="d7506-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="d7506-113">Il valore predefinito 1,0 indica la velocità creata.</span><span class="sxs-lookup"><span data-stu-id="d7506-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="d7506-114">Si noti che una traccia audio diventa difficile da comprendere a una velocità inferiore a 0,5 o superiore a 1,5.</span><span class="sxs-lookup"><span data-stu-id="d7506-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="d7506-115">La velocità di riproduzione 2 indica il doppio della velocità di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="d7506-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="d7506-116">Windows Media Player tenterà di utilizzare le quattro diverse modalità di riproduzione più efficaci delle seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7506-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="d7506-117">Riproduzione video uniforme con il pitch audio mantenuto</span><span class="sxs-lookup"><span data-stu-id="d7506-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="d7506-118">Riproduzione video smussata con pitch audio non mantenuto</span><span class="sxs-lookup"><span data-stu-id="d7506-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="d7506-119">Riproduzione video senza audio</span><span class="sxs-lookup"><span data-stu-id="d7506-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="d7506-120">Riproduzione video del fotogramma chiave senza audio</span><span class="sxs-lookup"><span data-stu-id="d7506-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="d7506-121">La modalità scelta da Windows Media Player dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.</span><span class="sxs-lookup"><span data-stu-id="d7506-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="d7506-122">Si applicano anche altre considerazioni, a seconda del formato multimediale digitale usato per creare il contenuto:</span><span class="sxs-lookup"><span data-stu-id="d7506-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="d7506-123">**Windows Media Video (WMV) e ASF.**</span><span class="sxs-lookup"><span data-stu-id="d7506-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="d7506-124">I valori ottimali per la proprietà **rate** sono compresi tra 1 e 10 o da 1 a 10 per la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="d7506-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="d7506-125">Anche i valori compresi tra 0,5 e 1,0 o da-0,5 a-1,0 possono funzionare correttamente nei casi in cui è possibile mantenere il pitch audio, ad esempio quando si giocano file che si trovano nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d7506-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="d7506-126">I valori con una grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.</span><span class="sxs-lookup"><span data-stu-id="d7506-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="d7506-127">**Altri formati video.**</span><span class="sxs-lookup"><span data-stu-id="d7506-127">**Other video formats.**</span></span> <span data-ttu-id="d7506-128">La proprietà **rate** può variare da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="d7506-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="d7506-129">I valori negativi non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="d7506-129">Negative values are not allowed.</span></span> <span data-ttu-id="d7506-130">I valori minori di 1 rappresentano un movimento lento.</span><span class="sxs-lookup"><span data-stu-id="d7506-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="d7506-131">I valori superiori a 9 sono consentiti, ma non sono molto significativi.</span><span class="sxs-lookup"><span data-stu-id="d7506-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="d7506-132">Il metodo **IWMPControls. fastForward** modifica il valore di **rate** su 5,0, mentre il metodo **IWMPControls. fastReverse** modifica il valore di **rate** in 5,0.</span><span class="sxs-lookup"><span data-stu-id="d7506-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="d7506-133">Non è possibile modificare la velocità di riproduzione di alcuni formati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="d7506-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="d7506-134">Usare la proprietà **IWMPSettings.** IsValid (in C# il metodo **IWMPSettings. Get \_ unavailable** ) per individuare se questa proprietà può essere specificata per un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d7506-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="d7506-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="d7506-135">Examples</span></span>

<span data-ttu-id="d7506-136">Nell'esempio seguente viene usato un controllo a discesa numerico che consente all'utente di modificare la velocità di riproduzione del supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="d7506-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="d7506-137">Quando l'utente fa clic sulle frecce verso l'alto o verso il basso del controllo, la proprietà **rate** viene impostata sul nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="d7506-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="d7506-138">Il possibile intervallo di valori nel controllo è 0,5 (metà velocità) a 2,0 (doppia velocità).</span><span class="sxs-lookup"><span data-stu-id="d7506-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="d7506-139">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="d7506-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d7506-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7506-140">Requirements</span></span>



| <span data-ttu-id="d7506-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7506-141">Requirement</span></span> | <span data-ttu-id="d7506-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d7506-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7506-143">Versione</span><span class="sxs-lookup"><span data-stu-id="d7506-143">Version</span></span><br/>   | <span data-ttu-id="d7506-144">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d7506-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d7506-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d7506-145">Namespace</span></span><br/> | <span data-ttu-id="d7506-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d7506-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d7506-147">Assembly</span><span class="sxs-lookup"><span data-stu-id="d7506-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d7506-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d7506-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7506-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7506-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7506-150">**IWMPControls. fastForward (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7506-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7506-151">**IWMPControls. fastReverse (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7506-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7506-152">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7506-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7506-153">**IWMPSettings. disavailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7506-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d7506-154">**IWMPSettings. mute (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7506-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





