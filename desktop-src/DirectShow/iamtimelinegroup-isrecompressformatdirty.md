---
description: 'Metodo IAMTimelineGroup::IsRecompressFormatDirty : non supportato.'
ms.assetid: 4fd6b9d9-1749-44e6-884a-16faeced4ed6
title: Metodo IAMTimelineGroup::IsRecompressFormatDirty (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsRecompressFormatDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 842b4178f93505a2848fa01aa055541943fb3c22
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098619"
---
# <a name="iamtimelinegroupisrecompressformatdirty-method"></a><span data-ttu-id="3b518-103">Metodo IAMTimelineGroup::IsRecompressFormatDirty</span><span class="sxs-lookup"><span data-stu-id="3b518-103">IAMTimelineGroup::IsRecompressFormatDirty method</span></span>

> [!Note]  
> <span data-ttu-id="3b518-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3b518-104">\[Deprecated.</span></span> <span data-ttu-id="3b518-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b518-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b518-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="3b518-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b518-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b518-107">Syntax</span></span>


```C++
HRESULT IsRecompressFormatDirty(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3b518-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b518-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b518-109">*Pval*</span><span class="sxs-lookup"><span data-stu-id="3b518-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3b518-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3b518-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b518-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b518-111">Return value</span></span>

<span data-ttu-id="3b518-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b518-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b518-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3b518-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b518-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b518-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b518-115">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="3b518-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b518-116">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b518-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b518-117">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3b518-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b518-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b518-118">Requirements</span></span>



| <span data-ttu-id="3b518-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b518-119">Requirement</span></span> | <span data-ttu-id="3b518-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3b518-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b518-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b518-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3b518-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="3b518-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b518-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3b518-123">Library</span></span><br/> | <dl> <span data-ttu-id="3b518-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b518-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b518-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b518-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b518-126">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="3b518-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




