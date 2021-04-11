---
description: "Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview al filtro."
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: Metodo IWiaPreview::D etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226150"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="3349c-103">IWiaPreview::D Metodo etectRegions</span><span class="sxs-lookup"><span data-stu-id="3349c-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="3349c-104">Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro.</span><span class="sxs-lookup"><span data-stu-id="3349c-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3349c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3349c-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3349c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3349c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3349c-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3349c-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3349c-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="3349c-108">Type: **LONG**</span></span>

<span data-ttu-id="3349c-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3349c-109">Not used.</span></span> <span data-ttu-id="3349c-110">Impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="3349c-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3349c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3349c-111">Return value</span></span>

<span data-ttu-id="3349c-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3349c-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3349c-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3349c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3349c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3349c-114">Return code</span></span>                                                                               | <span data-ttu-id="3349c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3349c-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3349c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3349c-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3349c-117">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="3349c-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="3349c-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3349c-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="3349c-119">Il driver non supporta la segmentazione.</span><span class="sxs-lookup"><span data-stu-id="3349c-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="3349c-120"><dt>**in caso contrario**</dt></span><span class="sxs-lookup"><span data-stu-id="3349c-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="3349c-121">Codice di errore COM standard.</span><span class="sxs-lookup"><span data-stu-id="3349c-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="3349c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="3349c-122">Remarks</span></span>

<span data-ttu-id="3349c-123">Prima di chiamare questa funzione, un'applicazione deve chiamare [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="3349c-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="3349c-124">Quando il componente Windows Image Acquisition (WIA) 2,0 Preview chiama **IWiaPreview::D etectregions**, richiama il filtro di segmentazione del driver e passa l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) passata in precedenza a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="3349c-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="3349c-125">Passa anche l'immagine memorizzata nella cache internamente al filtro.</span><span class="sxs-lookup"><span data-stu-id="3349c-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="3349c-126">Il filtro di segmentazione usa l'immagine memorizzata nella cache per creare gli extent figlio.</span><span class="sxs-lookup"><span data-stu-id="3349c-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="3349c-127">Se un'applicazione modifica le proprietà dell'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dopo aver chiamato [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), è necessario ripristinare le proprietà originali prima che l'applicazione chiami **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="3349c-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="3349c-128">Usare [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) per ripristinare le proprietà originali.</span><span class="sxs-lookup"><span data-stu-id="3349c-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="3349c-129">**IWiaPreview::D etectregions** viene usato per determinare le "aree secondarie" dell'immagine memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="3349c-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="3349c-130">Per ogni area secondaria rilevata, viene creato un nuovo elemento figlio WIA 2,0 sotto l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3349c-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="3349c-131">Per ogni elemento figlio, il filtro di segmentazione deve impostare i valori per le seguenti proprietà WIA 2,0: WIA \_ IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ stampa e WIA \_ IP \_ YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="3349c-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="3349c-132">Un filtro più avanzato Imposta altre proprietà WIA 2,0, ad esempio \_ gli indirizzi IP WIA \_ deasimmetria \_ X e WIA \_ IP \_ desfasamento \_ Y, se il driver supporta la deasimmetria.</span><span class="sxs-lookup"><span data-stu-id="3349c-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="3349c-133">Le \_ Proprietà WIA IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ stampa e WIA \_ IPS \_ YEXTENT rappresentano il rettangolo di delimitazione dell'area da analizzare.</span><span class="sxs-lookup"><span data-stu-id="3349c-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="3349c-134">Il driver potrebbe non supportare la segmentazione.</span><span class="sxs-lookup"><span data-stu-id="3349c-134">The driver might not support segmentation.</span></span> <span data-ttu-id="3349c-135">Prima di chiamare **IWiaPreview::D etectregions**, un'applicazione in genere controlla se il driver supporta la \_ proprietà di segmentazione degli indirizzi IP WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="3349c-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="3349c-136">Se la proprietà non è implementata, la segmentazione non è supportata e **IWiaPreview::D etectregions** ha esito negativo E restituisce e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="3349c-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="3349c-137">L'applicazione deve pulire gli elementi figlio creati chiamando **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="3349c-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="3349c-138">Se, ad esempio, un'applicazione effettua una chiamata aggiuntiva a **IWiaPreview::D etectregions** sullo stesso elemento, deve pulire gli elementi figlio precedenti.</span><span class="sxs-lookup"><span data-stu-id="3349c-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="3349c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3349c-139">Requirements</span></span>



| <span data-ttu-id="3349c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3349c-140">Requirement</span></span> | <span data-ttu-id="3349c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3349c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3349c-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3349c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3349c-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3349c-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3349c-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3349c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3349c-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3349c-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3349c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3349c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3349c-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3349c-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3349c-148">IDL</span><span class="sxs-lookup"><span data-stu-id="3349c-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3349c-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3349c-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




