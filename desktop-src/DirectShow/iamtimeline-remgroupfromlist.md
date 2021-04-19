---
description: Non supportata.
ms.assetid: 9ad5f5ee-2a2a-448b-9da4-2ad8d543eb22
title: 'Metodo IAMTimeline:: RemGroupFromList (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.RemGroupFromList
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58f7cd07f193a238f4195a5e4ed17e1ede3b548e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326787"
---
# <a name="iamtimelineremgroupfromlist-method"></a><span data-ttu-id="8bf3a-103">Metodo IAMTimeline:: RemGroupFromList</span><span class="sxs-lookup"><span data-stu-id="8bf3a-103">IAMTimeline::RemGroupFromList method</span></span>

> [!Note]  
> <span data-ttu-id="8bf3a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-104">\[Deprecated.</span></span> <span data-ttu-id="8bf3a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8bf3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8bf3a-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf3a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bf3a-107">Syntax</span></span>


```C++
HRESULT RemGroupFromList(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="8bf3a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bf3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf3a-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="8bf3a-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf3a-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf3a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bf3a-111">Return value</span></span>

<span data-ttu-id="8bf3a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bf3a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8bf3a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf3a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8bf3a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8bf3a-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8bf3a-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8bf3a-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8bf3a-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8bf3a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bf3a-118">Requirements</span></span>



| <span data-ttu-id="8bf3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf3a-119">Requirement</span></span> | <span data-ttu-id="8bf3a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8bf3a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf3a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bf3a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf3a-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3a-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8bf3a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bf3a-123">Library</span></span><br/> | <dl> <span data-ttu-id="8bf3a-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3a-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf3a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bf3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf3a-126">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




