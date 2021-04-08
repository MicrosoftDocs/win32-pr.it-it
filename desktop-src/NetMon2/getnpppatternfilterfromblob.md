---
description: La funzione GetNPPPatternFilterFromBlob Recupera il filtro di corrispondenza dei criteri da un BLOB specifico.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Funzione GetNPPPatternFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750082"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="08fa4-103">GetNPPPatternFilterFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="08fa4-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="08fa4-104">La funzione **GetNPPPatternFilterFromBlob** Recupera il filtro di corrispondenza dei criteri da un blob specifico.</span><span class="sxs-lookup"><span data-stu-id="08fa4-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="08fa4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08fa4-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="08fa4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08fa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08fa4-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08fa4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08fa4-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="08fa4-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="08fa4-109">*pExpression* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08fa4-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08fa4-110">Puntatore all'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="08fa4-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="08fa4-111">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="08fa4-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08fa4-112">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="08fa4-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08fa4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08fa4-113">Return value</span></span>

<span data-ttu-id="08fa4-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="08fa4-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="08fa4-115">Se la funzione ha esito negativo, il valore restituito è un NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="08fa4-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="08fa4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="08fa4-116">Remarks</span></span>

<span data-ttu-id="08fa4-117">Le informazioni sul filtro per la corrispondenza dei criteri vengono archiviate nella categoria **config** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="08fa4-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="08fa4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08fa4-118">Requirements</span></span>



| <span data-ttu-id="08fa4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08fa4-119">Requirement</span></span> | <span data-ttu-id="08fa4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="08fa4-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08fa4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08fa4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08fa4-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="08fa4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08fa4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08fa4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08fa4-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="08fa4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08fa4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08fa4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08fa4-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08fa4-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="08fa4-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="08fa4-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="08fa4-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08fa4-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="08fa4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="08fa4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08fa4-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08fa4-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08fa4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08fa4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08fa4-132">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-138">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="08fa4-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="08fa4-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




