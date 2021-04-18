---
description: La funzione SetDwordInBlob imposta il valore DWORD denominato di un BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Funzione SetDwordInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310489"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="40ded-103">SetDwordInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="40ded-103">SetDwordInBlob function</span></span>

<span data-ttu-id="40ded-104">La funzione **SetDwordInBlob** imposta il valore **DWORD** denominato di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="40ded-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ded-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40ded-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="40ded-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ded-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ded-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ded-108">Handle per un BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="40ded-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="40ded-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ded-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ded-110">Puntatore al nome del **proprietario** del BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="40ded-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="40ded-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ded-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ded-112">Puntatore al nome della **categoria** BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="40ded-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="40ded-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ded-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ded-114">Puntatore al nome del **tag** BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="40ded-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="40ded-115">*DWORD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ded-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ded-116">Valore **DWORD** del BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="40ded-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ded-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40ded-117">Return value</span></span>

<span data-ttu-id="40ded-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="40ded-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="40ded-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="40ded-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ded-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40ded-120">Requirements</span></span>



| <span data-ttu-id="40ded-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="40ded-121">Requirement</span></span> | <span data-ttu-id="40ded-122">Valore</span><span class="sxs-lookup"><span data-stu-id="40ded-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ded-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ded-123">Minimum supported client</span></span><br/> | <span data-ttu-id="40ded-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40ded-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="40ded-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ded-125">Minimum supported server</span></span><br/> | <span data-ttu-id="40ded-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40ded-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40ded-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40ded-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ded-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="40ded-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="40ded-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="40ded-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="40ded-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40ded-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="40ded-131">DLL</span><span class="sxs-lookup"><span data-stu-id="40ded-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ded-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ded-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ded-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40ded-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ded-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="40ded-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="40ded-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




