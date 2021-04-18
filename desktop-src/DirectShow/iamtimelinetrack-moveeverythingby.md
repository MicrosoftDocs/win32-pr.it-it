---
description: Questo metodo non è supportato.
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: 'Metodo IAMTimelineTrack:: MoveEverythingBy (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.MoveEverythingBy
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4eded92548c047e6d5102e603a5ab0554bd1f4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325626"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="01c1f-103">Metodo IAMTimelineTrack:: MoveEverythingBy</span><span class="sxs-lookup"><span data-stu-id="01c1f-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="01c1f-104">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="01c1f-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01c1f-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="01c1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c1f-107">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="01c1f-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="01c1f-108">Riservato.</span><span class="sxs-lookup"><span data-stu-id="01c1f-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="01c1f-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="01c1f-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="01c1f-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="01c1f-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c1f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01c1f-111">Return value</span></span>

<span data-ttu-id="01c1f-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01c1f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01c1f-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01c1f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c1f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="01c1f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01c1f-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="01c1f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01c1f-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="01c1f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01c1f-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="01c1f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01c1f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c1f-118">Requirements</span></span>



| <span data-ttu-id="01c1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c1f-119">Requirement</span></span> | <span data-ttu-id="01c1f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="01c1f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01c1f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c1f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="01c1f-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c1f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01c1f-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="01c1f-123">Library</span></span><br/> | <dl> <span data-ttu-id="01c1f-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01c1f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c1f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c1f-126">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="01c1f-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 




