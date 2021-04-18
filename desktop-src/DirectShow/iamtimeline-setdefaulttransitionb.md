---
description: 'Il metodo SetDefaultTransitionB imposta la transizione predefinita. Questo metodo è equivalente a IAMTimeline:: SetDefaultTransition, ma accetta un valore BSTR anziché un puntatore a un GUID.'
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: 'Metodo IAMTimeline:: SetDefaultTransitionB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 221491dd0be97f1808e469d956c189bf61458278
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325040"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a><span data-ttu-id="4bd99-104">Metodo IAMTimeline:: SetDefaultTransitionB</span><span class="sxs-lookup"><span data-stu-id="4bd99-104">IAMTimeline::SetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="4bd99-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4bd99-105">\[Deprecated.</span></span> <span data-ttu-id="4bd99-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4bd99-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4bd99-107">Il `SetDefaultTransitionB` metodo imposta la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4bd99-107">The `SetDefaultTransitionB` method sets the default transition.</span></span> <span data-ttu-id="4bd99-108">Questo metodo è equivalente a [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md), ma accetta un valore BSTR anziché un puntatore a un GUID.</span><span class="sxs-lookup"><span data-stu-id="4bd99-108">This method is equivalent to [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd99-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bd99-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="4bd99-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bd99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd99-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="4bd99-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd99-112">Valore BSTR che rappresenta il GUID della transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4bd99-112">BSTR value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bd99-113">Return value</span></span>

<span data-ttu-id="4bd99-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4bd99-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bd99-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bd99-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd99-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bd99-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4bd99-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4bd99-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4bd99-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4bd99-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4bd99-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4bd99-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4bd99-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bd99-120">Requirements</span></span>



| <span data-ttu-id="4bd99-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd99-121">Requirement</span></span> | <span data-ttu-id="4bd99-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4bd99-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd99-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bd99-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4bd99-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd99-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4bd99-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4bd99-125">Library</span></span><br/> | <dl> <span data-ttu-id="4bd99-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bd99-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd99-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bd99-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd99-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="4bd99-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="4bd99-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4bd99-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




