---
description: La classe WMIEvent è una classe di base da cui derivano tutte le classi di evento WMI.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Classe WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058098"
---
# <a name="wmievent-class"></a><span data-ttu-id="a6902-103">Classe WMIEvent</span><span class="sxs-lookup"><span data-stu-id="a6902-103">WMIEvent class</span></span>

<span data-ttu-id="a6902-104">La classe **WmiEvent** è una classe di base da cui derivano tutte le classi di evento WMI.</span><span class="sxs-lookup"><span data-stu-id="a6902-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="a6902-105">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a6902-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a6902-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a6902-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6902-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6902-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="a6902-108">Members</span><span class="sxs-lookup"><span data-stu-id="a6902-108">Members</span></span>

<span data-ttu-id="a6902-109">La classe **WmiEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6902-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a6902-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6902-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6902-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6902-111">Properties</span></span>

<span data-ttu-id="a6902-112">La classe **WmiEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6902-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6902-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="a6902-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6902-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a6902-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a6902-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6902-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6902-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="a6902-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="a6902-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="a6902-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="a6902-118">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="a6902-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="a6902-119">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="a6902-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6902-120">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a6902-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a6902-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6902-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6902-122">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="a6902-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="a6902-123">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="a6902-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="a6902-124">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="a6902-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="a6902-125">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="a6902-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="a6902-126">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6902-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6902-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6902-127">Remarks</span></span>

<span data-ttu-id="a6902-128">La classe **WmiEvent** deriva da [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="a6902-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6902-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6902-129">Requirements</span></span>



| <span data-ttu-id="a6902-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6902-130">Requirement</span></span> | <span data-ttu-id="a6902-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a6902-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6902-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6902-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a6902-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6902-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a6902-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6902-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a6902-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6902-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="a6902-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6902-136">Namespace</span></span><br/>                | <span data-ttu-id="a6902-137">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="a6902-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="a6902-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a6902-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6902-139"><dt>WMI. mof; </dt> <dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6902-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6902-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a6902-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6902-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6902-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="a6902-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6902-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6902-143">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="a6902-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="a6902-144">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="a6902-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

