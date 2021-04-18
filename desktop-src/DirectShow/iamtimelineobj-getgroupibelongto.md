---
description: Non supportata.
ms.assetid: a6242c1d-cf9a-4c96-9cfd-d32199ae74b8
title: 'Metodo IAMTimelineObj:: GetGroupIBelongTo (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGroupIBelongTo
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cefd3bb5923e056497556b15b6308160a2066c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331275"
---
# <a name="iamtimelineobjgetgroupibelongto-method"></a><span data-ttu-id="7cbef-103">Metodo IAMTimelineObj:: GetGroupIBelongTo</span><span class="sxs-lookup"><span data-stu-id="7cbef-103">IAMTimelineObj::GetGroupIBelongTo method</span></span>

> [!Note]  
> <span data-ttu-id="7cbef-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7cbef-104">\[Deprecated.</span></span> <span data-ttu-id="7cbef-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7cbef-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="7cbef-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbef-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cbef-107">Syntax</span></span>


```C++
HRESULT GetGroupIBelongTo(
   IAMTimelineGroup **ppGroup
);
```



## <a name="parameters"></a><span data-ttu-id="7cbef-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cbef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbef-109">*ppGroup*</span><span class="sxs-lookup"><span data-stu-id="7cbef-109">*ppGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="7cbef-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7cbef-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cbef-111">Return value</span></span>

<span data-ttu-id="7cbef-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7cbef-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cbef-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cbef-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cbef-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cbef-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7cbef-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7cbef-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7cbef-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7cbef-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7cbef-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7cbef-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7cbef-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cbef-118">Requirements</span></span>



| <span data-ttu-id="7cbef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbef-119">Requirement</span></span> | <span data-ttu-id="7cbef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7cbef-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbef-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cbef-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7cbef-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cbef-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7cbef-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cbef-123">Library</span></span><br/> | <dl> <span data-ttu-id="7cbef-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cbef-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cbef-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cbef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbef-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="7cbef-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




