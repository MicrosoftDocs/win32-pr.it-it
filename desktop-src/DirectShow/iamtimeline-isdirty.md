---
description: 'Metodo IAMTimeline::IsDirty: non supportato.'
ms.assetid: ed6fd633-23b8-4b80-901c-d7b50fa4c15e
title: Metodo IAMTimeline::IsDirty (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.IsDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ee51c44ae99a26e54a616da6752511f8a4e5f4a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119589"
---
# <a name="iamtimelineisdirty-method"></a><span data-ttu-id="5d973-103">Metodo IAMTimeline::IsDirty</span><span class="sxs-lookup"><span data-stu-id="5d973-103">IAMTimeline::IsDirty method</span></span>

> [!Note]  
> <span data-ttu-id="5d973-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5d973-104">\[Deprecated.</span></span> <span data-ttu-id="5d973-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d973-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d973-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5d973-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d973-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d973-107">Syntax</span></span>


```C++
HRESULT IsDirty(
   BOOL *pDirty
);
```



## <a name="parameters"></a><span data-ttu-id="5d973-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d973-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d973-109">*pDirty*</span><span class="sxs-lookup"><span data-stu-id="5d973-109">*pDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="5d973-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5d973-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d973-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d973-111">Return value</span></span>

<span data-ttu-id="5d973-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d973-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d973-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5d973-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d973-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d973-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d973-115">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5d973-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d973-116">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d973-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d973-117">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5d973-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d973-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d973-118">Requirements</span></span>



| <span data-ttu-id="5d973-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d973-119">Requirement</span></span> | <span data-ttu-id="5d973-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5d973-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d973-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d973-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5d973-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="5d973-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d973-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d973-123">Library</span></span><br/> | <dl> <span data-ttu-id="5d973-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d973-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d973-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d973-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d973-126">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="5d973-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




