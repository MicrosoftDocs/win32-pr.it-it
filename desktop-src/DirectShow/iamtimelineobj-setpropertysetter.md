---
description: Il metodo SetPropertySetter imposta il metodo di impostazione della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto. Chiamare questo metodo sugli oggetti di transizione ed effetto.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Metodo IAMTimelineObj:: SetPropertySetter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330815"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="700e1-105">Metodo IAMTimelineObj:: SetPropertySetter</span><span class="sxs-lookup"><span data-stu-id="700e1-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="700e1-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="700e1-106">\[Deprecated.</span></span> <span data-ttu-id="700e1-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="700e1-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="700e1-108">Il `SetPropertySetter` metodo imposta il metodo di impostazione della proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="700e1-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="700e1-109">Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="700e1-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="700e1-110">Chiamare questo metodo sugli oggetti di transizione ed effetto.</span><span class="sxs-lookup"><span data-stu-id="700e1-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="700e1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="700e1-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="700e1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="700e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700e1-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="700e1-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="700e1-114">Puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) del setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="700e1-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700e1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="700e1-115">Return value</span></span>

<span data-ttu-id="700e1-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="700e1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="700e1-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="700e1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="700e1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="700e1-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="700e1-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="700e1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="700e1-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="700e1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="700e1-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="700e1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="700e1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700e1-122">Requirements</span></span>



| <span data-ttu-id="700e1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="700e1-123">Requirement</span></span> | <span data-ttu-id="700e1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="700e1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="700e1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="700e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="700e1-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="700e1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="700e1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="700e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="700e1-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="700e1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700e1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700e1-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="700e1-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="700e1-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="700e1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




