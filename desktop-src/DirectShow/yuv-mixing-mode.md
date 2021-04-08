---
description: Modalità di combinazione YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modalità di combinazione YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884129"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="f7fda-103">Modalità di combinazione YUV</span><span class="sxs-lookup"><span data-stu-id="f7fda-103">YUV Mixing Mode</span></span>

<span data-ttu-id="f7fda-104">Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f7fda-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="f7fda-105">A partire da Windows XP Service Pack 2, VMR supporta una modalità di combinazione denominata YUV mixing mode.</span><span class="sxs-lookup"><span data-stu-id="f7fda-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="f7fda-106">Questa modalità è particolarmente utile per le applicazioni TV o DVD avanzate.</span><span class="sxs-lookup"><span data-stu-id="f7fda-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="f7fda-107">Si tratta di una parte della potenza del mixer VMR per ottenere prestazioni migliori su hardware grafico di fascia bassa che usa una struttura di architettura di memoria unificata.</span><span class="sxs-lookup"><span data-stu-id="f7fda-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="f7fda-108">La modalità di combinazione YUV è supportata sia in VMR-7 che in VMR-9.</span><span class="sxs-lookup"><span data-stu-id="f7fda-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="f7fda-109">**Vantaggi**</span><span class="sxs-lookup"><span data-stu-id="f7fda-109">**Advantages**</span></span>

<span data-ttu-id="f7fda-110">La modalità di combinazione YUV presenta diversi vantaggi relativi alle prestazioni di rendering rispetto alla modalità di combinazione RGB originale supportata da VMR:</span><span class="sxs-lookup"><span data-stu-id="f7fda-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="f7fda-111">Quando VMR è in modalità di combinazione YUV, tutte le operazioni di deinterlacciamento e composizione del flusso video vengono eseguite nello spazio dei colori YUV.</span><span class="sxs-lookup"><span data-stu-id="f7fda-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="f7fda-112">Le superfici YUV richiedono in genere da 50% a 60% di larghezza di banda di memoria inferiore rispetto alle superfici RGB equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f7fda-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="f7fda-113">Il deinterlacciamento e la composizione del flusso vengono eseguiti da una singola chiamata al driver Graphics.</span><span class="sxs-lookup"><span data-stu-id="f7fda-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="f7fda-114">Il driver può usare le funzionalità di multitexturing dell'hardware grafico, con conseguente risparmio di larghezza di banda della memoria.</span><span class="sxs-lookup"><span data-stu-id="f7fda-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="f7fda-115">Sebbene qualsiasi applicazione video possa usare la modalità di combinazione YUV, è destinata principalmente a due tipi di applicazione di riproduzione video:</span><span class="sxs-lookup"><span data-stu-id="f7fda-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="f7fda-116">Applicazioni TV che visualizzano le didascalie o il televideo chiuso.</span><span class="sxs-lookup"><span data-stu-id="f7fda-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="f7fda-117">Le applicazioni DVD visualizzano i dati delle sottoimmagini DVD o i sottotitoli chiusi.</span><span class="sxs-lookup"><span data-stu-id="f7fda-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="f7fda-118">**Restrizioni**</span><span class="sxs-lookup"><span data-stu-id="f7fda-118">**Restrictions**</span></span>

