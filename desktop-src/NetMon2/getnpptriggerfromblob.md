---
description: La funzione GetNPPTriggerFromBlob Recupera il trigger dal BLOB specificato.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Funzione GetNPPTriggerFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305901"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="ef5be-103">GetNPPTriggerFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="ef5be-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="ef5be-104">La funzione **GetNPPTriggerFromBlob** Recupera il trigger dal blob specificato.</span><span class="sxs-lookup"><span data-stu-id="ef5be-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef5be-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="ef5be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef5be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef5be-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef5be-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef5be-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="ef5be-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="ef5be-109">*pTrigger* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef5be-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef5be-110">Puntatore al valore del trigger.</span><span class="sxs-lookup"><span data-stu-id="ef5be-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="ef5be-111">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef5be-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef5be-112">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="ef5be-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef5be-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef5be-113">Return value</span></span>

<span data-ttu-id="ef5be-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ef5be-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ef5be-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ef5be-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef5be-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef5be-116">Remarks</span></span>

<span data-ttu-id="ef5be-117">Le informazioni sul trigger sono archiviate nella categoria **trigger** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ef5be-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef5be-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef5be-118">Requirements</span></span>



| <span data-ttu-id="ef5be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef5be-119">Requirement</span></span> | <span data-ttu-id="ef5be-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ef5be-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5be-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef5be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef5be-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef5be-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ef5be-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef5be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef5be-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef5be-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef5be-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef5be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef5be-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef5be-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ef5be-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef5be-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef5be-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef5be-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef5be-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ef5be-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef5be-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef5be-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef5be-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef5be-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef5be-132">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-133">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-135">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-136">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-137">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-139">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="ef5be-140">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="ef5be-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




