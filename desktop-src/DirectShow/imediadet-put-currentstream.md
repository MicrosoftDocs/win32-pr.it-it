---
description: Il \_ metodo Put CurrentStream specifica il numero di flusso per il rilevatore multimediale da usare.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'IMediaDet: metodo:p ut_CurrentStream (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327824"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="828c2-103">IMediaDet::p UT \_ CurrentStream metodo</span><span class="sxs-lookup"><span data-stu-id="828c2-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="828c2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="828c2-104">\[Deprecated.</span></span> <span data-ttu-id="828c2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="828c2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="828c2-106">Il `put_CurrentStream` metodo specifica il numero di flusso per il rilevatore multimediale da usare.</span><span class="sxs-lookup"><span data-stu-id="828c2-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="828c2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="828c2-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="828c2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="828c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828c2-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="828c2-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="828c2-110">Numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="828c2-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="828c2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="828c2-111">Return value</span></span>

<span data-ttu-id="828c2-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="828c2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="828c2-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="828c2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="828c2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="828c2-114">Remarks</span></span>

<span data-ttu-id="828c2-115">Prima di chiamare questo metodo, chiamare [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) per impostare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="828c2-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="828c2-116">Chiamare [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) per determinare il numero di flussi contenuti nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="828c2-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="828c2-117">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="828c2-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="828c2-118">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="828c2-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="828c2-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="828c2-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="828c2-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="828c2-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="828c2-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="828c2-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="828c2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="828c2-122">Requirements</span></span>



| <span data-ttu-id="828c2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="828c2-123">Requirement</span></span> | <span data-ttu-id="828c2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="828c2-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="828c2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="828c2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="828c2-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="828c2-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="828c2-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="828c2-127">Library</span></span><br/> | <dl> <span data-ttu-id="828c2-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="828c2-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828c2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="828c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828c2-130">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="828c2-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="828c2-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="828c2-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




