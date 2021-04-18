---
description: Il metodo GetPriority recupera la priorità del gruppo.
ms.assetid: d698317f-ace6-40ed-b125-7e2427fb683b
title: 'Metodo IAMTimelineGroup:: GetPriority (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eef0c4e0c2db439a7c593841d3aed44ab7654db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328621"
---
# <a name="iamtimelinegroupgetpriority-method"></a><span data-ttu-id="63420-103">Metodo IAMTimelineGroup:: GetPriority</span><span class="sxs-lookup"><span data-stu-id="63420-103">IAMTimelineGroup::GetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="63420-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="63420-104">\[Deprecated.</span></span> <span data-ttu-id="63420-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="63420-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="63420-106">Il `GetPriority` metodo recupera la priorità del gruppo.</span><span class="sxs-lookup"><span data-stu-id="63420-106">The `GetPriority` method retrieves the group's priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="63420-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63420-107">Syntax</span></span>


```C++
HRESULT GetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="63420-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="63420-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63420-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="63420-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="63420-110">Riceve la priorità del gruppo.</span><span class="sxs-lookup"><span data-stu-id="63420-110">Receives the group's priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63420-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63420-111">Return value</span></span>

<span data-ttu-id="63420-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="63420-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63420-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63420-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63420-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="63420-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63420-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="63420-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="63420-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="63420-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="63420-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="63420-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63420-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63420-118">Requirements</span></span>



| <span data-ttu-id="63420-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63420-119">Requirement</span></span> | <span data-ttu-id="63420-120">Valore</span><span class="sxs-lookup"><span data-stu-id="63420-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63420-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63420-121">Header</span></span><br/>  | <dl> <span data-ttu-id="63420-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="63420-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="63420-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="63420-123">Library</span></span><br/> | <dl> <span data-ttu-id="63420-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63420-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63420-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63420-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63420-126">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="63420-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="63420-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="63420-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




