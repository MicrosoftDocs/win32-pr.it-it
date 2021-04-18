---
description: Il metodo seprops imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Metodo IPropertySetter:: seprops (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329621"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="ffe3e-103">Metodo IPropertySetter:: seprops</span><span class="sxs-lookup"><span data-stu-id="ffe3e-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="ffe3e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-104">\[Deprecated.</span></span> <span data-ttu-id="ffe3e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ffe3e-106">Il `SetProps` metodo imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe3e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffe3e-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="ffe3e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffe3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe3e-109">*PTarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe3e-110">Puntatore all'oggetto di destinazione per il quale impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="ffe3e-111">*rtNow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe3e-112">Ora in cui impostare le proprietà, in unità 100-nanosecondi, oppure-1 per impostare le proprietà statiche (quelle che non variano nel tempo).</span><span class="sxs-lookup"><span data-stu-id="ffe3e-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe3e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffe3e-113">Return value</span></span>

<span data-ttu-id="ffe3e-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ffe3e-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffe3e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe3e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffe3e-116">Remarks</span></span>

<span data-ttu-id="ffe3e-117">Questo metodo viene chiamato da DES per impostare le proprietà su una transizione o un effetto.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="ffe3e-118">In genere, un'applicazione non chiamerà questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-118">An application will not normally call this method.</span></span>

<span data-ttu-id="ffe3e-119">L'oggetto specificato da *PTarget* deve implementare l'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="ffe3e-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="ffe3e-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ffe3e-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffe3e-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ffe3e-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ffe3e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffe3e-123">Requirements</span></span>



| <span data-ttu-id="ffe3e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffe3e-124">Requirement</span></span> | <span data-ttu-id="ffe3e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ffe3e-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe3e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffe3e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ffe3e-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe3e-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ffe3e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="ffe3e-128">Library</span></span><br/> | <dl> <span data-ttu-id="ffe3e-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffe3e-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe3e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffe3e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe3e-131">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="ffe3e-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="ffe3e-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ffe3e-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




