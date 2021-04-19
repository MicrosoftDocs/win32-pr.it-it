---
description: Il metodo GetSubObjectLoaded determina se il puntatore del sottooggetto è stato impostato.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'Metodo IAMTimelineObj:: GetSubObjectLoaded (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326552"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="d2a1a-103">Metodo IAMTimelineObj:: GetSubObjectLoaded</span><span class="sxs-lookup"><span data-stu-id="d2a1a-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="d2a1a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-104">\[Deprecated.</span></span> <span data-ttu-id="d2a1a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2a1a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2a1a-106">Il `GetSubObjectLoaded` metodo determina se il puntatore del sottooggetto è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a1a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a1a-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d2a1a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2a1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a1a-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="d2a1a-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a1a-110">Riceve un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-110">Receives a Boolean value.</span></span> <span data-ttu-id="d2a1a-111">Se il valore è **true**, il puntatore al sottooggetto è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="d2a1a-112">Se **false**, il puntatore non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a1a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2a1a-113">Return value</span></span>

<span data-ttu-id="d2a1a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2a1a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2a1a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a1a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2a1a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2a1a-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2a1a-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2a1a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2a1a-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d2a1a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2a1a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a1a-120">Requirements</span></span>



| <span data-ttu-id="d2a1a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a1a-121">Requirement</span></span> | <span data-ttu-id="d2a1a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a1a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a1a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2a1a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2a1a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a1a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2a1a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2a1a-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2a1a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2a1a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a1a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a1a-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="d2a1a-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d2a1a-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d2a1a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




