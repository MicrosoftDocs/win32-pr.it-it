---
description: Non supportata.
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: 'Metodo IAMTimeline:: GetDirtyRange (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2eb0c830e7bdf441432130785e1e5397d1d4267e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331094"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="0e759-103">Metodo IAMTimeline:: GetDirtyRange</span><span class="sxs-lookup"><span data-stu-id="0e759-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="0e759-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0e759-104">\[Deprecated.</span></span> <span data-ttu-id="0e759-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e759-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e759-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="0e759-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e759-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e759-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="0e759-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e759-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e759-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="0e759-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0e759-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0e759-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e759-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="0e759-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="0e759-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0e759-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e759-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e759-113">Return value</span></span>

<span data-ttu-id="0e759-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0e759-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e759-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e759-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e759-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e759-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e759-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0e759-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e759-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e759-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e759-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0e759-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e759-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e759-120">Requirements</span></span>



| <span data-ttu-id="0e759-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e759-121">Requirement</span></span> | <span data-ttu-id="0e759-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0e759-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e759-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e759-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0e759-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e759-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e759-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e759-125">Library</span></span><br/> | <dl> <span data-ttu-id="0e759-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e759-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e759-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e759-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e759-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="0e759-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




