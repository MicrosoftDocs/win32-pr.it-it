---
description: Il \_ metodo Get OutputStreams Recupera il numero di flussi audio e video contenuti nell'origine multimediale. Tutti gli altri tipi di flusso, ad esempio i flussi di dati, vengono ignorati.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Metodo IMediaDet:: get_OutputStreams (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331504"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="cae79-104">Metodo IMediaDet:: Get \_ OutputStreams</span><span class="sxs-lookup"><span data-stu-id="cae79-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="cae79-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="cae79-105">\[Deprecated.</span></span> <span data-ttu-id="cae79-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cae79-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cae79-107">Il `get_OutputStreams` metodo recupera il numero di flussi audio e video contenuti nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="cae79-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="cae79-108">Tutti gli altri tipi di flusso, ad esempio i flussi di dati, vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="cae79-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae79-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cae79-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cae79-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cae79-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae79-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cae79-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cae79-112">Riceve il numero di flussi di output.</span><span class="sxs-lookup"><span data-stu-id="cae79-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae79-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cae79-113">Return value</span></span>

<span data-ttu-id="cae79-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cae79-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cae79-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cae79-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae79-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cae79-116">Remarks</span></span>

<span data-ttu-id="cae79-117">Prima di chiamare questo metodo, chiamare [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) per impostare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="cae79-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="cae79-118">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cae79-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="cae79-119">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="cae79-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="cae79-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="cae79-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cae79-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cae79-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cae79-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cae79-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cae79-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cae79-123">Requirements</span></span>



| <span data-ttu-id="cae79-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae79-124">Requirement</span></span> | <span data-ttu-id="cae79-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cae79-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae79-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cae79-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cae79-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae79-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cae79-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="cae79-128">Library</span></span><br/> | <dl> <span data-ttu-id="cae79-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae79-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae79-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cae79-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae79-131">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="cae79-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="cae79-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cae79-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




