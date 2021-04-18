---
title: Evento Player. ScriptCommand
description: L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato. | Evento Player. ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Media Player di Windows Event ScriptCommand
- Windows Event ScriptCommand Media Player, classe Player
- Classe Player Windows Media Player, evento ScriptCommand
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333922"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="87579-107">Evento Player. ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="87579-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="87579-108">L'evento **ScriptCommand** si verifica quando viene ricevuto un comando o un URL sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="87579-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="87579-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87579-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="87579-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="87579-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87579-111">*scType*</span><span class="sxs-lookup"><span data-stu-id="87579-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="87579-112">Stringa che specifica il tipo di comando di script.</span><span class="sxs-lookup"><span data-stu-id="87579-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="87579-113">*Param*</span><span class="sxs-lookup"><span data-stu-id="87579-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="87579-114">**Stringa** che specifica il comando script.</span><span class="sxs-lookup"><span data-stu-id="87579-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87579-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87579-115">Return value</span></span>

<span data-ttu-id="87579-116">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="87579-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87579-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="87579-117">Remarks</span></span>

<span data-ttu-id="87579-118">I comandi possono essere incorporati tra i suoni e le immagini di un file o di un flusso Windows Media.</span><span class="sxs-lookup"><span data-stu-id="87579-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="87579-119">I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso.</span><span class="sxs-lookup"><span data-stu-id="87579-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="87579-120">Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un evento **ScriptCommand** con due parametri.</span><span class="sxs-lookup"><span data-stu-id="87579-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="87579-121">Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando.</span><span class="sxs-lookup"><span data-stu-id="87579-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="87579-122">Il tipo di parametro viene utilizzato per determinare la modalità di elaborazione del parametro del comando.</span><span class="sxs-lookup"><span data-stu-id="87579-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="87579-123">Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito dall'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="87579-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="87579-124">Nella tabella seguente sono elencati i tipi di comando script elaborati automaticamente da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="87579-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="87579-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="87579-125">Type</span></span>                   | <span data-ttu-id="87579-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87579-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87579-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="87579-127">CAPTION</span></span>                | <span data-ttu-id="87579-128">Il controllo Visualizza il testo associato nell'elemento DIV specificato da *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="87579-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="87579-129">EVENTO</span><span class="sxs-lookup"><span data-stu-id="87579-129">EVENT</span></span>                  | <span data-ttu-id="87579-130">Indica al controllo di eseguire le istruzioni definite per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="87579-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="87579-131">FILENAME</span><span class="sxs-lookup"><span data-stu-id="87579-131">FILENAME</span></span>               | <span data-ttu-id="87579-132">Il controllo Reimposta la proprietà **URL** , tenta di aprire il file specificato e inizia immediatamente a riprodurre il nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="87579-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="87579-133">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="87579-133">OPENEVENT</span></span>              | <span data-ttu-id="87579-134">Memorizza nel buffer il comando del tipo di evento associato per l'esecuzione tempestiva dello script di evento.</span><span class="sxs-lookup"><span data-stu-id="87579-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="87579-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="87579-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="87579-136">Il parametro *param* contiene il testo lirico sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="87579-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="87579-137">Windows Media Player Visualizza il testo lirico nell'area didascalia chiusa della funzionalità **ora di riproduzione** .</span><span class="sxs-lookup"><span data-stu-id="87579-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="87579-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="87579-138">TEXT</span></span>                   | <span data-ttu-id="87579-139">Il controllo Visualizza il testo associato nell'elemento DIV specificato da *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="87579-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="87579-140">URL</span><span class="sxs-lookup"><span data-stu-id="87579-140">URL</span></span>                    | <span data-ttu-id="87579-141">Il controllo apre automaticamente l'URL specificato utilizzando il browser Internet predefinito se le *Impostazioni*. la proprietà **invokeURLs** è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="87579-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="87579-142">È possibile incorporare qualsiasi altro tipo di comando purché si fornisca codice reciproco per gestire il comando.</span><span class="sxs-lookup"><span data-stu-id="87579-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="87579-143">Sebbene i comandi sconosciuti vengano ignorati dal controllo Media Player di Windows, vengono comunque passati all'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="87579-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="87579-144">I comandi URL ricevuti dal controllo Media Player Windows vengono richiamati automaticamente nel Web browser predefinito se le *Impostazioni*. la proprietà **invokeURLs** è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="87579-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="87579-145">È possibile utilizzare le *Impostazioni*. proprietà **DefaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="87579-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="87579-146">L'URL inviato a Windows Media Player viene elaborato in relazione all'URL di base specificato dalle *Impostazioni*. proprietà **BaseUrl** .</span><span class="sxs-lookup"><span data-stu-id="87579-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="87579-147">L'URL di base è concatenato all'URL relativamente specificato, ottenendo un URL completo che viene passato come parametro Command dall'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="87579-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="87579-148">Il controllo Media Player Windows elabora sempre i comandi di tipo URL in arrivo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="87579-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="87579-149">Viene ricevuto un comando di tipo URL.</span><span class="sxs-lookup"><span data-stu-id="87579-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="87579-150">*Impostazioni*. **BaseUrl** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.</span><span class="sxs-lookup"><span data-stu-id="87579-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="87579-151">Viene chiamato *ScriptCommand* .</span><span class="sxs-lookup"><span data-stu-id="87579-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="87579-152">Dopo che *ScriptCommand* restituisce, *Settings*. **invokeURLs** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="87579-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="87579-153">Se *le impostazioni*. **invokeURLs** è true e il comando è di tipo URL, viene richiamato l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="87579-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="87579-154">Se *le impostazioni*. **invokeURLs** è false o se il comando non è di tipo URL, il comando viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="87579-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="87579-155">Quando si crea un file di Windows Media, è possibile specificare il frame in cui viene visualizzato il nuovo URL concatenando due e commerciali e il nome del frame nel campo del parametro.</span><span class="sxs-lookup"><span data-stu-id="87579-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="87579-156">Nell'esempio seguente vengono illustrati i tipici parametri *ScriptCommand* .</span><span class="sxs-lookup"><span data-stu-id="87579-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="87579-157">Specifica che è necessario avviare la *pagina* URL *nel frame frame* .</span><span class="sxs-lookup"><span data-stu-id="87579-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="87579-158">L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione (veloce o invertito).</span><span class="sxs-lookup"><span data-stu-id="87579-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="87579-159">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="87579-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="87579-160">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="87579-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="87579-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87579-161">Requirements</span></span>



| <span data-ttu-id="87579-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="87579-162">Requirement</span></span> | <span data-ttu-id="87579-163">Valore</span><span class="sxs-lookup"><span data-stu-id="87579-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87579-164">Versione</span><span class="sxs-lookup"><span data-stu-id="87579-164">Version</span></span><br/> | <span data-ttu-id="87579-165">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="87579-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="87579-166">DLL</span><span class="sxs-lookup"><span data-stu-id="87579-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="87579-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87579-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87579-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87579-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87579-169">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="87579-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="87579-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="87579-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="87579-171">**Settings. baseURL**</span><span class="sxs-lookup"><span data-stu-id="87579-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="87579-172">**Settings. defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="87579-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="87579-173">**Settings. invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="87579-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





