---
description: Il metodo SetMediaType imposta il tipo di supporto non compresso per il gruppo.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Metodo IAMTimelineGroup:: SetMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331632"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="c730e-103">Metodo IAMTimelineGroup:: SetMediaType</span><span class="sxs-lookup"><span data-stu-id="c730e-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="c730e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c730e-104">\[Deprecated.</span></span> <span data-ttu-id="c730e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c730e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c730e-106">Il `SetMediaType` metodo imposta il tipo di supporto non compresso per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="c730e-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c730e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c730e-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="c730e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c730e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c730e-109">*PMT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c730e-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c730e-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrive il formato.</span><span class="sxs-lookup"><span data-stu-id="c730e-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c730e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c730e-111">Return value</span></span>

<span data-ttu-id="c730e-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="c730e-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="c730e-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c730e-113">Return code</span></span>                                                                                             | <span data-ttu-id="c730e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c730e-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c730e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c730e-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c730e-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c730e-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="c730e-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="c730e-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="c730e-118">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="c730e-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="c730e-119"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="c730e-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="c730e-120">Il tipo di supporto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c730e-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c730e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c730e-121">Remarks</span></span>

<span data-ttu-id="c730e-122">Sono supportati i tipi di supporto seguenti:</span><span class="sxs-lookup"><span data-stu-id="c730e-122">The following media types are supported:</span></span>

-   <span data-ttu-id="c730e-123">Video RGB non compresso</span><span class="sxs-lookup"><span data-stu-id="c730e-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="c730e-124">16 bit per pixel, formato 555 (MEDIASUBTYPE \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="c730e-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="c730e-125">24 bit per pixel (MEDIASUBTYPE \_ RGB24)</span><span class="sxs-lookup"><span data-stu-id="c730e-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="c730e-126">32 bit per pixel, con alfa (MEDIASUBTYPE \_ ARGB32, not MEDIASUBTYPE \_ rgb32)</span><span class="sxs-lookup"><span data-stu-id="c730e-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="c730e-127">audio PCM stereo a 16 bit ( \_ PCM MEDIASUBTYPE)</span><span class="sxs-lookup"><span data-stu-id="c730e-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="c730e-128">I tipi di video devono usare il formato \_ videoinfo per il tipo di formato e [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="c730e-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="c730e-129">Il formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c730e-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="c730e-130">Inoltre, i formati video dall'alto verso il basso (*biHeight* < 0) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="c730e-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="c730e-131">Per specificare un formato di compressione per il gruppo, chiamare il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="c730e-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="c730e-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c730e-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c730e-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c730e-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c730e-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c730e-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c730e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c730e-135">Requirements</span></span>



| <span data-ttu-id="c730e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c730e-136">Requirement</span></span> | <span data-ttu-id="c730e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c730e-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c730e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c730e-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c730e-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c730e-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c730e-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="c730e-140">Library</span></span><br/> | <dl> <span data-ttu-id="c730e-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c730e-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c730e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c730e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c730e-143">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="c730e-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="c730e-144">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c730e-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




