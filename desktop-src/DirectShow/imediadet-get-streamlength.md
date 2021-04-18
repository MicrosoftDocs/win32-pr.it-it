---
description: Il \_ metodo Get StreamLength recupera la durata del flusso corrente.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'Metodo IMediaDet:: get_StreamLength (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331503"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="4424a-103">Metodo IMediaDet:: Get \_ StreamLength</span><span class="sxs-lookup"><span data-stu-id="4424a-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="4424a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4424a-104">\[Deprecated.</span></span> <span data-ttu-id="4424a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4424a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4424a-106">Il `get_StreamLength` metodo recupera la durata del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="4424a-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="4424a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4424a-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4424a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4424a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4424a-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4424a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4424a-110">Riceve la durata del flusso, in secondi.</span><span class="sxs-lookup"><span data-stu-id="4424a-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4424a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4424a-111">Return value</span></span>

<span data-ttu-id="4424a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4424a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4424a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4424a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4424a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4424a-114">Remarks</span></span>

<span data-ttu-id="4424a-115">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="4424a-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="4424a-116">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4424a-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="4424a-117">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="4424a-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="4424a-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4424a-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4424a-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4424a-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4424a-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4424a-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4424a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4424a-121">Requirements</span></span>



| <span data-ttu-id="4424a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4424a-122">Requirement</span></span> | <span data-ttu-id="4424a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4424a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4424a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4424a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4424a-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4424a-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4424a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4424a-126">Library</span></span><br/> | <dl> <span data-ttu-id="4424a-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4424a-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4424a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4424a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4424a-129">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="4424a-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="4424a-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4424a-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




