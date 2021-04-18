---
title: MCI_MAKE_TMSF macro (Mciapi. h)
description: La \_ macro MCI make \_ TMSF crea un valore di ora in formato tracce/minuti/secondi/frame (TMSF) compresso dai valori di tracce, minuti, secondi e frame specificati.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302630"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="80fdf-104">MCI \_ make \_ TMSF (macro)</span><span class="sxs-lookup"><span data-stu-id="80fdf-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="80fdf-105">La macro **MCI \_ make \_ TMSF** crea un valore di ora in formato tracce/minuti/secondi/frame (TMSF) compresso dai valori di tracce, minuti, secondi e frame specificati.</span><span class="sxs-lookup"><span data-stu-id="80fdf-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fdf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80fdf-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="80fdf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="80fdf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80fdf-108">*brani*</span><span class="sxs-lookup"><span data-stu-id="80fdf-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="80fdf-109">Numero di tracce.</span><span class="sxs-lookup"><span data-stu-id="80fdf-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="80fdf-110">*minuti*</span><span class="sxs-lookup"><span data-stu-id="80fdf-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="80fdf-111">Numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="80fdf-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="80fdf-112">*secondi*</span><span class="sxs-lookup"><span data-stu-id="80fdf-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="80fdf-113">Numero di secondi.</span><span class="sxs-lookup"><span data-stu-id="80fdf-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="80fdf-114">*frame*</span><span class="sxs-lookup"><span data-stu-id="80fdf-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="80fdf-115">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="80fdf-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80fdf-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80fdf-116">Return value</span></span>

<span data-ttu-id="80fdf-117">Restituisce l'ora nel formato TMSF compresso.</span><span class="sxs-lookup"><span data-stu-id="80fdf-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="80fdf-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="80fdf-118">Remarks</span></span>

<span data-ttu-id="80fdf-119">L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="80fdf-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="80fdf-120">La macro **MCI \_ make \_ TMSF** è definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="80fdf-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="80fdf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80fdf-121">Requirements</span></span>



| <span data-ttu-id="80fdf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80fdf-122">Requirement</span></span> | <span data-ttu-id="80fdf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="80fdf-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80fdf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80fdf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80fdf-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80fdf-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="80fdf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80fdf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80fdf-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80fdf-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="80fdf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80fdf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="80fdf-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80fdf-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80fdf-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80fdf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fdf-131">MCI</span><span class="sxs-lookup"><span data-stu-id="80fdf-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="80fdf-132">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="80fdf-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





