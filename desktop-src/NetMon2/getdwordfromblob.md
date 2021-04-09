---
description: La funzione GetDwordFromBlob Recupera il valore DWORD denominato da un BLOB.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: Funzione GetDwordFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128339"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="c15c2-103">GetDwordFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="c15c2-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="c15c2-104">La funzione **GetDwordFromBlob** Recupera il valore **DWORD** denominato da un BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c15c2-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="c15c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c15c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c15c2-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15c2-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c15c2-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15c2-110">Puntatore al nome del proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="c15c2-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15c2-112">Puntatore al nome della categoria BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="c15c2-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15c2-114">Puntatore al nome del tag BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="c15c2-115">*pDword* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c15c2-116">Puntatore al valore **DWORD** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="c15c2-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c15c2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c15c2-117">Return value</span></span>

<span data-ttu-id="c15c2-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c15c2-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c15c2-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="c15c2-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15c2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c15c2-120">Requirements</span></span>



| <span data-ttu-id="c15c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c15c2-121">Requirement</span></span> | <span data-ttu-id="c15c2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c15c2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c15c2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c15c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c15c2-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c15c2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c15c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c15c2-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c15c2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c15c2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c15c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c15c2-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c15c2-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c15c2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c15c2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c15c2-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c15c2-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c15c2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c15c2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c15c2-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c15c2-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15c2-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c15c2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15c2-134">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="c15c2-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="c15c2-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




