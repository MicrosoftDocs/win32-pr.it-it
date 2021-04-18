---
description: Il \_ metodo Get StreamMediaType Recupera il tipo di supporto del flusso corrente. Tutti i flussi video vengono convertiti in tipi VIDEOINFOHEADER e tutti i flussi audio vengono convertiti in tipi WAVEFORMATEX.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Metodo IMediaDet:: get_StreamMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331501"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="7f6c2-104">Metodo IMediaDet:: Get \_ StreamMediaType</span><span class="sxs-lookup"><span data-stu-id="7f6c2-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="7f6c2-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-105">\[Deprecated.</span></span> <span data-ttu-id="7f6c2-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7f6c2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7f6c2-107">Il `get_StreamMediaType` metodo recupera il tipo di supporto del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="7f6c2-108">Tutti i flussi video vengono convertiti in tipi [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e tutti i flussi audio vengono convertiti in tipi [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7f6c2-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6c2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f6c2-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7f6c2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f6c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6c2-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f6c2-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6c2-112">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) compilata con il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6c2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f6c2-113">Return value</span></span>

<span data-ttu-id="7f6c2-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f6c2-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f6c2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f6c2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f6c2-116">Remarks</span></span>

<span data-ttu-id="7f6c2-117">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c2-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="7f6c2-118">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="7f6c2-119">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c2-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="7f6c2-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7f6c2-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f6c2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7f6c2-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f6c2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f6c2-123">Requirements</span></span>



| <span data-ttu-id="7f6c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f6c2-124">Requirement</span></span> | <span data-ttu-id="7f6c2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7f6c2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6c2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f6c2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7f6c2-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c2-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7f6c2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f6c2-128">Library</span></span><br/> | <dl> <span data-ttu-id="7f6c2-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c2-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6c2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f6c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6c2-131">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="7f6c2-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="7f6c2-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7f6c2-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
