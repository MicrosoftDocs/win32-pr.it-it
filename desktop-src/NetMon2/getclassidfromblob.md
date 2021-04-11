---
description: La funzione GetClassIDFromBlob recupera un valore di identificatore di classe denominato da un BLOB.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Funzione GetClassIDFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128343"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="74065-103">GetClassIDFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="74065-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="74065-104">La funzione **GetClassIDFromBlob** recupera un valore di identificatore di classe denominato da un BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="74065-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74065-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="74065-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74065-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74065-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74065-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="74065-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74065-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74065-110">Puntatore al nome del proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="74065-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74065-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74065-112">Puntatore al nome della categoria BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="74065-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74065-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74065-114">Puntatore al nome del tag BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="74065-115">*pClsID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74065-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74065-116">Puntatore all'identificatore di classe BLOB.</span><span class="sxs-lookup"><span data-stu-id="74065-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74065-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74065-117">Return value</span></span>

<span data-ttu-id="74065-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="74065-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="74065-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="74065-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="74065-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74065-120">Requirements</span></span>



| <span data-ttu-id="74065-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="74065-121">Requirement</span></span> | <span data-ttu-id="74065-122">Valore</span><span class="sxs-lookup"><span data-stu-id="74065-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74065-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74065-123">Minimum supported client</span></span><br/> | <span data-ttu-id="74065-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74065-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74065-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74065-125">Minimum supported server</span></span><br/> | <span data-ttu-id="74065-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74065-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74065-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74065-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="74065-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="74065-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="74065-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="74065-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="74065-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74065-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="74065-131">DLL</span><span class="sxs-lookup"><span data-stu-id="74065-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74065-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74065-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74065-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74065-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74065-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="74065-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="74065-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="74065-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="74065-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




