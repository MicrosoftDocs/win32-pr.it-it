---
title: Classe Win32_CentralPublishingChangeEvent
description: Evento che rappresenta una modifica alle impostazioni di RDV centrale.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Classe Win32_CentralPublishingChangeEvent Servizi Desktop remoto
- Classe Win32_CentralPublishingChangeEvent Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477422"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="961ef-105">Win32 \_ CentralPublishingChangeEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="961ef-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="961ef-106">Evento che rappresenta una modifica alle impostazioni di RDV centrale.</span><span class="sxs-lookup"><span data-stu-id="961ef-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="961ef-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="961ef-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="961ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="961ef-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="961ef-109">Members</span><span class="sxs-lookup"><span data-stu-id="961ef-109">Members</span></span>

<span data-ttu-id="961ef-110">La classe **Win32 \_ CentralPublishingChangeEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="961ef-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="961ef-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="961ef-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="961ef-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="961ef-112">Properties</span></span>

<span data-ttu-id="961ef-113">La classe **Win32 \_ CentralPublishingChangeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="961ef-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="961ef-114">**Tipo operazione**</span><span class="sxs-lookup"><span data-stu-id="961ef-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="961ef-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="961ef-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="961ef-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="961ef-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="961ef-117">Tipo di operazione corrispondente all'evento.</span><span class="sxs-lookup"><span data-stu-id="961ef-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="961ef-118">**Creazione** (0)</span><span class="sxs-lookup"><span data-stu-id="961ef-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="961ef-119">**Modifica** (1)</span><span class="sxs-lookup"><span data-stu-id="961ef-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="961ef-120">**Elimina** (2)</span><span class="sxs-lookup"><span data-stu-id="961ef-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="961ef-121">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="961ef-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="961ef-122">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="961ef-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="961ef-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="961ef-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="961ef-124">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="961ef-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="961ef-125">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="961ef-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="961ef-126">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="961ef-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="961ef-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="961ef-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="961ef-128">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="961ef-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="961ef-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="961ef-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="961ef-130">Oggetto modificato dall'operazione corrispondente all'evento.</span><span class="sxs-lookup"><span data-stu-id="961ef-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="961ef-131">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="961ef-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="961ef-132">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="961ef-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="961ef-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="961ef-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="961ef-134">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="961ef-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="961ef-135">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="961ef-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="961ef-136">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="961ef-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="961ef-137">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="961ef-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="961ef-138">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="961ef-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="961ef-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="961ef-139">Requirements</span></span>



| <span data-ttu-id="961ef-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="961ef-140">Requirement</span></span> | <span data-ttu-id="961ef-141">Valore</span><span class="sxs-lookup"><span data-stu-id="961ef-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="961ef-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="961ef-142">Minimum supported client</span></span><br/> | <span data-ttu-id="961ef-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="961ef-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="961ef-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="961ef-144">Minimum supported server</span></span><br/> | <span data-ttu-id="961ef-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="961ef-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="961ef-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="961ef-146">Namespace</span></span><br/>                | <span data-ttu-id="961ef-147">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="961ef-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="961ef-148">MOF</span><span class="sxs-lookup"><span data-stu-id="961ef-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="961ef-149"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="961ef-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="961ef-150">DLL</span><span class="sxs-lookup"><span data-stu-id="961ef-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="961ef-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="961ef-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

