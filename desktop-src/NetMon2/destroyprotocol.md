---
description: La funzione DestroyProtocol Elimina il protocollo creato dalla funzione CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Funzione DestroyProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227382"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="7baa5-103">DestroyProtocol (funzione)</span><span class="sxs-lookup"><span data-stu-id="7baa5-103">DestroyProtocol function</span></span>

<span data-ttu-id="7baa5-104">La funzione **DestroyProtocol** Elimina il protocollo creato dalla funzione **CreateProtocol** .</span><span class="sxs-lookup"><span data-stu-id="7baa5-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7baa5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7baa5-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7baa5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7baa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7baa5-107">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7baa5-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7baa5-108">Handle per il protocollo da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="7baa5-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7baa5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7baa5-109">Return value</span></span>

<span data-ttu-id="7baa5-110">No.</span><span class="sxs-lookup"><span data-stu-id="7baa5-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7baa5-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7baa5-111">Remarks</span></span>

<span data-ttu-id="7baa5-112">La DLL del parser chiama la funzione **DestroyProtocol** durante la relativa implementazione di [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="7baa5-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="7baa5-113">**DestroyProtocol** viene chiamato quando il sistema operativo sta per scaricare la dll.</span><span class="sxs-lookup"><span data-stu-id="7baa5-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="7baa5-114">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="7baa5-114">For information on</span></span>                                        | <span data-ttu-id="7baa5-115">Vedere</span><span class="sxs-lookup"><span data-stu-id="7baa5-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7baa5-116">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="7baa5-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="7baa5-117">Parser</span><span class="sxs-lookup"><span data-stu-id="7baa5-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="7baa5-118">Come implementare **DllMain** include un esempio.</span><span class="sxs-lookup"><span data-stu-id="7baa5-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="7baa5-119">Implementazione di DllMain</span><span class="sxs-lookup"><span data-stu-id="7baa5-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="7baa5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7baa5-120">Requirements</span></span>



| <span data-ttu-id="7baa5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7baa5-121">Requirement</span></span> | <span data-ttu-id="7baa5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7baa5-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7baa5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7baa5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7baa5-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7baa5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7baa5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7baa5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7baa5-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7baa5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7baa5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7baa5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7baa5-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7baa5-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7baa5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="7baa5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7baa5-130"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7baa5-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7baa5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7baa5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7baa5-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7baa5-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7baa5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7baa5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7baa5-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="7baa5-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




