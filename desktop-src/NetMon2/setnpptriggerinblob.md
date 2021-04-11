---
description: Imposta il trigger del BLOB.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Funzione SetNPPTriggerInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226237"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="a7de8-103">SetNPPTriggerInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="a7de8-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="a7de8-104">La funzione **SetNPPTriggerInBlob** imposta il trigger del BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7de8-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7de8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7de8-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a7de8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7de8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7de8-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7de8-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7de8-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7de8-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a7de8-109">*pTrigger* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7de8-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7de8-110">Puntatore al valore del trigger.</span><span class="sxs-lookup"><span data-stu-id="a7de8-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="a7de8-111">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7de8-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7de8-112">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="a7de8-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7de8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7de8-113">Return value</span></span>

<span data-ttu-id="a7de8-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a7de8-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a7de8-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="a7de8-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7de8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7de8-116">Remarks</span></span>

<span data-ttu-id="a7de8-117">I dati del trigger vengono archiviati nella categoria **trigger** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7de8-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7de8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7de8-118">Requirements</span></span>



| <span data-ttu-id="a7de8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7de8-119">Requirement</span></span> | <span data-ttu-id="a7de8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a7de8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7de8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7de8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7de8-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7de8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7de8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7de8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7de8-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7de8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7de8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7de8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7de8-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7de8-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a7de8-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7de8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7de8-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7de8-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a7de8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a7de8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7de8-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7de8-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7de8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7de8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7de8-132">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-139">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="a7de8-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="a7de8-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




