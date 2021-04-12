---
description: Funge da classe padre per tutti i tipi di evento definiti dall'utente, noti anche come eventi estrinseci.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: Classe __ExtrinsicEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233480"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="b4d41-103">\_\_Classe ExtrinsicEvent</span><span class="sxs-lookup"><span data-stu-id="b4d41-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="b4d41-104">La classe di sistema **\_ \_ ExtrinsicEvent** è una classe di base astratta che funge da classe padre per tutti i tipi di evento definiti dall'utente, noti anche come [eventi estrinseci](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="b4d41-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="b4d41-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b4d41-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b4d41-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b4d41-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4d41-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b4d41-108">Members</span><span class="sxs-lookup"><span data-stu-id="b4d41-108">Members</span></span>

<span data-ttu-id="b4d41-109">La classe **\_ \_ ExtrinsicEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b4d41-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b4d41-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4d41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4d41-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4d41-111">Properties</span></span>

<span data-ttu-id="b4d41-112">La classe **\_ \_ ExtrinsicEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4d41-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4d41-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="b4d41-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d41-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4d41-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4d41-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4d41-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d41-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="b4d41-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b4d41-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b4d41-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="b4d41-118">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b4d41-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4d41-119">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="b4d41-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d41-120">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4d41-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4d41-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4d41-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d41-122">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b4d41-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b4d41-123">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="b4d41-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b4d41-124">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="b4d41-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="b4d41-125">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b4d41-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b4d41-126">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b4d41-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4d41-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4d41-127">Remarks</span></span>

<span data-ttu-id="b4d41-128">La classe **\_ \_ ExtrinsicEvent** è derivata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b4d41-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d41-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4d41-129">Requirements</span></span>



| <span data-ttu-id="b4d41-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4d41-130">Requirement</span></span> | <span data-ttu-id="b4d41-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b4d41-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b4d41-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4d41-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d41-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4d41-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b4d41-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4d41-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d41-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4d41-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b4d41-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4d41-136">Namespace</span></span><br/>                | <span data-ttu-id="b4d41-137">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="b4d41-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b4d41-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4d41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d41-139">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="b4d41-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="b4d41-140">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b4d41-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

