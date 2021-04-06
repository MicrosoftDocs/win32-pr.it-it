---
title: MCI_MAKE_HMS macro (Mciapi. h)
description: Il MCI \_ make \_ HMS macro crea un valore di ora in formato ore/minuti/secondi (HMS) compresso tra i valori di ore, minuti e secondi specificati.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743143"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="de0a6-104">MCI \_ make \_ HMS macro</span><span class="sxs-lookup"><span data-stu-id="de0a6-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="de0a6-105">Il **MCI \_ make \_ HMS** macro crea un valore di ora in formato ore/minuti/secondi (HMS) compresso tra i valori di ore, minuti e secondi specificati.</span><span class="sxs-lookup"><span data-stu-id="de0a6-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de0a6-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="de0a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="de0a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0a6-108">*ore*</span><span class="sxs-lookup"><span data-stu-id="de0a6-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="de0a6-109">Numero di ore.</span><span class="sxs-lookup"><span data-stu-id="de0a6-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="de0a6-110">*minuti*</span><span class="sxs-lookup"><span data-stu-id="de0a6-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="de0a6-111">Numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="de0a6-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="de0a6-112">*secondi*</span><span class="sxs-lookup"><span data-stu-id="de0a6-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="de0a6-113">Numero di secondi.</span><span class="sxs-lookup"><span data-stu-id="de0a6-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0a6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de0a6-114">Return value</span></span>

<span data-ttu-id="de0a6-115">Restituisce l'ora nel formato HMS compresso.</span><span class="sxs-lookup"><span data-stu-id="de0a6-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="de0a6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="de0a6-116">Remarks</span></span>

<span data-ttu-id="de0a6-117">L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi.</span><span class="sxs-lookup"><span data-stu-id="de0a6-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="de0a6-118">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="de0a6-118">The most significant byte is unused.</span></span>

<span data-ttu-id="de0a6-119">Il **MCI \_ make \_ HMS** macro viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="de0a6-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="de0a6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de0a6-120">Requirements</span></span>



| <span data-ttu-id="de0a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="de0a6-121">Requirement</span></span> | <span data-ttu-id="de0a6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="de0a6-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de0a6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de0a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="de0a6-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de0a6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="de0a6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de0a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="de0a6-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de0a6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="de0a6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de0a6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="de0a6-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="de0a6-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0a6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de0a6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0a6-130">MCI</span><span class="sxs-lookup"><span data-stu-id="de0a6-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="de0a6-131">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="de0a6-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





