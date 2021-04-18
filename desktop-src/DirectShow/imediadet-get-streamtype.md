---
description: Il \_ metodo Get StreamType recupera l'identificatore univoco globale (Guid) per il tipo di supporto del flusso corrente.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Metodo IMediaDet:: get_StreamType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332031"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="e0a5f-103">Metodo IMediaDet:: Get \_ StreamType</span><span class="sxs-lookup"><span data-stu-id="e0a5f-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="e0a5f-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-104">\[Deprecated.</span></span> <span data-ttu-id="e0a5f-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0a5f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0a5f-106">Il `get_StreamType` metodo recupera l'identificatore univoco globale (Guid) per il tipo di supporto del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a5f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0a5f-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e0a5f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0a5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a5f-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e0a5f-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a5f-110">Riceve il GUID di tipo principale per il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0a5f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0a5f-111">Return value</span></span>

<span data-ttu-id="e0a5f-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0a5f-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0a5f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a5f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0a5f-114">Remarks</span></span>

<span data-ttu-id="e0a5f-115">Questo metodo recupera il membro **majortype** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="e0a5f-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="e0a5f-116">La struttura del **\_ \_ tipo di supporto am** descrive il formato del flusso e il membro **majortype** è un GUID che indica la categoria generale, ad esempio audio o video.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="e0a5f-117">Per un flusso video, il GUID è MEDIATYPE \_ video.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="e0a5f-118">Per audio, è MEDIATYPE \_ audio.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="e0a5f-119">Per recuperare l'intera struttura del **\_ \_ tipo di supporto** , chiamare il metodo [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="e0a5f-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="e0a5f-120">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="e0a5f-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="e0a5f-121">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="e0a5f-122">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="e0a5f-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="e0a5f-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0a5f-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0a5f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e0a5f-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e0a5f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0a5f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0a5f-126">Requirements</span></span>



| <span data-ttu-id="e0a5f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a5f-127">Requirement</span></span> | <span data-ttu-id="e0a5f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e0a5f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a5f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0a5f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e0a5f-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0a5f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e0a5f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0a5f-131">Library</span></span><br/> | <dl> <span data-ttu-id="e0a5f-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0a5f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a5f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0a5f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a5f-134">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="e0a5f-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="e0a5f-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e0a5f-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




