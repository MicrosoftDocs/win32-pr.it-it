---
description: Il metodo GetTimelineType Recupera il tipo dell'oggetto.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'Metodo IAMTimelineObj:: GetTimelineType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324002"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="bb0b3-103">Metodo IAMTimelineObj:: GetTimelineType</span><span class="sxs-lookup"><span data-stu-id="bb0b3-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="bb0b3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-104">\[Deprecated.</span></span> <span data-ttu-id="bb0b3-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb0b3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb0b3-106">Il `GetTimelineType` metodo recupera il tipo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0b3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb0b3-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bb0b3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb0b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb0b3-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="bb0b3-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="bb0b3-110">Riceve un membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che indica il tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb0b3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb0b3-111">Return value</span></span>

<span data-ttu-id="bb0b3-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb0b3-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb0b3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb0b3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb0b3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb0b3-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb0b3-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb0b3-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb0b3-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bb0b3-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb0b3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb0b3-118">Requirements</span></span>



| <span data-ttu-id="bb0b3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb0b3-119">Requirement</span></span> | <span data-ttu-id="bb0b3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bb0b3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0b3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb0b3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bb0b3-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb0b3-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb0b3-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb0b3-123">Library</span></span><br/> | <dl> <span data-ttu-id="bb0b3-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb0b3-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0b3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb0b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0b3-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="bb0b3-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="bb0b3-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="bb0b3-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




