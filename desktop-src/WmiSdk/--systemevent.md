---
description: Rappresenta un evento di sistema.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: Classe __SystemEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232911"
---
# <a name="__systemevent-class"></a><span data-ttu-id="598e0-103">\_\_Classe SystemEvent</span><span class="sxs-lookup"><span data-stu-id="598e0-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="598e0-104">La classe di sistema **\_ \_ SystemEvent** rappresenta un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="598e0-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="598e0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="598e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="598e0-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="598e0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="598e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="598e0-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="598e0-108">Members</span><span class="sxs-lookup"><span data-stu-id="598e0-108">Members</span></span>

<span data-ttu-id="598e0-109">La classe **\_ \_ SystemEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="598e0-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="598e0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="598e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="598e0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="598e0-111">Properties</span></span>

<span data-ttu-id="598e0-112">La classe **\_ \_ SystemEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="598e0-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="598e0-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="598e0-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="598e0-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="598e0-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="598e0-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="598e0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="598e0-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="598e0-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="598e0-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="598e0-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="598e0-118">Un  elenco di controllo di accesso (ACL) null [**nel \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato a tutti i tempi.</span><span class="sxs-lookup"><span data-stu-id="598e0-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="598e0-119">Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="598e0-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="598e0-120">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="598e0-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="598e0-121">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="598e0-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="598e0-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="598e0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="598e0-123">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="598e0-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="598e0-124">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="598e0-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="598e0-125">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="598e0-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="598e0-126">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="598e0-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="598e0-127">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="598e0-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="598e0-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="598e0-128">Remarks</span></span>

<span data-ttu-id="598e0-129">La classe **\_ \_ SystemEvent** è derivata dalla classe [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="598e0-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="598e0-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="598e0-130">Requirements</span></span>



| <span data-ttu-id="598e0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="598e0-131">Requirement</span></span> | <span data-ttu-id="598e0-132">Valore</span><span class="sxs-lookup"><span data-stu-id="598e0-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="598e0-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="598e0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="598e0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="598e0-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="598e0-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="598e0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="598e0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="598e0-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="598e0-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="598e0-137">Namespace</span></span><br/>                | <span data-ttu-id="598e0-138">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="598e0-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="598e0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="598e0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598e0-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="598e0-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="598e0-141">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="598e0-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

