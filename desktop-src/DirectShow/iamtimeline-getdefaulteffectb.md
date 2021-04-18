---
description: "Il metodo GetDefaultEffectB recupera l'effetto predefinito. Questo metodo è equivalente a IAMTimeline:: GetDefaultEffect, ma riceve un valore BSTR anziché un GUID."
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Metodo IAMTimeline:: GetDefaultEffectB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331099"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a><span data-ttu-id="01df5-104">Metodo IAMTimeline:: GetDefaultEffectB</span><span class="sxs-lookup"><span data-stu-id="01df5-104">IAMTimeline::GetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="01df5-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="01df5-105">\[Deprecated.</span></span> <span data-ttu-id="01df5-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01df5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01df5-107">Il `GetDefaultEffectB` metodo recupera l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="01df5-107">The `GetDefaultEffectB` method retrieves the default effect.</span></span> <span data-ttu-id="01df5-108">Questo metodo è equivalente a [**IAMTimeline:: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), ma riceve un valore **BSTR** anziché un GUID.</span><span class="sxs-lookup"><span data-stu-id="01df5-108">This method is equivalent to [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), but receives a **BSTR** value rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="01df5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01df5-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="01df5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="01df5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01df5-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="01df5-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="01df5-112">Riceve un valore **BSTR** che rappresenta il GUID dell'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="01df5-112">Receives a **BSTR** value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01df5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01df5-113">Return value</span></span>

<span data-ttu-id="01df5-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01df5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01df5-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01df5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01df5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="01df5-116">Remarks</span></span>

<span data-ttu-id="01df5-117">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="01df5-117">The method allocates memory for the string.</span></span> <span data-ttu-id="01df5-118">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="01df5-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="01df5-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="01df5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01df5-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="01df5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01df5-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="01df5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01df5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01df5-122">Requirements</span></span>



| <span data-ttu-id="01df5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01df5-123">Requirement</span></span> | <span data-ttu-id="01df5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="01df5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01df5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01df5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="01df5-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01df5-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01df5-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="01df5-127">Library</span></span><br/> | <dl> <span data-ttu-id="01df5-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01df5-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01df5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01df5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01df5-130">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="01df5-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="01df5-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="01df5-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




