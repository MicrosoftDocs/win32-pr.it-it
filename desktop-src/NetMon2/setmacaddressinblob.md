---
description: La funzione SetMacAddressInBlob imposta l'indirizzo MAC richiesto di un BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Funzione SetMacAddressInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883342"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="e31f1-103">SetMacAddressInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="e31f1-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="e31f1-104">La funzione **SetMacAddressInBlob** imposta l'indirizzo Mac richiesto di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="e31f1-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e31f1-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="e31f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e31f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31f1-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f1-108">Handle per il BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="e31f1-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="e31f1-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f1-110">Puntatore al nome del **proprietario** del BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="e31f1-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e31f1-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f1-112">Puntatore al nome della **categoria** BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="e31f1-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e31f1-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f1-114">Puntatore al nome del **tag** BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="e31f1-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e31f1-115">*pMacAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f1-116">Puntatore all'indirizzo MAC del BLOB da impostare.</span><span class="sxs-lookup"><span data-stu-id="e31f1-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31f1-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e31f1-117">Return value</span></span>

<span data-ttu-id="e31f1-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e31f1-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e31f1-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="e31f1-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31f1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e31f1-120">Requirements</span></span>



| <span data-ttu-id="e31f1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31f1-121">Requirement</span></span> | <span data-ttu-id="e31f1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e31f1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e31f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e31f1-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e31f1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e31f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e31f1-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e31f1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e31f1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e31f1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31f1-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e31f1-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e31f1-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e31f1-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e31f1-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e31f1-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e31f1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e31f1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31f1-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31f1-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31f1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e31f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31f1-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-137">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="e31f1-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="e31f1-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




