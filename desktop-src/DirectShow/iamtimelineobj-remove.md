---
description: Il metodo Remove rimuove questo oggetto dalla sequenza temporale (inclusi gli oggetti figlio), per il reinserimento altrove.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Metodo IAMTimelineObj:: Remove (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330824"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="83411-103">Metodo IAMTimelineObj:: Remove</span><span class="sxs-lookup"><span data-stu-id="83411-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="83411-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="83411-104">\[Deprecated.</span></span> <span data-ttu-id="83411-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83411-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="83411-106">Il `Remove` metodo rimuove l'oggetto dalla sequenza temporale (inclusi gli oggetti figlio), per il reinserimento altrove.</span><span class="sxs-lookup"><span data-stu-id="83411-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="83411-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83411-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="83411-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83411-108">Parameters</span></span>

<span data-ttu-id="83411-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="83411-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83411-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83411-110">Return value</span></span>

<span data-ttu-id="83411-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="83411-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83411-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83411-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="83411-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="83411-113">Remarks</span></span>

<span data-ttu-id="83411-114">Chiamare questo metodo solo se l'applicazione inserisce immediatamente nuovamente l'oggetto nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="83411-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="83411-115">Non è un'operazione valida chiamare questo metodo senza reinserire l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="83411-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="83411-116">Per rimuovere un oggetto in modo permanente, chiamare [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="83411-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="83411-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="83411-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="83411-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="83411-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="83411-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="83411-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83411-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83411-120">Requirements</span></span>



| <span data-ttu-id="83411-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="83411-121">Requirement</span></span> | <span data-ttu-id="83411-122">Valore</span><span class="sxs-lookup"><span data-stu-id="83411-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83411-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83411-123">Header</span></span><br/>  | <dl> <span data-ttu-id="83411-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="83411-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="83411-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="83411-125">Library</span></span><br/> | <dl> <span data-ttu-id="83411-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83411-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83411-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83411-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83411-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="83411-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="83411-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="83411-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




