---
description: Il metodo GetNextSrcEx recupera l'origine successiva dopo l'origine specificata.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Metodo IAMTimelineTrack:: GetNextSrcEx (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325636"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="c81e2-103">Metodo IAMTimelineTrack:: GetNextSrcEx</span><span class="sxs-lookup"><span data-stu-id="c81e2-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="c81e2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c81e2-104">\[Deprecated.</span></span> <span data-ttu-id="c81e2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c81e2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c81e2-106">Il `GetNextSrcEx` metodo recupera l'origine successiva dopo l'origine specificata.</span><span class="sxs-lookup"><span data-stu-id="c81e2-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="c81e2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c81e2-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="c81e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c81e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81e2-109">*pLast*</span><span class="sxs-lookup"><span data-stu-id="c81e2-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="c81e2-110">Puntatore all'oggetto di origine precedente oppure **null** per recuperare la prima origine nella traccia.</span><span class="sxs-lookup"><span data-stu-id="c81e2-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="c81e2-111">*ppNext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c81e2-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c81e2-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine successivo.</span><span class="sxs-lookup"><span data-stu-id="c81e2-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c81e2-113">Return value</span></span>

<span data-ttu-id="c81e2-114">Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c81e2-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c81e2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c81e2-115">Remarks</span></span>

<span data-ttu-id="c81e2-116">Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="c81e2-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="c81e2-117">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c81e2-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="c81e2-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c81e2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c81e2-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c81e2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c81e2-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c81e2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c81e2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c81e2-121">Requirements</span></span>



| <span data-ttu-id="c81e2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81e2-122">Requirement</span></span> | <span data-ttu-id="c81e2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c81e2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c81e2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c81e2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c81e2-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c81e2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c81e2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c81e2-126">Library</span></span><br/> | <dl> <span data-ttu-id="c81e2-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c81e2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81e2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c81e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81e2-129">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="c81e2-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="c81e2-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c81e2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