<span data-ttu-id="f7fda-119">Una serie di restrizioni viene applicata da VMR quando viene inserita in modalità di combinazione YUV:</span><span class="sxs-lookup"><span data-stu-id="f7fda-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="f7fda-120">Il flusso 0 (il flusso connesso al pin di input 0) può essere progressivo o interlacciato; tutti gli altri flussi devono essere progressivi.</span><span class="sxs-lookup"><span data-stu-id="f7fda-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="f7fda-121">GUID \_ null (modalità di trama) non consentito per il flusso 0.</span><span class="sxs-lookup"><span data-stu-id="f7fda-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="f7fda-122">\_Non è possibile usare DeinterlacePref Weave come modalità di fallback perché questo potrebbe impedire la creazione di un dispositivo di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="f7fda-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="f7fda-123">La modalità di combinazione YUV richiede un dispositivo deinterlacciato anche se il video in arrivo non è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="f7fda-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="f7fda-124">Non è possibile apportare modifiche al valore alfa planare associato a ogni flusso di input di VMR.</span><span class="sxs-lookup"><span data-stu-id="f7fda-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="f7fda-125">L'utente non può modificare l'ordine Z dei flussi video connessi.</span><span class="sxs-lookup"><span data-stu-id="f7fda-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="f7fda-126">L'ordine Z predefinito viene ricavato dall'ordine del PIN.</span><span class="sxs-lookup"><span data-stu-id="f7fda-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="f7fda-127">La chiave di colore non è supportata.</span><span class="sxs-lookup"><span data-stu-id="f7fda-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="f7fda-128">Il pin di input 0 deve ricevere il flusso video.</span><span class="sxs-lookup"><span data-stu-id="f7fda-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="f7fda-129">Gli altri pin di input possono ricevere solo i dati del sottoflusso video, ad esempio l'immagine secondaria del DVD, i sottotitoli o il televideo.</span><span class="sxs-lookup"><span data-stu-id="f7fda-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="f7fda-130">Gli altri pin di input possono accettare solo formati YUV alfanumerici per pixel, ad esempio AYUV, AI44 e IA44.</span><span class="sxs-lookup"><span data-stu-id="f7fda-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="f7fda-131">Nessuno dei pin di input di VMR può accettare qualsiasi formato RGB.</span><span class="sxs-lookup"><span data-stu-id="f7fda-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="f7fda-132">Le immagini bitmap fornite dall'applicazione non possono più essere combinate con il video prima della presentazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7fda-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="f7fda-133">I singoli flussi secondari non possono essere invertiti orizzontalmente o verticalmente usando le funzioni del mixer "output Rectangle" di VMR.</span><span class="sxs-lookup"><span data-stu-id="f7fda-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="f7fda-134">Sono supportati il riposizionamento e il ridimensionamento del flusso "normale".</span><span class="sxs-lookup"><span data-stu-id="f7fda-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="f7fda-135">Il colore di sfondo di combinazione (specificato da [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) è ancora specificato nello spazio colore RGB, come in modalità di combinazione RGB.</span><span class="sxs-lookup"><span data-stu-id="f7fda-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="f7fda-136">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="f7fda-136">**Configuration**</span></span>

<span data-ttu-id="f7fda-137">Le applicazioni devono configurare in modo esplicito VMR per sfruttare i vantaggi della modalità di combinazione YUV; la modalità di combinazione RGB originale rimane quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="f7fda-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="f7fda-138">Per abilitare la modalità di combinazione YUV in VMR-7, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il \_ flag MixerPref RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="f7fda-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="f7fda-139">Questa chiamata deve essere eseguita prima della connessione di uno dei pin di input di VMR.</span><span class="sxs-lookup"><span data-stu-id="f7fda-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="f7fda-140">Per abilitare la modalità di combinazione YUV in VMR-9, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag MixerPref9 RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="f7fda-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="f7fda-141">L'unico modo per determinare se VMR-7 supporta la nuova modalità di combinazione YUV è provare a impostare VMR in tale modalità.</span><span class="sxs-lookup"><span data-stu-id="f7fda-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="f7fda-142">Se la chiamata ha esito positivo, è comunque possibile riportare il VMR in modalità di combinazione RGB, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f7fda-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="f7fda-143">Dopo aver impostato la modalità di combinazione YUV, il VMR può essere modificato di nuovo in modalità di combinazione RGB solo dopo la disconnessione di tutti i pin di input.</span><span class="sxs-lookup"><span data-stu-id="f7fda-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="f7fda-144">In modalità di combinazione YUV è possibile ridurre il carico sull'unità di elaborazione grafica (GPU) applicando i flag seguenti nel metodo **SetMixingPrefs** :</span><span class="sxs-lookup"><span data-stu-id="f7fda-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="f7fda-145">Flag</span><span class="sxs-lookup"><span data-stu-id="f7fda-145">Flag</span></span>                                                                                 | <span data-ttu-id="f7fda-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7fda-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f7fda-147">VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB</span><span class="sxs-lookup"><span data-stu-id="f7fda-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="f7fda-148">Passa a Bob deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="f7fda-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="f7fda-149">VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="f7fda-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="f7fda-150">Decimare l'immagine di un fattore 2 orizzontalmente e verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f7fda-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="f7fda-151">È possibile aggiungere o rimuovere questi flag mentre è in esecuzione il grafico dei filtri; la modifica viene applicata quando il mixer VMR compone il frame video successivo.</span><span class="sxs-lookup"><span data-stu-id="f7fda-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="f7fda-152">I flag non si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f7fda-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="f7fda-153">Queste impostazioni riducono la qualità dell'immagine, quindi in genere si applicano solo quando la qualità del video è meno importante, ad esempio se il video viene riprodotto in una piccola parte dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f7fda-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7fda-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7fda-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7fda-155">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="f7fda-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




