---
description: Il metodo GetMediaLength recupera la lunghezza del supporto di questo oggetto di origine.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'Metodo IAMTimelineSrc:: GetMediaLength (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329144"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="77475-103">Metodo IAMTimelineSrc:: GetMediaLength</span><span class="sxs-lookup"><span data-stu-id="77475-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="77475-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="77475-104">\[Deprecated.</span></span> <span data-ttu-id="77475-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77475-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="77475-106">Il `GetMediaLength` metodo recupera la lunghezza del supporto di questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="77475-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="77475-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77475-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="77475-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77475-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77475-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="77475-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="77475-110">Riceve la lunghezza del supporto in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="77475-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77475-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77475-111">Return value</span></span>

<span data-ttu-id="77475-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="77475-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="77475-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="77475-113">Return code</span></span>                                                                                     | <span data-ttu-id="77475-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77475-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="77475-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77475-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="77475-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="77475-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="77475-117"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="77475-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="77475-118">I tempi dei supporti non sono impostati per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="77475-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="77475-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="77475-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="77475-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="77475-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="77475-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="77475-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="77475-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="77475-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="77475-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="77475-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="77475-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="77475-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77475-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77475-125">Requirements</span></span>



| <span data-ttu-id="77475-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="77475-126">Requirement</span></span> | <span data-ttu-id="77475-127">Valore</span><span class="sxs-lookup"><span data-stu-id="77475-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77475-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77475-128">Header</span></span><br/>  | <dl> <span data-ttu-id="77475-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="77475-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="77475-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="77475-130">Library</span></span><br/> | <dl> <span data-ttu-id="77475-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77475-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77475-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77475-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77475-133">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="77475-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="77475-134">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="77475-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="77475-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="77475-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




