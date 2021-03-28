---
description: Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).
title: Funzione di callback MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966876"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="17c53-103">Funzione di callback MRUCMPPROC</span><span class="sxs-lookup"><span data-stu-id="17c53-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="17c53-104">Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="17c53-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17c53-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="17c53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c53-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="17c53-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="17c53-108">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="17c53-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="17c53-109">Prima stringa.</span><span class="sxs-lookup"><span data-stu-id="17c53-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="17c53-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="17c53-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="17c53-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="17c53-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="17c53-112">Seconda stringa da confrontare con la prima.</span><span class="sxs-lookup"><span data-stu-id="17c53-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c53-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17c53-113">Return value</span></span>

<span data-ttu-id="17c53-114">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="17c53-114">Type: **int**</span></span>

<span data-ttu-id="17c53-115">Restituisce 0 se gli elementi sono identici, altrimenti un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="17c53-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c53-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="17c53-116">Remarks</span></span>

<span data-ttu-id="17c53-117">Questa funzione può essere specificata facoltativamente per l'uso nella struttura [**MRUINFO**](mruinfo.md) passata a [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="17c53-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="17c53-118">Questa operazione è utile quando l'elenco MRU è stato creato con il flag **\_ binario MRU** .</span><span class="sxs-lookup"><span data-stu-id="17c53-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="17c53-119">Quando questa funzione non viene specificata, vengono utilizzate le funzioni di confronto di stringhe standard.</span><span class="sxs-lookup"><span data-stu-id="17c53-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c53-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17c53-120">Requirements</span></span>



| <span data-ttu-id="17c53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c53-121">Requirement</span></span> | <span data-ttu-id="17c53-122">Valore</span><span class="sxs-lookup"><span data-stu-id="17c53-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="17c53-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17c53-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17c53-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17c53-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="17c53-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17c53-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17c53-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17c53-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="17c53-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="17c53-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="17c53-128">**MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="17c53-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




