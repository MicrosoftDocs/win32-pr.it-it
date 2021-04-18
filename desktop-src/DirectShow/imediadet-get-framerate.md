---
description: Il \_ metodo Get framerate recupera la frequenza dei fotogrammi del flusso corrente. Il flusso deve essere un flusso video.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Metodo IMediaDet:: get_FrameRate (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331505"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="ef208-104">Metodo IMediaDet:: Get \_ framerate</span><span class="sxs-lookup"><span data-stu-id="ef208-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="ef208-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ef208-105">\[Deprecated.</span></span> <span data-ttu-id="ef208-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef208-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef208-107">Il `get_FrameRate` metodo recupera la frequenza dei fotogrammi del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="ef208-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="ef208-108">Il flusso deve essere un flusso video.</span><span class="sxs-lookup"><span data-stu-id="ef208-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef208-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef208-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ef208-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef208-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef208-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ef208-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ef208-112">Riceve la frequenza dei fotogrammi, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="ef208-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef208-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef208-113">Return value</span></span>

<span data-ttu-id="ef208-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef208-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ef208-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef208-115">Possible values include the following:</span></span>



| <span data-ttu-id="ef208-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ef208-116">Return code</span></span>                                                                                             | <span data-ttu-id="ef208-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef208-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="ef208-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="ef208-119">L'intestazione del formato video non specifica una frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="ef208-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="ef208-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ef208-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ef208-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ef208-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="ef208-123">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="ef208-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="ef208-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="ef208-125">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="ef208-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="ef208-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="ef208-127">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="ef208-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="ef208-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef208-128">Remarks</span></span>

<span data-ttu-id="ef208-129">Questo metodo non è in grado di recuperare la frequenza dei fotogrammi da un file ASF.</span><span class="sxs-lookup"><span data-stu-id="ef208-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="ef208-130">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="ef208-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="ef208-131">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ef208-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="ef208-132">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="ef208-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef208-133">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ef208-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef208-134">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef208-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef208-135">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ef208-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef208-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef208-136">Requirements</span></span>



| <span data-ttu-id="ef208-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef208-137">Requirement</span></span> | <span data-ttu-id="ef208-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ef208-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef208-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef208-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ef208-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef208-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef208-141">Library</span></span><br/> | <dl> <span data-ttu-id="ef208-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef208-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef208-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef208-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef208-144">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="ef208-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="ef208-145">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ef208-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




