---
description: 'PageFault_TransitionFault classe: questa classe è la classe del tipo di evento per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault classe
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
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106459"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="265d3-104">Classe PageFault \_ TransitionFault</span><span class="sxs-lookup"><span data-stu-id="265d3-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="265d3-105">Questa classe è la classe del tipo di evento per gli eventi di errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="265d3-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="265d3-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="265d3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="265d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="265d3-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="265d3-108">Members</span><span class="sxs-lookup"><span data-stu-id="265d3-108">Members</span></span>

<span data-ttu-id="265d3-109">La **classe PageFault \_ TransitionFault** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="265d3-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="265d3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="265d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="265d3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="265d3-111">Properties</span></span>

<span data-ttu-id="265d3-112">La **classe PageFault \_ TransitionFault** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="265d3-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="265d3-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="265d3-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265d3-114">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="265d3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="265d3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="265d3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265d3-116">Qualificatori: WmiDataId(2), Puntatore</span><span class="sxs-lookup"><span data-stu-id="265d3-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="265d3-117">Puntatore all'istruzione corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="265d3-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="265d3-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="265d3-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="265d3-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="265d3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="265d3-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="265d3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="265d3-121">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="265d3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="265d3-122">Indirizzo virtuale della pagina che ha causato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="265d3-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="265d3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="265d3-123">Requirements</span></span>



| <span data-ttu-id="265d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="265d3-124">Requirement</span></span> | <span data-ttu-id="265d3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="265d3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="265d3-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="265d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="265d3-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="265d3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="265d3-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="265d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="265d3-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="265d3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="265d3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="265d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265d3-131">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="265d3-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




