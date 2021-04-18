---
title: Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
description: L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato. | Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328309"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f2fee-105">Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f2fee-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f2fee-106">L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="f2fee-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="f2fee-107">Event Data</span></span>

<span data-ttu-id="f2fee-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_ScriptCommandEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="f2fee-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="f2fee-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="f2fee-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f2fee-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2fee-110">Property</span></span> | <span data-ttu-id="f2fee-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2fee-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="f2fee-112">scType</span><span class="sxs-lookup"><span data-stu-id="f2fee-112">scType</span></span>   | <span data-ttu-id="f2fee-113">System. StringSpecifies il tipo di comando per script.</span><span class="sxs-lookup"><span data-stu-id="f2fee-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="f2fee-114">param</span><span class="sxs-lookup"><span data-stu-id="f2fee-114">param</span></span>    | <span data-ttu-id="f2fee-115">System. StringSpecifies il comando script.</span><span class="sxs-lookup"><span data-stu-id="f2fee-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="f2fee-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2fee-116">Remarks</span></span>

<span data-ttu-id="f2fee-117">I comandi possono essere incorporati tra i suoni e le immagini di un file o di un flusso Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f2fee-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="f2fee-118">I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso.</span><span class="sxs-lookup"><span data-stu-id="f2fee-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="f2fee-119">Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un evento **ScriptCommand** con due parametri.</span><span class="sxs-lookup"><span data-stu-id="f2fee-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="f2fee-120">Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando.</span><span class="sxs-lookup"><span data-stu-id="f2fee-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="f2fee-121">Il tipo di parametro viene utilizzato per determinare la modalità di elaborazione del parametro del comando.</span><span class="sxs-lookup"><span data-stu-id="f2fee-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="f2fee-122">Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito dall'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="f2fee-123">Nella tabella seguente sono elencati i tipi di comando script elaborati automaticamente da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f2fee-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="f2fee-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2fee-124">Type</span></span>                   | <span data-ttu-id="f2fee-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2fee-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fee-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="f2fee-126">CAPTION</span></span>                | <span data-ttu-id="f2fee-127">Il controllo Visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="f2fee-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="f2fee-128">EVENTO</span><span class="sxs-lookup"><span data-stu-id="f2fee-128">EVENT</span></span>                  | <span data-ttu-id="f2fee-129">Il controllo esegue le istruzioni definite per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="f2fee-130">FILENAME</span><span class="sxs-lookup"><span data-stu-id="f2fee-130">FILENAME</span></span>               | <span data-ttu-id="f2fee-131">Il controllo Reimposta la proprietà **URL** , tenta di aprire il file specificato e inizia immediatamente a riprodurre il nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="f2fee-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="f2fee-132">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="f2fee-132">OPENEVENT</span></span>              | <span data-ttu-id="f2fee-133">Memorizza nel buffer il comando del tipo di evento associato per l'esecuzione tempestiva dello script di evento.</span><span class="sxs-lookup"><span data-stu-id="f2fee-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="f2fee-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="f2fee-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="f2fee-135">Il parametro *param* contiene il testo lirico sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="f2fee-136">Windows Media Player Visualizza il testo lirico nell'area didascalia chiusa della funzionalità **ora di riproduzione** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="f2fee-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="f2fee-137">TEXT</span></span>                   | <span data-ttu-id="f2fee-138">Il controllo Visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="f2fee-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="f2fee-139">URL</span><span class="sxs-lookup"><span data-stu-id="f2fee-139">URL</span></span>                    | <span data-ttu-id="f2fee-140">Il controllo apre automaticamente l'URL specificato utilizzando il browser Internet predefinito, se IWMPSettings. la proprietà **invokeURLs** è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f2fee-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="f2fee-141">È possibile incorporare qualsiasi altro tipo di comando purché si fornisca il codice per gestire il comando.</span><span class="sxs-lookup"><span data-stu-id="f2fee-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="f2fee-142">Sebbene i comandi sconosciuti vengano ignorati dal controllo Media Player di Windows, vengono comunque passati all'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="f2fee-143">L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione in modalità avanzamento rapido o riavvolgimento.</span><span class="sxs-lookup"><span data-stu-id="f2fee-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="f2fee-144">I comandi dell'URL ricevuti dal controllo Media Player di Windows vengono richiamati automaticamente nel Web browser predefinito, se IWMPSettings. la proprietà **invokeURLs** è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f2fee-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="f2fee-145">È possibile usare IWMPSettings. proprietà **DefaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="f2fee-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="f2fee-146">L'URL inviato a Windows Media Player viene elaborato in relazione all'URL di base specificato da IWMPSettings. proprietà **BaseUrl** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="f2fee-147">L'URL di base viene concatenato all'URL relativo, ottenendo un URL completo che viene passato come parametro Command dall'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="f2fee-148">Il controllo Media Player Windows elabora sempre i comandi URL in arrivo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f2fee-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="f2fee-149">Viene ricevuto un comando di tipo URL.</span><span class="sxs-lookup"><span data-stu-id="f2fee-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="f2fee-150">IWMPSettings. **BaseUrl** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.</span><span class="sxs-lookup"><span data-stu-id="f2fee-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="f2fee-151">Viene chiamato **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="f2fee-152">Dopo la restituzione di **ScriptCommand** , IWMPSettings. **invokeURLs** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="f2fee-153">Se IWMPSettings. **invokeURLs** è true e il comando è un comando URL, viene richiamato l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="f2fee-154">Se IWMPSettings. **invokeURLs** è false o se il comando non è un comando URL, il comando viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f2fee-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="f2fee-155">Quando si crea un file di Windows Media, è possibile specificare il frame in cui viene visualizzato il nuovo URL concatenando due e commerciali e il nome del frame nel campo del parametro.</span><span class="sxs-lookup"><span data-stu-id="f2fee-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="f2fee-156">Nell'esempio seguente vengono illustrati i tipici parametri **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f2fee-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="f2fee-157">Specifica che è necessario avviare la *pagina* URL *nel frame frame* .</span><span class="sxs-lookup"><span data-stu-id="f2fee-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="f2fee-158">L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione (con avanzamento rapido o riavvolto).</span><span class="sxs-lookup"><span data-stu-id="f2fee-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fee-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2fee-159">Requirements</span></span>



| <span data-ttu-id="f2fee-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2fee-160">Requirement</span></span> | <span data-ttu-id="f2fee-161">Valore</span><span class="sxs-lookup"><span data-stu-id="f2fee-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fee-162">Versione</span><span class="sxs-lookup"><span data-stu-id="f2fee-162">Version</span></span><br/>   | <span data-ttu-id="f2fee-163">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f2fee-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f2fee-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2fee-164">Namespace</span></span><br/> | <span data-ttu-id="f2fee-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f2fee-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f2fee-166">Assembly</span><span class="sxs-lookup"><span data-stu-id="f2fee-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f2fee-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f2fee-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2fee-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2fee-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fee-169">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fee-170">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fee-171">**IWMPClosedCaption. captioningId (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fee-172">**IWMPSettings. baseURL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fee-173">**IWMPSettings. defaultFrame (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fee-174">**IWMPSettings. invokeURLs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fee-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





