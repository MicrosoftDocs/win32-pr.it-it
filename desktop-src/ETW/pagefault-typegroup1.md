---
description: 'PageFault_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 classe
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
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106409"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="a13b1-104">Classe PageFault \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="a13b1-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="a13b1-105">Questa classe è la classe del tipo di evento per gli eventi di errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="a13b1-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="a13b1-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a13b1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a13b1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a13b1-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="a13b1-108">Members</span><span class="sxs-lookup"><span data-stu-id="a13b1-108">Members</span></span>

<span data-ttu-id="a13b1-109">La **classe PageFault \_ TypeGroup1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a13b1-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a13b1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a13b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a13b1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a13b1-111">Properties</span></span>

<span data-ttu-id="a13b1-112">La **classe PageFault \_ TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a13b1-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a13b1-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="a13b1-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a13b1-114">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="a13b1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a13b1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a13b1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a13b1-116">Qualificatori: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="a13b1-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a13b1-117">Puntatore all'istruzione corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a13b1-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="a13b1-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="a13b1-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a13b1-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="a13b1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a13b1-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a13b1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a13b1-121">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="a13b1-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a13b1-122">Indirizzo virtuale della pagina che ha causato l'errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="a13b1-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a13b1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a13b1-123">Remarks</span></span>

<span data-ttu-id="a13b1-124">Un errore di pagina si verifica quando una pagina cercata nella cache di memoria non viene trovata e deve essere recuperata da un'altra posizione nella memoria (errore soft) o dal disco (errore hardware).</span><span class="sxs-lookup"><span data-stu-id="a13b1-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="a13b1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a13b1-125">Requirements</span></span>



| <span data-ttu-id="a13b1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a13b1-126">Requirement</span></span> | <span data-ttu-id="a13b1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a13b1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a13b1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a13b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a13b1-129">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a13b1-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a13b1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a13b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a13b1-131">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a13b1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a13b1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a13b1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13b1-133">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="a13b1-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




