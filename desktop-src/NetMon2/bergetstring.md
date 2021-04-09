---
description: La funzione BERGetString decodifica una stringa con codifica BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Funzione BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881449"
---
# <a name="bergetstring-function"></a><span data-ttu-id="86eab-103">BERGetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="86eab-103">BERGetString function</span></span>

<span data-ttu-id="86eab-104">La funzione **BERGetString** decodifica una stringa con codifica BER.</span><span class="sxs-lookup"><span data-stu-id="86eab-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="86eab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86eab-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="86eab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86eab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86eab-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="86eab-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="86eab-108">Puntatore alla stringa decodificata.</span><span class="sxs-lookup"><span data-stu-id="86eab-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="86eab-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="86eab-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="86eab-110">Puntatore al puntatore della stringa decodificata.</span><span class="sxs-lookup"><span data-stu-id="86eab-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="86eab-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="86eab-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="86eab-112">Puntatore alla lunghezza dell'intestazione restituita.</span><span class="sxs-lookup"><span data-stu-id="86eab-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="86eab-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="86eab-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="86eab-114">Puntatore alla lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="86eab-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="86eab-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="86eab-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="86eab-116">Puntatore al puntatore della voce BER successiva.</span><span class="sxs-lookup"><span data-stu-id="86eab-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86eab-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86eab-117">Return value</span></span>

<span data-ttu-id="86eab-118">Se la funzione ha esito positivo (ovvero se una stringa con codifica BER valida è decodificata), il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="86eab-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="86eab-119">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="86eab-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="86eab-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86eab-120">Requirements</span></span>



| <span data-ttu-id="86eab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="86eab-121">Requirement</span></span> | <span data-ttu-id="86eab-122">Valore</span><span class="sxs-lookup"><span data-stu-id="86eab-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86eab-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86eab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86eab-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86eab-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="86eab-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86eab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86eab-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86eab-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86eab-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86eab-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="86eab-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="86eab-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="86eab-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="86eab-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="86eab-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86eab-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="86eab-131">DLL</span><span class="sxs-lookup"><span data-stu-id="86eab-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86eab-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86eab-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




