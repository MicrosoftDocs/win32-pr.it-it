---
description: Imposta il filtro di corrispondenza del modello BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Funzione SetNPPPatternFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526749"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="7f044-103">SetNPPPatternFilterInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="7f044-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="7f044-104">La funzione **SetNPPPatternFilterInBlob** imposta il filtro di corrispondenza del modello BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f044-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f044-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f044-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="7f044-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f044-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f044-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f044-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f044-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f044-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="7f044-109">*pExpression* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f044-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f044-110">Puntatore a una struttura di [espressioni](expression.md) che definisce l'espressione di filtro da impostare.</span><span class="sxs-lookup"><span data-stu-id="7f044-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="7f044-111">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f044-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f044-112">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="7f044-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f044-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f044-113">Return value</span></span>

<span data-ttu-id="7f044-114">Se la funzione **SetNPPPatternFilterInBlob** ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7f044-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7f044-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="7f044-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f044-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f044-116">Remarks</span></span>

<span data-ttu-id="7f044-117">Il criterio di ricerca corrisponde ai dati del filtro archiviati nella categoria **config** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f044-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f044-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f044-118">Requirements</span></span>



| <span data-ttu-id="7f044-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f044-119">Requirement</span></span> | <span data-ttu-id="7f044-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7f044-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f044-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f044-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f044-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f044-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f044-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f044-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f044-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f044-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f044-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f044-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f044-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f044-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="7f044-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f044-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f044-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f044-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f044-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7f044-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f044-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f044-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f044-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f044-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f044-132">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-139">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="7f044-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="7f044-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




