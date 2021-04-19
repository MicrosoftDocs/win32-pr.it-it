---
description: 'Il metodo GetDefaultTransitionB recupera la transizione predefinita. Questo metodo è equivalente a IAMTimeline:: GetDefaultTransition, ma riceve un valore BSTR anziché un GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'Metodo IAMTimeline:: GetDefaultTransitionB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332694"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a><span data-ttu-id="43fe0-104">Metodo IAMTimeline:: GetDefaultTransitionB</span><span class="sxs-lookup"><span data-stu-id="43fe0-104">IAMTimeline::GetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="43fe0-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="43fe0-105">\[Deprecated.</span></span> <span data-ttu-id="43fe0-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43fe0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43fe0-107">Il `GetDefaultTransitionB` metodo recupera la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="43fe0-107">The `GetDefaultTransitionB` method retrieves the default transition.</span></span> <span data-ttu-id="43fe0-108">Questo metodo è equivalente a [**IAMTimeline:: GetDefaultTransition**](iamtimeline-getdefaulttransition.md), ma riceve un valore BSTR anziché un GUID.</span><span class="sxs-lookup"><span data-stu-id="43fe0-108">This method is equivalent to [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), but receives a BSTR value, rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fe0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43fe0-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="43fe0-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="43fe0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fe0-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="43fe0-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="43fe0-112">Riceve un valore **BSTR** che rappresenta il GUID della transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="43fe0-112">Receives a **BSTR** value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fe0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43fe0-113">Return value</span></span>

<span data-ttu-id="43fe0-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43fe0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43fe0-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43fe0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43fe0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="43fe0-116">Remarks</span></span>

<span data-ttu-id="43fe0-117">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="43fe0-117">The method allocates memory for the string.</span></span> <span data-ttu-id="43fe0-118">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="43fe0-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="43fe0-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="43fe0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43fe0-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="43fe0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43fe0-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="43fe0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43fe0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43fe0-122">Requirements</span></span>



| <span data-ttu-id="43fe0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fe0-123">Requirement</span></span> | <span data-ttu-id="43fe0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="43fe0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43fe0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43fe0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="43fe0-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fe0-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43fe0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="43fe0-127">Library</span></span><br/> | <dl> <span data-ttu-id="43fe0-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43fe0-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43fe0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43fe0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fe0-130">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="43fe0-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="43fe0-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="43fe0-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




