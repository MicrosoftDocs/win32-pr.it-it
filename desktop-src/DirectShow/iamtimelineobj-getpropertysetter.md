---
description: Il metodo GetPropertySetter Recupera il metodo di impostazione della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Metodo IAMTimelineObj:: GetPropertySetter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331271"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="8fac9-104">Metodo IAMTimelineObj:: GetPropertySetter</span><span class="sxs-lookup"><span data-stu-id="8fac9-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="8fac9-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8fac9-105">\[Deprecated.</span></span> <span data-ttu-id="8fac9-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8fac9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8fac9-107">Il `GetPropertySetter` metodo recupera il setter della proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8fac9-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="8fac9-108">Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8fac9-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fac9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fac9-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8fac9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fac9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fac9-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8fac9-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8fac9-112">Riceve un puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) del setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fac9-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="8fac9-113">Se l'oggetto non dispone di un setter di proprietà, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="8fac9-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fac9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fac9-114">Return value</span></span>

<span data-ttu-id="8fac9-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8fac9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8fac9-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fac9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fac9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fac9-117">Remarks</span></span>

<span data-ttu-id="8fac9-118">Se il valore restituito in *pval* non è **null**, l'interfaccia **IPropertySetter** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="8fac9-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="8fac9-119">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="8fac9-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="8fac9-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8fac9-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8fac9-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8fac9-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8fac9-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8fac9-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fac9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fac9-123">Requirements</span></span>



| <span data-ttu-id="8fac9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fac9-124">Requirement</span></span> | <span data-ttu-id="8fac9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8fac9-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fac9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fac9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8fac9-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fac9-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8fac9-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fac9-128">Library</span></span><br/> | <dl> <span data-ttu-id="8fac9-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fac9-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fac9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fac9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fac9-131">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="8fac9-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8fac9-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8fac9-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




