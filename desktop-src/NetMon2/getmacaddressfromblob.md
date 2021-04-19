---
description: La funzione GetMacAddressFromBlob recupera l'indirizzo MAC denominato da un BLOB.
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: Funzione GetMacAddressFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317749"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="4f247-103">GetMacAddressFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f247-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="4f247-104">La funzione **GetMacAddressFromBlob** recupera l'indirizzo Mac denominato da un BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f247-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f247-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="4f247-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f247-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f247-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f247-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f247-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4f247-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f247-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f247-110">Puntatore al nome del proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="4f247-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f247-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f247-112">Puntatore al nome della categoria BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="4f247-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f247-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f247-114">Puntatore al nome del tag BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="4f247-115">*pMacAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f247-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f247-116">Puntatore all'indirizzo MAC del BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f247-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f247-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f247-117">Return value</span></span>

<span data-ttu-id="4f247-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4f247-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4f247-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="4f247-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f247-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f247-120">Requirements</span></span>



| <span data-ttu-id="4f247-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f247-121">Requirement</span></span> | <span data-ttu-id="4f247-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4f247-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f247-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f247-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4f247-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f247-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4f247-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f247-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4f247-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f247-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f247-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f247-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f247-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f247-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4f247-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f247-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f247-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f247-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4f247-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4f247-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f247-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f247-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f247-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f247-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f247-134">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-137">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="4f247-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="4f247-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




