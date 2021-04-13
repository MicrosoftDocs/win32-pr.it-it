---
description: La funzione SetBoolInBlob imposta un valore booleano in una determinata posizione all'interno di un BLOB.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Funzione SetBoolInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528639"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="7bf88-103">SetBoolInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="7bf88-103">SetBoolInBlob function</span></span>

<span data-ttu-id="7bf88-104">La funzione **SetBoolInBlob** imposta un valore booleano in una determinata posizione all'interno di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bf88-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bf88-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="7bf88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bf88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf88-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf88-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bf88-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="7bf88-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf88-110">Puntatore al nome del **proprietario** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bf88-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="7bf88-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf88-112">Puntatore al nome della **categoria** BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bf88-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="7bf88-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf88-114">Puntatore al nome del **tag** BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bf88-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="7bf88-115">*Bool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf88-116">Valore booleano impostato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7bf88-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf88-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bf88-117">Return value</span></span>

<span data-ttu-id="7bf88-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7bf88-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7bf88-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="7bf88-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf88-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bf88-120">Requirements</span></span>



| <span data-ttu-id="7bf88-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf88-121">Requirement</span></span> | <span data-ttu-id="7bf88-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf88-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf88-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bf88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf88-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7bf88-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bf88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf88-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bf88-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7bf88-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bf88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf88-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf88-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="7bf88-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bf88-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bf88-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bf88-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="7bf88-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7bf88-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bf88-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bf88-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf88-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bf88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf88-134">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-135">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="7bf88-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="7bf88-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




