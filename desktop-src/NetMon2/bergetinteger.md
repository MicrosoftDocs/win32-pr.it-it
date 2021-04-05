---
description: La funzione BERGetInteger decodifica un valore integer con codifica BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Funzione BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883670"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="be416-103">BERGetInteger (funzione)</span><span class="sxs-lookup"><span data-stu-id="be416-103">BERGetInteger function</span></span>

<span data-ttu-id="be416-104">La funzione **BERGetInteger** decodifica un valore integer con codifica BER.</span><span class="sxs-lookup"><span data-stu-id="be416-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="be416-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be416-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="be416-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be416-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="be416-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="be416-108">Puntatore all'integer decodificato.</span><span class="sxs-lookup"><span data-stu-id="be416-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="be416-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="be416-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="be416-110">Puntatore al puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="be416-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="be416-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="be416-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="be416-112">Puntatore alla lunghezza dell'intestazione restituita.</span><span class="sxs-lookup"><span data-stu-id="be416-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="be416-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="be416-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="be416-114">Puntatore alla lunghezza dei dati.</span><span class="sxs-lookup"><span data-stu-id="be416-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="be416-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="be416-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="be416-116">Puntatore al puntatore alla voce BER successiva.</span><span class="sxs-lookup"><span data-stu-id="be416-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be416-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be416-117">Return value</span></span>

<span data-ttu-id="be416-118">Se la funzione ha esito positivo, ovvero se viene trovato e convertito un intero con codifica BER valido, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="be416-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="be416-119">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="be416-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="be416-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be416-120">Requirements</span></span>



| <span data-ttu-id="be416-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="be416-121">Requirement</span></span> | <span data-ttu-id="be416-122">Valore</span><span class="sxs-lookup"><span data-stu-id="be416-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be416-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be416-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be416-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be416-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="be416-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be416-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be416-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be416-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be416-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be416-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be416-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be416-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="be416-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="be416-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="be416-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be416-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="be416-131">DLL</span><span class="sxs-lookup"><span data-stu-id="be416-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be416-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be416-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




