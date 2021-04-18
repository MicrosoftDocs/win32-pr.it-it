---
description: Il metodo GetMediaType Recupera il tipo di supporto non compresso per il gruppo.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'Metodo IAMTimelineGroup:: GetMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333685"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="8934b-103">Metodo IAMTimelineGroup:: GetMediaType</span><span class="sxs-lookup"><span data-stu-id="8934b-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="8934b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8934b-104">\[Deprecated.</span></span> <span data-ttu-id="8934b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8934b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8934b-106">Il `GetMediaType` metodo recupera il tipo di supporto non compresso per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="8934b-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="8934b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8934b-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8934b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8934b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8934b-109">*PMT* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8934b-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8934b-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) compilata con il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8934b-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8934b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8934b-111">Return value</span></span>

<span data-ttu-id="8934b-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8934b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8934b-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8934b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8934b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8934b-114">Remarks</span></span>

<span data-ttu-id="8934b-115">Il chiamante deve liberare il blocco di formato del tipo di supporto restituito, fornito nel membro **pbFormat** della struttura del \_ tipo di supporto am restituito \_ .</span><span class="sxs-lookup"><span data-stu-id="8934b-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="8934b-116">È possibile usare la funzione helper [**FreeMediaType**](freemediatype.md) dalla libreria di classi di base.</span><span class="sxs-lookup"><span data-stu-id="8934b-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="8934b-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8934b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8934b-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8934b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8934b-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8934b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8934b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8934b-120">Requirements</span></span>



| <span data-ttu-id="8934b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8934b-121">Requirement</span></span> | <span data-ttu-id="8934b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8934b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8934b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8934b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8934b-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8934b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8934b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8934b-125">Library</span></span><br/> | <dl> <span data-ttu-id="8934b-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8934b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8934b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8934b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8934b-128">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="8934b-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="8934b-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8934b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




