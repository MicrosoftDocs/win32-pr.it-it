---
description: La funzione BERGetHeader decodifica un'intestazione Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Funzione BERGetHeader (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311641"
---
# <a name="bergetheader-function"></a><span data-ttu-id="d7d35-103">BERGetHeader (funzione)</span><span class="sxs-lookup"><span data-stu-id="d7d35-103">BERGetHeader function</span></span>

<span data-ttu-id="d7d35-104">La funzione **BERGetHeader** decodifica un'intestazione Choice.</span><span class="sxs-lookup"><span data-stu-id="d7d35-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7d35-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="d7d35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7d35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d35-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="d7d35-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d35-108">Puntatore all'intestazione Choice.</span><span class="sxs-lookup"><span data-stu-id="d7d35-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="d7d35-109">*pTag*</span><span class="sxs-lookup"><span data-stu-id="d7d35-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d35-110">Puntatore al tag restituito.</span><span class="sxs-lookup"><span data-stu-id="d7d35-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="d7d35-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="d7d35-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d35-112">Puntatore alla lunghezza dell'intestazione restituita.</span><span class="sxs-lookup"><span data-stu-id="d7d35-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="d7d35-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="d7d35-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d35-114">Puntatore alla lunghezza dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="d7d35-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="d7d35-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="d7d35-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d35-116">Puntatore al contenuto dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="d7d35-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d35-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7d35-117">Return value</span></span>

<span data-ttu-id="d7d35-118">Se la funzione ha esito positivo, ovvero viene trovata un'intestazione Choice BER valida, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d7d35-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="d7d35-119">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d7d35-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7d35-120">Requirements</span></span>



| <span data-ttu-id="d7d35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d35-121">Requirement</span></span> | <span data-ttu-id="d7d35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d7d35-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d35-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7d35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d35-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7d35-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d7d35-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7d35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d35-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7d35-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7d35-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7d35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d35-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d35-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7d35-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7d35-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7d35-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7d35-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7d35-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d35-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d35-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d35-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




