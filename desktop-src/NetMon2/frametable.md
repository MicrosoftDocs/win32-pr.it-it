---
description: La struttura FRAMETABLE, un buffer circolare di puntatori ai frame, viene restituita alle applicazioni collegate all'interfaccia ITRC dell'oggetto NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Struttura FRAMETABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128351"
---
# <a name="frametable-structure"></a><span data-ttu-id="54e31-103">Struttura FRAMETABLE</span><span class="sxs-lookup"><span data-stu-id="54e31-103">FRAMETABLE structure</span></span>

<span data-ttu-id="54e31-104">La struttura **Frametable** , un buffer circolare di puntatori ai frame, viene restituita alle applicazioni collegate all'interfaccia **itrc** dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="54e31-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54e31-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="54e31-106">Members</span><span class="sxs-lookup"><span data-stu-id="54e31-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="54e31-107">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="54e31-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="54e31-108">Lunghezza totale della tabella.</span><span class="sxs-lookup"><span data-stu-id="54e31-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="54e31-109">**StartIndex**</span><span class="sxs-lookup"><span data-stu-id="54e31-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="54e31-110">Primo indice all'interno della tabella.</span><span class="sxs-lookup"><span data-stu-id="54e31-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="54e31-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="54e31-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="54e31-112">Ultimo indice all'interno della tabella.</span><span class="sxs-lookup"><span data-stu-id="54e31-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="54e31-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="54e31-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="54e31-114">Numero di frame descritti da questa tabella.</span><span class="sxs-lookup"><span data-stu-id="54e31-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="54e31-115">**Frame**</span><span class="sxs-lookup"><span data-stu-id="54e31-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="54e31-116">Matrice effettiva di descrittori di frame.</span><span class="sxs-lookup"><span data-stu-id="54e31-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54e31-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54e31-117">Requirements</span></span>



| <span data-ttu-id="54e31-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e31-118">Requirement</span></span> | <span data-ttu-id="54e31-119">Valore</span><span class="sxs-lookup"><span data-stu-id="54e31-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54e31-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e31-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54e31-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54e31-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="54e31-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e31-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54e31-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54e31-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="54e31-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54e31-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e31-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e31-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




