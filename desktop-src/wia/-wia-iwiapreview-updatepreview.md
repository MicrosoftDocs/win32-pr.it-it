---
description: "Ottiene l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview."
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Metodo IWiaPreview:: UpdatePreview (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129418"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="54135-103">Metodo IWiaPreview:: UpdatePreview</span><span class="sxs-lookup"><span data-stu-id="54135-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="54135-104">Ottiene l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="54135-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="54135-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54135-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="54135-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54135-107">*lOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54135-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54135-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="54135-108">Type: **LONG**</span></span>

<span data-ttu-id="54135-109">Specifica se l'applicazione richiede il componente WIA 2,0 Preview per passare un'area secondaria dell'immagine memorizzata nella cache o l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="54135-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="54135-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span><span class="sxs-lookup"><span data-stu-id="54135-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="54135-111">Passa l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="54135-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="54135-112">*pChildWiaItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54135-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54135-113">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="54135-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="54135-114">Specifica un puntatore all'elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , che è un elemento figlio dell'elemento **IWiaItem2** specificato dal parametro *pWiaItem2* del metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="54135-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="54135-115">In alternativa, se l'applicazione richiede un'anteprima dell'intero piano, specifica un puntatore al parametro *pWiaItem2* del metodo **IWiaPreview:: GetNewPreview** .</span><span class="sxs-lookup"><span data-stu-id="54135-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="54135-116">Quando *pChildWiaItem* è figlio del parametro *pWiaItem2* di **IWiaPreview:: GetNewPreview**, questo elemento figlio viene in genere creato dal filtro di segmentazione.</span><span class="sxs-lookup"><span data-stu-id="54135-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54135-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54135-117">Return value</span></span>

<span data-ttu-id="54135-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="54135-118">Type: **HRESULT**</span></span>

<span data-ttu-id="54135-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="54135-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54135-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54135-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="54135-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="54135-121">Remarks</span></span>

<span data-ttu-id="54135-122">Questo metodo passa l'immagine memorizzata nella cache e non filtrata tramite il filtro di elaborazione dell'immagine, che quindi scrive i dati filtrati nel flusso fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="54135-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="54135-123">Il componente WIA 2,0 Preview recupera questo flusso chiamando il metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro di elaborazione dell'immagine, che quindi chiama l'implementazione **GetNextStream** del callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="54135-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="54135-124">Prima di chiamare **IWiaPreview:: UpdatePreview**, un'applicazione deve prima chiamare [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) per acquisire l'immagine dallo scanner; in caso contrario, il metodo restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="54135-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="54135-125">Il componente WIA 2,0 Preview archivia l'immagine non filtrata scaricata dal driver.</span><span class="sxs-lookup"><span data-stu-id="54135-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="54135-126">È possibile che l'elemento WIA 2,0 passato in **IWiaPreview:: UpdatePreview** rappresenti solo una piccola area dell'immagine scaricata dal driver.</span><span class="sxs-lookup"><span data-stu-id="54135-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="54135-127">Se questo è il caso, il componente WIA 2,0 Preview interrompe effettivamente questa area dall'immagine memorizzata nella cache prima di passarla al filtro di elaborazione dell'immagine, che a sua volta passa i dati dell'immagine filtrata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="54135-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="54135-128">Affinché un'applicazione passi l'intera immagine memorizzata nella cache al filtro di elaborazione dell'immagine, che a sua volta lo passa all'applicazione, deve impostare *lOptions* su **WiaPreviewReturnOriginalImage** quando si chiama **IWiaPreview:: UpdatePreview**.</span><span class="sxs-lookup"><span data-stu-id="54135-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="54135-129">Quando si imposta *lOptions* su **WiaPreviewReturnOriginalImage**, l'applicazione deve garantire che le impostazioni dell'extent ([**WIA \_ IPS \_ stampa**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YEXTENT**) dell'elemento passato a **IWiaPreview:: UpdatePreview** corrispondano all'immagine memorizzata nella cache completa.</span><span class="sxs-lookup"><span data-stu-id="54135-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="54135-130">Il filtro di elaborazione delle immagini non deve eseguire alcuna operazione diversa in questo caso. Filtra semplicemente l'immagine, in base alle proprietà di *pChildWiaItem* , in genere in questo caso *pChildWiaItem* è lo stesso elemento passato a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="54135-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="54135-131">Le diverse aree secondarie vengono ignorate e l'intera immagine viene filtrata utilizzando le stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="54135-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="54135-132">Ci sono due motivi per cui un'applicazione esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="54135-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="54135-133">L'applicazione potrebbe non supportare la modifica delle impostazioni, ad esempio la [**\_ \_ luminosità degli indirizzi IP**](-wia-wiaitempropscanneritem.md) WIA e il **\_ \_ contrasto degli indirizzi IP WIA**, singolarmente per ogni area rilevata dal filtro di segmentazione (oppure potrebbe non voler usare anche il filtro di segmentazione).</span><span class="sxs-lookup"><span data-stu-id="54135-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="54135-134">È più semplice per l'applicazione chiamare **IWiaPreview:: UpdatePreview** con **WiaPreviewReturnOriginalImage** in modo che riceva sempre l'immagine completa dal componente WIA 2,0 Preview.</span><span class="sxs-lookup"><span data-stu-id="54135-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="54135-135">Il componente WIA 2,0 Preview non supporta il formato di immagine dell'immagine di anteprima, nel qual caso non può eseguire le azioni per tagliare l'area desiderata.</span><span class="sxs-lookup"><span data-stu-id="54135-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="54135-136">Il supporto del formato immagine del componente WIA 2,0 Preview è limitato ai formati per i quali sono presenti codificatori e decodificatori di Windows GDI+ 1,1.</span><span class="sxs-lookup"><span data-stu-id="54135-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="54135-137">Questi formati sono bitmap (BMP) (bitmap che include BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="54135-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="54135-138">Si noti che se l'applicazione passa **WiaPreviewReturnOriginalImage** a **IWiaPreview:: UpdatePreview**, il componente di anteprima WIA 2,0 può supportare qualsiasi formato immagine o pixel.</span><span class="sxs-lookup"><span data-stu-id="54135-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="54135-139">**IWiaPreview:: UpdatePreview** imposta la proprietà di [**\_ \_ Anteprima WIA DPS**](-wia-wiaitempropscannerdevice.md) (e la Reimposta prima della restituzione, a meno che non sia stata impostata in precedenza).</span><span class="sxs-lookup"><span data-stu-id="54135-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="54135-140">In questo modo, il driver (e l'hardware) e il filtro di elaborazione delle immagini sanno che l'elemento è un'analisi di anteprima.</span><span class="sxs-lookup"><span data-stu-id="54135-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="54135-141">Un'applicazione deve garantire che *pChildWiaItem* abbia lo stesso formato di immagine [**( \_ \_ formato ipa WIA**](-wia-wiaitempropcommonitem.md)) e la risoluzione ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YRES**) come *pWiaItem* aveva quando è stato passato a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="54135-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="54135-142">Il formato dell'elemento figlio deve corrispondere al formato dell'immagine memorizzata nella cache del componente WIA 2,0 Preview (il componente di anteprima WIA 2,0 non esegue alcuna conversione dell'immagine).</span><span class="sxs-lookup"><span data-stu-id="54135-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="54135-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="54135-143">Examples</span></span>

<span data-ttu-id="54135-144">UpdateRegion deve essere chiamato ogni volta che un utente cambia, ad esempio, la luminosità o il contrasto per l'elemento figlio rappresentato da `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="54135-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="54135-145">Questo elemento figlio è stato precedentemente creato dal filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span><span class="sxs-lookup"><span data-stu-id="54135-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="54135-146">L'immagine scritta in [IStream](/windows/win32/api/objidl/nn-objidl-istream) viene restituita dal metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) dell'interfaccia di callback di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="54135-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="54135-147">Il codice per GetSubRegionItem viene omesso in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="54135-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="54135-148">Dopo che questa funzione è stata chiamata, un'applicazione in genere ridisegni l'area sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="54135-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="54135-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54135-149">Requirements</span></span>



| <span data-ttu-id="54135-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="54135-150">Requirement</span></span> | <span data-ttu-id="54135-151">Valore</span><span class="sxs-lookup"><span data-stu-id="54135-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54135-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54135-152">Minimum supported client</span></span><br/> | <span data-ttu-id="54135-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54135-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54135-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54135-154">Minimum supported server</span></span><br/> | <span data-ttu-id="54135-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54135-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="54135-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54135-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="54135-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="54135-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="54135-158">IDL</span><span class="sxs-lookup"><span data-stu-id="54135-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54135-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54135-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
