---
description: Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Metodo IProvidePropertyBuilder:: ExecuteBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325215"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="7ad7d-103">Metodo IProvidePropertyBuilder:: ExecuteBuilder</span><span class="sxs-lookup"><span data-stu-id="7ad7d-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="7ad7d-104">Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ad7d-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="7ad7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ad7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad7d-107">*DISPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-108">DISPID della proprietà per la quale viene visualizzato il generatore.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="7ad7d-109">*bstrGuidBldr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-110">**BSTR** del GUID del generatore da richiamare.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="7ad7d-111">Questa operazione viene restituita da [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="7ad7d-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad7d-112">*pdispApp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-113">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ad7d-114">*hwndBldrOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-115">Handle per la finestra del generatore popup padre.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="7ad7d-116">*pvarValue* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-117">Valore corrente della proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-117">The current value of the property.</span></span> <span data-ttu-id="7ad7d-118">Questo valore può essere modificato dall'oggetto e modificato nel nuovo valore se *pbActionCommitted* è **true**.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="7ad7d-119">*pbActionCommitted* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7ad7d-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad7d-120">Valore che indica se il generatore ha eseguito un'azione sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="7ad7d-121">Può essere usato quando un utente modifica qualcosa, quindi preme OK nella finestra di dialogo Generatore popup.</span><span class="sxs-lookup"><span data-stu-id="7ad7d-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad7d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ad7d-122">Return value</span></span>

<span data-ttu-id="7ad7d-123">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ad7d-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad7d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ad7d-124">Requirements</span></span>



| <span data-ttu-id="7ad7d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ad7d-125">Requirement</span></span> | <span data-ttu-id="7ad7d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ad7d-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad7d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ad7d-127">DLL</span></span><br/> | <dl> <span data-ttu-id="7ad7d-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ad7d-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad7d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ad7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad7d-130">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="7ad7d-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




