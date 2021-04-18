---
title: macro max (Minwindef. h)
description: La macro max Confronta due valori e restituisce quello più grande. Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Max macro Windows Multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517632"
---
# <a name="max-macro"></a><span data-ttu-id="b1bf2-106">max (macro)</span><span class="sxs-lookup"><span data-stu-id="b1bf2-106">max macro</span></span>

<span data-ttu-id="b1bf2-107">La macro **Max** Confronta due valori e restituisce quello più grande.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="b1bf2-108">Il tipo di dati può essere qualsiasi tipo di dati numerico, con segno o senza segno.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="b1bf2-109">Il tipo di dati degli argomenti e il valore restituito sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bf2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1bf2-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="b1bf2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1bf2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bf2-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="b1bf2-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="b1bf2-113">Specifica il primo di due valori.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="b1bf2-114">*Value2*</span><span class="sxs-lookup"><span data-stu-id="b1bf2-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="b1bf2-115">Specifica il secondo di due valori.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bf2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1bf2-116">Return value</span></span>

<span data-ttu-id="b1bf2-117">Il valore restituito è il maggiore dei due valori specificati.</span><span class="sxs-lookup"><span data-stu-id="b1bf2-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1bf2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1bf2-118">Remarks</span></span>

<span data-ttu-id="b1bf2-119">La macro **Max** è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="b1bf2-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="b1bf2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1bf2-120">Requirements</span></span>



| <span data-ttu-id="b1bf2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1bf2-121">Requirement</span></span> | <span data-ttu-id="b1bf2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b1bf2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bf2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bf2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bf2-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1bf2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b1bf2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bf2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bf2-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1bf2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b1bf2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1bf2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1bf2-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bf2-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





