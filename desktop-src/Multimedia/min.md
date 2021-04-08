---
title: macro min (Minwindef. h)
description: La macro min Confronta due valori e restituisce quello più piccolo. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macro Windows Multimedia
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743927"
---
# <a name="min-macro"></a><span data-ttu-id="9f577-106">min (macro)</span><span class="sxs-lookup"><span data-stu-id="9f577-106">min macro</span></span>

<span data-ttu-id="9f577-107">La macro **min** Confronta due valori e restituisce quello più piccolo.</span><span class="sxs-lookup"><span data-stu-id="9f577-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="9f577-108">Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno.</span><span class="sxs-lookup"><span data-stu-id="9f577-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="9f577-109">Il tipo di dati degli argomenti e il valore restituito sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="9f577-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f577-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f577-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="9f577-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f577-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f577-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="9f577-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="9f577-113">Specifica il primo di due valori.</span><span class="sxs-lookup"><span data-stu-id="9f577-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="9f577-114">*Value2*</span><span class="sxs-lookup"><span data-stu-id="9f577-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="9f577-115">Specifica il secondo di due valori.</span><span class="sxs-lookup"><span data-stu-id="9f577-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f577-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f577-116">Return value</span></span>

<span data-ttu-id="9f577-117">Il valore restituito è il più piccolo dei due valori specificati.</span><span class="sxs-lookup"><span data-stu-id="9f577-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f577-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f577-118">Remarks</span></span>

<span data-ttu-id="9f577-119">La macro **min** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="9f577-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="9f577-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f577-120">Requirements</span></span>



| <span data-ttu-id="9f577-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f577-121">Requirement</span></span> | <span data-ttu-id="9f577-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9f577-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f577-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f577-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f577-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f577-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9f577-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f577-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f577-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f577-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f577-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f577-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f577-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f577-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





