---
description: La struttura HANDOFFTABLE definisce i protocolli di una tabella con continuità.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Struttura HANDOFFTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305890"
---
# <a name="handofftable-structure"></a><span data-ttu-id="afa5b-103">Struttura HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="afa5b-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="afa5b-104">La struttura **HANDOFFTABLE** definisce i protocolli di una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="afa5b-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="afa5b-105">Questa struttura viene compilata da Network Monitor in base alle informazioni contenute in un file con estensione ini fornito dall'utente durante la chiamata della funzione [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="afa5b-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa5b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afa5b-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="afa5b-107">Members</span><span class="sxs-lookup"><span data-stu-id="afa5b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="afa5b-108">**Sig. attivo \_**</span><span class="sxs-lookup"><span data-stu-id="afa5b-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="afa5b-109">Firma che identifica la tabella come tabella di continuità.</span><span class="sxs-lookup"><span data-stu-id="afa5b-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="afa5b-110">**numEntries a caldo \_**</span><span class="sxs-lookup"><span data-stu-id="afa5b-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="afa5b-111">Numero di voci che Network Monitor aggiunte alla tabella di continuità.</span><span class="sxs-lookup"><span data-stu-id="afa5b-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="afa5b-112">**\_voci sensibili**</span><span class="sxs-lookup"><span data-stu-id="afa5b-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="afa5b-113">Tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="afa5b-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afa5b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="afa5b-114">Remarks</span></span>

<span data-ttu-id="afa5b-115">Questa struttura e le strutture HANDOFFENTRY associate vengono compilate da Network Monitor quando Network Monitor crea una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="afa5b-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="afa5b-116">Le informazioni sul protocollo utilizzate durante la creazione di una tabella con continuità vengono fornite in un file ini fornito dall'applicazione quando viene chiamato [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="afa5b-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa5b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afa5b-117">Requirements</span></span>



| <span data-ttu-id="afa5b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa5b-118">Requirement</span></span> | <span data-ttu-id="afa5b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="afa5b-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="afa5b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afa5b-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="afa5b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="afa5b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afa5b-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="afa5b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="afa5b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afa5b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa5b-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa5b-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa5b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afa5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa5b-127">HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="afa5b-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="afa5b-128">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="afa5b-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




