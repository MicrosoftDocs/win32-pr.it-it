---
description: È una classe di base astratta che funge da classe padre per tutti gli eventi intrinseci ed estrinseci.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: Classe __Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319325"
---
# <a name="__event-class"></a><span data-ttu-id="d2169-103">\_\_Classe di evento</span><span class="sxs-lookup"><span data-stu-id="d2169-103">\_\_Event class</span></span>

<span data-ttu-id="d2169-104">La classe del sistema di **\_ \_ eventi** è una classe di base astratta che funge da classe padre per tutti gli eventi intrinseci ed estrinseci.</span><span class="sxs-lookup"><span data-stu-id="d2169-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="d2169-105">Tutti i nuovi tipi di evento devono infine derivare da un **\_ \_ evento**.</span><span class="sxs-lookup"><span data-stu-id="d2169-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="d2169-106">Gli eventi intrinseci derivano direttamente da questa classe.</span><span class="sxs-lookup"><span data-stu-id="d2169-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="d2169-107">Gli eventi estrinseci definiti dall'utente derivano da una sottoclasse di questa classe denominata [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="d2169-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="d2169-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d2169-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d2169-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d2169-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2169-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2169-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d2169-111">Members</span><span class="sxs-lookup"><span data-stu-id="d2169-111">Members</span></span>

<span data-ttu-id="d2169-112">La classe di **\_ \_ evento** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2169-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="d2169-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2169-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2169-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2169-114">Properties</span></span>

<span data-ttu-id="d2169-115">La classe di **\_ \_ evento** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2169-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2169-116">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="d2169-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2169-117">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d2169-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d2169-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2169-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2169-119">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="d2169-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="d2169-120">Per ulteriori informazioni, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2169-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2169-121">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="d2169-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2169-122">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2169-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2169-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2169-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2169-124">Valore univoco che indica l'ora in cui viene generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="d2169-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="d2169-125">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="d2169-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d2169-126">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="d2169-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="d2169-127">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2169-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2169-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2169-128">Remarks</span></span>

<span data-ttu-id="d2169-129">La classe di **\_ \_ evento** è derivata da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2169-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2169-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2169-130">Requirements</span></span>



| <span data-ttu-id="d2169-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2169-131">Requirement</span></span> | <span data-ttu-id="d2169-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d2169-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d2169-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2169-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d2169-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2169-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d2169-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2169-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d2169-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2169-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d2169-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2169-137">Namespace</span></span><br/>                | <span data-ttu-id="d2169-138">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="d2169-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d2169-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2169-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2169-140">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="d2169-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="d2169-141">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d2169-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d2169-142">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="d2169-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="d2169-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d2169-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d2169-144">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d2169-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d2169-145">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d2169-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

