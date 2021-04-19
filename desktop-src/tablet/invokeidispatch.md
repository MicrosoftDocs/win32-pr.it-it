---
description: Richiama la funzionalità helper per l'interfaccia IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313923"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="e4591-103">InvokeIDispatch (funzione)</span><span class="sxs-lookup"><span data-stu-id="e4591-103">InvokeIDispatch function</span></span>

<span data-ttu-id="e4591-104">Richiama la funzionalità helper per l'interfaccia IDispatch.</span><span class="sxs-lookup"><span data-stu-id="e4591-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="e4591-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4591-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4591-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4591-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="e4591-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4591-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4591-108">*pDispatch*</span><span class="sxs-lookup"><span data-stu-id="e4591-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="e4591-109">Istanza dell'interfaccia IDispatch.</span><span class="sxs-lookup"><span data-stu-id="e4591-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="e4591-110">*DISPID*</span><span class="sxs-lookup"><span data-stu-id="e4591-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="e4591-111">Metodo, proprietà o argomento da passare.</span><span class="sxs-lookup"><span data-stu-id="e4591-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="e4591-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="e4591-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="e4591-113">Parametri da passare.</span><span class="sxs-lookup"><span data-stu-id="e4591-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="e4591-114">*pvarResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4591-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4591-115">Struttura che riceve i valori recuperati.</span><span class="sxs-lookup"><span data-stu-id="e4591-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4591-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4591-116">Return value</span></span>

<span data-ttu-id="e4591-117">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4591-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e4591-118">Se ha esito negativo, i codici restituiti possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e4591-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="e4591-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4591-119">Return code</span></span>                                                                                  | <span data-ttu-id="e4591-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4591-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="e4591-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4591-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e4591-122">Il valore di *pDispatch* non è valido.</span><span class="sxs-lookup"><span data-stu-id="e4591-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4591-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4591-123">Requirements</span></span>



| <span data-ttu-id="e4591-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4591-124">Requirement</span></span> | <span data-ttu-id="e4591-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e4591-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4591-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4591-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4591-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e4591-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e4591-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4591-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4591-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e4591-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e4591-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4591-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4591-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4591-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




