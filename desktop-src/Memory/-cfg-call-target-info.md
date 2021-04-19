---
description: Rappresenta le informazioni sulle destinazioni di chiamata per la protezione del flusso di controllo (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Struttura CFG_CALL_TARGET_INFO (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311746"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="d3078-103">\_Struttura delle \_ informazioni di destinazione della chiamata cfg \_</span><span class="sxs-lookup"><span data-stu-id="d3078-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="d3078-104">Rappresenta le informazioni sulle destinazioni di chiamata per la protezione del flusso di controllo (CFG).</span><span class="sxs-lookup"><span data-stu-id="d3078-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3078-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3078-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="d3078-106">Members</span><span class="sxs-lookup"><span data-stu-id="d3078-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3078-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d3078-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="d3078-108">Offset relativo a un indirizzo virtuale (iniziale) fornito.</span><span class="sxs-lookup"><span data-stu-id="d3078-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="d3078-109">Questo offset deve essere allineato a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="d3078-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="d3078-110">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d3078-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d3078-111">Flag che descrivono l'operazione da eseguire sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="d3078-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="d3078-112">Se è impostata la **\_ destinazione della chiamata cfg \_ \_ valida** , l'indirizzo verrà contrassegnato come valido per cfg.</span><span class="sxs-lookup"><span data-stu-id="d3078-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="d3078-113">In caso contrario, verrà contrassegnata come destinazione di chiamata non valida.</span><span class="sxs-lookup"><span data-stu-id="d3078-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3078-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3078-114">Requirements</span></span>



| <span data-ttu-id="d3078-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3078-115">Requirement</span></span> | <span data-ttu-id="d3078-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3078-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3078-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3078-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3078-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d3078-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d3078-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3078-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3078-120">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="d3078-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3078-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3078-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3078-122"><dt>Ntmmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3078-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




