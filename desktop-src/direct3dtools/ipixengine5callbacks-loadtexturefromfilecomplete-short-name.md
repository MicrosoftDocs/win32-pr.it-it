---
description: Funzione di callback utilizzata per notificare all'host quando è stato completato un caricamento della trama.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5Callbacks:: LoadTextureFromFileComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304186"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="0ed6e-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>Metodo IPixEngine5Callbacks:: LoadTextureFromFileComplete</span><span class="sxs-lookup"><span data-stu-id="0ed6e-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="0ed6e-104">Funzione di callback utilizzata per notificare all'host quando è stato completato un caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ed6e-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="0ed6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ed6e-106">Parameters</span></span>

<span data-ttu-id="0ed6e-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-107">*textureId* </span></span>  
<span data-ttu-id="0ed6e-108">ID della trama caricata.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="0ed6e-109">*textureDesc* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-109">*textureDesc* </span></span>  
<span data-ttu-id="0ed6e-110">Descrittore di trama della trama caricata.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="0ed6e-111">*numSlices* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-111">*numSlices* </span></span>  
<span data-ttu-id="0ed6e-112">Numero di sezioni della trama.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-112">The number of slices the texture has.</span></span>

<span data-ttu-id="0ed6e-113">*\_sliceIndicies count2* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="0ed6e-114">Sezionare indici associato alla trama.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="0ed6e-115">*\_sliceDescriptors count2* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="0ed6e-116">Descrittori per ogni sezione.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-116">Descriptors for each slice.</span></span>

<span data-ttu-id="0ed6e-117">*numFormatOverrides* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="0ed6e-118">Numero di sostituzioni di formato.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-118">The number of format overrides.</span></span>

<span data-ttu-id="0ed6e-119">*\_formatOverrides count5* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="0ed6e-120">Il formato sostituisce.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-120">The format overrides.</span></span>

<span data-ttu-id="0ed6e-121">*istogramma* </span><span class="sxs-lookup"><span data-stu-id="0ed6e-121">*histogram* </span></span>  
<span data-ttu-id="0ed6e-122">Indirizzo dei dati dell'istogramma per la trama caricata.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ed6e-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ed6e-123">Return value</span></span>

<span data-ttu-id="0ed6e-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ed6e-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ed6e-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed6e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ed6e-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0ed6e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ed6e-127">Header</span></span></p></td><td><span data-ttu-id="0ed6e-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0ed6e-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0ed6e-129"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0ed6e-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0ed6e-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="0ed6e-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
