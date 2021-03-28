---
description: Questa classe è la classe del tipo di evento per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: Classe PageFault_TransitionFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883069"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="5d700-104">\_Classe pagefault TransitionFault</span><span class="sxs-lookup"><span data-stu-id="5d700-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="5d700-105">Questa classe è la classe del tipo di evento per gli eventi di errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="5d700-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="5d700-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="5d700-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d700-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d700-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="5d700-108">Members</span><span class="sxs-lookup"><span data-stu-id="5d700-108">Members</span></span>

<span data-ttu-id="5d700-109">La **classe \_ TransitionFault di pagefault** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5d700-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="5d700-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5d700-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d700-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5d700-111">Properties</span></span>

<span data-ttu-id="5d700-112">La **classe \_ TransitionFault di pagefault** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d700-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d700-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="5d700-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d700-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d700-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d700-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5d700-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d700-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="5d700-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5d700-117">Puntatore all'istruzione corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5d700-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="5d700-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="5d700-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d700-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d700-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d700-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5d700-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d700-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="5d700-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5d700-122">Indirizzo virtuale della pagina che ha causato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="5d700-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d700-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d700-123">Requirements</span></span>



| <span data-ttu-id="5d700-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d700-124">Requirement</span></span> | <span data-ttu-id="5d700-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5d700-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5d700-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d700-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5d700-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d700-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d700-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d700-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5d700-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d700-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5d700-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d700-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d700-131">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="5d700-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




