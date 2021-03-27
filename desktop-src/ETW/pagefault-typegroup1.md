---
description: Questa classe è la classe del tipo di evento per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Classe PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232277"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="6fcb3-104">\_Classe pagefault TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="6fcb3-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="6fcb3-105">Questa classe è la classe del tipo di evento per gli eventi di errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="6fcb3-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fcb3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fcb3-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="6fcb3-108">Members</span><span class="sxs-lookup"><span data-stu-id="6fcb3-108">Members</span></span>

<span data-ttu-id="6fcb3-109">La **classe \_ TypeGroup1 di pagefault** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6fcb3-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6fcb3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fcb3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fcb3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fcb3-111">Properties</span></span>

<span data-ttu-id="6fcb3-112">La **classe \_ TypeGroup1 di pagefault** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fcb3-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="6fcb3-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcb3-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fcb3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcb3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fcb3-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="6fcb3-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fcb3-117">Puntatore all'istruzione corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="6fcb3-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="6fcb3-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcb3-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fcb3-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcb3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fcb3-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="6fcb3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fcb3-122">Indirizzo virtuale della pagina che ha causato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fcb3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fcb3-123">Remarks</span></span>

<span data-ttu-id="6fcb3-124">Un errore di pagina si verifica quando una pagina cercata nella cache in memoria non viene trovata e deve essere recuperata da un'altra posizione nella memoria (un errore software) o dal disco (errore hardware).</span><span class="sxs-lookup"><span data-stu-id="6fcb3-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcb3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fcb3-125">Requirements</span></span>



| <span data-ttu-id="6fcb3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcb3-126">Requirement</span></span> | <span data-ttu-id="6fcb3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcb3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6fcb3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcb3-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fcb3-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fcb3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcb3-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fcb3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fcb3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fcb3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcb3-133">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




