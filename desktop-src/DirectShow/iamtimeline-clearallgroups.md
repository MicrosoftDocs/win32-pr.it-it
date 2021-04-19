---
description: Il metodo ClearAllGroups rimuove tutti i gruppi dalla sequenza temporale, insieme a tutti gli oggetti contenuti in tali gruppi.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'Metodo IAMTimeline:: ClearAllGroups (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326805"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="9ee62-103">Metodo IAMTimeline:: ClearAllGroups</span><span class="sxs-lookup"><span data-stu-id="9ee62-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="9ee62-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9ee62-104">\[Deprecated.</span></span> <span data-ttu-id="9ee62-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ee62-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ee62-106">Il `ClearAllGroups` metodo rimuove tutti i gruppi dalla sequenza temporale, insieme a tutti gli oggetti contenuti in tali gruppi.</span><span class="sxs-lookup"><span data-stu-id="9ee62-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee62-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ee62-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="9ee62-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ee62-108">Parameters</span></span>

<span data-ttu-id="9ee62-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9ee62-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ee62-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ee62-110">Return value</span></span>

<span data-ttu-id="9ee62-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ee62-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ee62-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ee62-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ee62-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ee62-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ee62-114">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9ee62-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ee62-115">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ee62-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ee62-116">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ee62-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ee62-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ee62-117">Requirements</span></span>



| <span data-ttu-id="9ee62-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ee62-118">Requirement</span></span> | <span data-ttu-id="9ee62-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9ee62-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee62-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ee62-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9ee62-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee62-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ee62-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ee62-122">Library</span></span><br/> | <dl> <span data-ttu-id="9ee62-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ee62-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ee62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee62-125">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="9ee62-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="9ee62-126">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="9ee62-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




