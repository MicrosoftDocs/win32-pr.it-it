---
description: Il metodo GetGroupCount Recupera il numero di gruppi contenuti nella sequenza temporale.
ms.assetid: 24351e03-3132-4363-8171-eae517fb770a
title: 'Metodo IAMTimeline:: GetGroupCount (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroupCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4d16cf44839b05f39bc747cb89eda77842caa04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330829"
---
# <a name="iamtimelinegetgroupcount-method"></a><span data-ttu-id="bad54-103">Metodo IAMTimeline:: GetGroupCount</span><span class="sxs-lookup"><span data-stu-id="bad54-103">IAMTimeline::GetGroupCount method</span></span>

> [!Note]  
> <span data-ttu-id="bad54-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bad54-104">\[Deprecated.</span></span> <span data-ttu-id="bad54-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bad54-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bad54-106">Il `GetGroupCount` metodo recupera il numero di gruppi contenuti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="bad54-106">The `GetGroupCount` method retrieves the number of groups that are contained in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad54-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bad54-107">Syntax</span></span>


```C++
HRESULT GetGroupCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="bad54-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bad54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad54-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="bad54-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="bad54-110">Riceve il numero di gruppi nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="bad54-110">Receives the number of groups in the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad54-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bad54-111">Return value</span></span>

<span data-ttu-id="bad54-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bad54-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bad54-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bad54-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad54-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bad54-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bad54-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bad54-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bad54-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bad54-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bad54-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bad54-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bad54-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bad54-118">Requirements</span></span>



| <span data-ttu-id="bad54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad54-119">Requirement</span></span> | <span data-ttu-id="bad54-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bad54-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bad54-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bad54-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bad54-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad54-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bad54-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="bad54-123">Library</span></span><br/> | <dl> <span data-ttu-id="bad54-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bad54-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad54-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bad54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad54-126">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="bad54-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="bad54-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="bad54-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




