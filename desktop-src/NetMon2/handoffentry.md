---
description: La struttura HANDOFFENTRY definisce una voce di protocollo specifica in una struttura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Struttura HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525128"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="2435b-103">Struttura HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="2435b-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="2435b-104">La struttura **HANDOFFENTRY** definisce una voce di protocollo specifica in una struttura **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="2435b-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="2435b-105">Questa struttura viene compilata da Network Monitor in base alle informazioni contenute in un file con estensione ini fornito dall'utente durante la chiamata della funzione [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="2435b-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="2435b-106">Questa struttura non deve mai essere modificata in modo esplicito da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2435b-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="2435b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2435b-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="2435b-108">Members</span><span class="sxs-lookup"><span data-stu-id="2435b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2435b-109">**Hoe \_ sig**</span><span class="sxs-lookup"><span data-stu-id="2435b-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="2435b-110">Firma che identifica questa voce come una voce di tabella di continuità.</span><span class="sxs-lookup"><span data-stu-id="2435b-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="2435b-111">**\_ProtIdentNumber Hoe**</span><span class="sxs-lookup"><span data-stu-id="2435b-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="2435b-112">Numero di protocollo fornito dal file ini fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2435b-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="2435b-113">**\_ProtocolHandle Hoe**</span><span class="sxs-lookup"><span data-stu-id="2435b-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="2435b-114">Handle del protocollo creato utilizzando il nome del protocollo fornito dal file ini fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2435b-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="2435b-115">**\_ProtocolData Hoe**</span><span class="sxs-lookup"><span data-stu-id="2435b-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="2435b-116">Dati dell'istanza del protocollo forniti dal file ini fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2435b-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2435b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2435b-117">Remarks</span></span>

<span data-ttu-id="2435b-118">Questa struttura viene compilata da Network Monitor quando Network Monitor crea una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="2435b-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="2435b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2435b-119">Requirements</span></span>



| <span data-ttu-id="2435b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2435b-120">Requirement</span></span> | <span data-ttu-id="2435b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2435b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2435b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2435b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2435b-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2435b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2435b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2435b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2435b-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2435b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2435b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2435b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2435b-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2435b-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2435b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2435b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2435b-129">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="2435b-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




