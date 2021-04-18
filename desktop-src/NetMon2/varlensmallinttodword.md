---
description: La funzione VarLenSmallIntToDword converte un valore integer di lunghezza variabile, piccolo, in un valore DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Funzione VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310785"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="080b1-103">VarLenSmallIntToDword (funzione)</span><span class="sxs-lookup"><span data-stu-id="080b1-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="080b1-104">La funzione **VarLenSmallIntToDword** converte un valore integer di lunghezza variabile, piccolo, in un valore **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="080b1-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="080b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="080b1-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="080b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="080b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="080b1-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="080b1-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="080b1-108">Puntatore al valore integer a lunghezza variabile, piccolo.</span><span class="sxs-lookup"><span data-stu-id="080b1-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="080b1-109">*ValueLen*</span><span class="sxs-lookup"><span data-stu-id="080b1-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="080b1-110">Lunghezza (in byte) dell'intero piccolo a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="080b1-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="080b1-111">*fIsByteswapped*</span><span class="sxs-lookup"><span data-stu-id="080b1-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="080b1-112">Flag che indica se la lunghezza della variabile Small Integer è scambio di byte.</span><span class="sxs-lookup"><span data-stu-id="080b1-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="080b1-113">*lpDword*</span><span class="sxs-lookup"><span data-stu-id="080b1-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="080b1-114">**DWORD** in cui viene convertito il valore integer.</span><span class="sxs-lookup"><span data-stu-id="080b1-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="080b1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="080b1-115">Return value</span></span>

<span data-ttu-id="080b1-116">Il valore restituito è un puntatore a **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="080b1-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="080b1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="080b1-117">Requirements</span></span>



| <span data-ttu-id="080b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="080b1-118">Requirement</span></span> | <span data-ttu-id="080b1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="080b1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="080b1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="080b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="080b1-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="080b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="080b1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="080b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="080b1-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="080b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="080b1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="080b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="080b1-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="080b1-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="080b1-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="080b1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="080b1-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="080b1-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="080b1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="080b1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080b1-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="080b1-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




