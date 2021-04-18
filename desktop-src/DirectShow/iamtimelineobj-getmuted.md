---
description: Il metodo getmuted recupera lo stato disattivato dell'oggetto.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'Metodo IAMTimelineObj:: getmute (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331272"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="b91e8-103">Metodo IAMTimelineObj:: getmuted</span><span class="sxs-lookup"><span data-stu-id="b91e8-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="b91e8-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b91e8-104">\[Deprecated.</span></span> <span data-ttu-id="b91e8-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b91e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b91e8-106">Il `GetMuted` metodo recupera lo stato di silenziamento dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b91e8-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b91e8-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b91e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b91e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91e8-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="b91e8-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b91e8-110">Riceve un valore che indica lo stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="b91e8-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="b91e8-111">Se il valore è **true**, l'oggetto e i relativi elementi figlio vengono disattivati.</span><span class="sxs-lookup"><span data-stu-id="b91e8-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91e8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b91e8-112">Return value</span></span>

<span data-ttu-id="b91e8-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b91e8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b91e8-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b91e8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b91e8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b91e8-115">Remarks</span></span>

<span data-ttu-id="b91e8-116">Se l'elemento padre di un oggetto viene disattivato, l'oggetto viene disattivato indipendentemente dallo stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="b91e8-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="b91e8-117">Quando l'elemento padre non viene più disattivato, viene ripristinato lo stato precedente disattivato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b91e8-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="b91e8-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b91e8-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b91e8-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b91e8-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b91e8-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b91e8-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b91e8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b91e8-121">Requirements</span></span>



| <span data-ttu-id="b91e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91e8-122">Requirement</span></span> | <span data-ttu-id="b91e8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b91e8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91e8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b91e8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b91e8-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b91e8-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b91e8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b91e8-126">Library</span></span><br/> | <dl> <span data-ttu-id="b91e8-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b91e8-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91e8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b91e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91e8-129">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b91e8-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b91e8-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b91e8-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




