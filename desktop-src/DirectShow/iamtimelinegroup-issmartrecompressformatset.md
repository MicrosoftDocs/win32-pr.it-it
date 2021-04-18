---
description: Il metodo IsSmartRecompressFormatSet determina se è stato impostato un formato di ricompressione intelligente per il gruppo.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'Metodo IAMTimelineGroup:: IsSmartRecompressFormatSet (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328613"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="4c984-103">Metodo IAMTimelineGroup:: IsSmartRecompressFormatSet</span><span class="sxs-lookup"><span data-stu-id="4c984-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="4c984-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4c984-104">\[Deprecated.</span></span> <span data-ttu-id="4c984-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c984-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c984-106">Il `IsSmartRecompressFormatSet` metodo determina se è stato impostato un formato di ricompressione intelligente per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="4c984-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c984-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c984-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4c984-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c984-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="4c984-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4c984-110">Riceve un valore booleano che indica se è stato impostato un formato di compressione.</span><span class="sxs-lookup"><span data-stu-id="4c984-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="4c984-111">Se **true**, è stato impostato un formato di compressione.</span><span class="sxs-lookup"><span data-stu-id="4c984-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c984-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c984-112">Return value</span></span>

<span data-ttu-id="4c984-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c984-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c984-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c984-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c984-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c984-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c984-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4c984-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c984-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c984-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c984-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c984-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c984-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c984-119">Requirements</span></span>



| <span data-ttu-id="4c984-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c984-120">Requirement</span></span> | <span data-ttu-id="4c984-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4c984-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c984-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c984-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4c984-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c984-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c984-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c984-124">Library</span></span><br/> | <dl> <span data-ttu-id="4c984-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c984-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c984-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c984-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c984-127">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="4c984-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="4c984-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4c984-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




