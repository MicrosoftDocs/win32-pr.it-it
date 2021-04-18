---
description: Recupera un valore booleano denominato da un BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Funzione GetBoolFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305918"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="2b35a-103">GetBoolFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b35a-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="2b35a-104">La funzione **GetBoolFromBlob** recupera un valore booleano denominato da un BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b35a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b35a-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="2b35a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b35a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b35a-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35a-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2b35a-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35a-110">Puntatore al nome del proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="2b35a-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35a-112">Puntatore al nome della categoria BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="2b35a-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35a-114">Puntatore al nome del tag BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="2b35a-115">*pBool* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b35a-116">Puntatore al valore booleano del BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b35a-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b35a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b35a-117">Return value</span></span>

<span data-ttu-id="2b35a-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2b35a-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2b35a-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="2b35a-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b35a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b35a-120">Requirements</span></span>



| <span data-ttu-id="2b35a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b35a-121">Requirement</span></span> | <span data-ttu-id="2b35a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2b35a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b35a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b35a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b35a-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b35a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b35a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b35a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b35a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b35a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b35a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b35a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b35a-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b35a-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b35a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b35a-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b35a-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b35a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b35a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b35a-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b35a-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b35a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b35a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b35a-134">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-135">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b35a-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b35a-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




