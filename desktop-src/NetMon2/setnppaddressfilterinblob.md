---
description: La funzione SetNPPAddressFilterInBlob imposta il filtro degli indirizzi specificato nel BLOB.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Funzione SetNPPAddressFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318642"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="69ee8-103">SetNPPAddressFilterInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="69ee8-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="69ee8-104">La funzione **SetNPPAddressFilterInBlob** imposta il filtro degli indirizzi specificato nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="69ee8-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ee8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69ee8-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="69ee8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69ee8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ee8-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69ee8-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ee8-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="69ee8-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="69ee8-109">*pAddressTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69ee8-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ee8-110">Puntatore a una struttura [**ADDRESSTABLE**](addresstable.md) che definisce la tabella degli indirizzi allocata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="69ee8-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ee8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69ee8-111">Return value</span></span>

<span data-ttu-id="69ee8-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="69ee8-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="69ee8-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="69ee8-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ee8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69ee8-114">Requirements</span></span>



| <span data-ttu-id="69ee8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ee8-115">Requirement</span></span> | <span data-ttu-id="69ee8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="69ee8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69ee8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69ee8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69ee8-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69ee8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="69ee8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69ee8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69ee8-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69ee8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69ee8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69ee8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69ee8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ee8-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="69ee8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="69ee8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="69ee8-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69ee8-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="69ee8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="69ee8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69ee8-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69ee8-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ee8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69ee8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ee8-128">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-133">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="69ee8-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="69ee8-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




