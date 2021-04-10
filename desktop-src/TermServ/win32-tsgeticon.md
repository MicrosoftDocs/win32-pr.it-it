---
title: Classe Win32_TSGetIcon
description: Restituisce il contenuto dell'icona specificata dal percorso e dall'indice del file.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGetIcon Servizi Desktop remoto
- Classe Win32_TSGetIcon Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964318"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="d6370-105">Win32 \_ TSGetIcon (classe)</span><span class="sxs-lookup"><span data-stu-id="d6370-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="d6370-106">Restituisce il contenuto dell'icona specificata dal percorso del file e dall'indice</span><span class="sxs-lookup"><span data-stu-id="d6370-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="d6370-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d6370-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6370-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6370-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d6370-109">Members</span><span class="sxs-lookup"><span data-stu-id="d6370-109">Members</span></span>

<span data-ttu-id="d6370-110">La classe **Win32 \_ TSGetIcon** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d6370-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="d6370-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d6370-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6370-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6370-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6370-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="d6370-113">Methods</span></span>

<span data-ttu-id="d6370-114">La classe **Win32 \_ TSGetIcon** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d6370-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="d6370-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="d6370-115">Method</span></span>                                     | <span data-ttu-id="d6370-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6370-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="d6370-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="d6370-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="d6370-118">Restituisce il contenuto dell'icona specificata.</span><span class="sxs-lookup"><span data-stu-id="d6370-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d6370-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6370-119">Properties</span></span>

<span data-ttu-id="d6370-120">La classe **Win32 \_ TSGetIcon** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d6370-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6370-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d6370-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6370-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6370-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6370-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6370-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6370-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d6370-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d6370-125">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6370-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d6370-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6370-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6370-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d6370-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6370-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6370-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6370-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6370-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6370-130">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6370-130">Description of the object.</span></span>

<span data-ttu-id="d6370-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6370-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6370-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d6370-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6370-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6370-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d6370-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6370-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6370-135">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d6370-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d6370-136">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6370-136">The date the object was installed.</span></span> <span data-ttu-id="d6370-137">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="d6370-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d6370-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6370-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6370-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d6370-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6370-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6370-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6370-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6370-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6370-142">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6370-142">The name of the object.</span></span>

<span data-ttu-id="d6370-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6370-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6370-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="d6370-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6370-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6370-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6370-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6370-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6370-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d6370-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d6370-148">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6370-148">Current status of the object.</span></span> <span data-ttu-id="d6370-149">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="d6370-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d6370-150">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="d6370-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d6370-151">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d6370-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d6370-152">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d6370-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d6370-153">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d6370-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d6370-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6370-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d6370-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="d6370-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-156">("Errore")</span><span class="sxs-lookup"><span data-stu-id="d6370-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-157">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="d6370-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-158">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d6370-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-159">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="d6370-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-160">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="d6370-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-161">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="d6370-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6370-162">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="d6370-162">("Service")</span></span>


<span data-ttu-id="d6370-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d6370-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d6370-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6370-164">Requirements</span></span>



| <span data-ttu-id="d6370-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6370-165">Requirement</span></span> | <span data-ttu-id="d6370-166">Valore</span><span class="sxs-lookup"><span data-stu-id="d6370-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6370-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6370-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d6370-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d6370-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d6370-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6370-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d6370-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6370-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="d6370-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6370-171">Namespace</span></span><br/>                | <span data-ttu-id="d6370-172">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d6370-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d6370-173">MOF</span><span class="sxs-lookup"><span data-stu-id="d6370-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6370-174"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6370-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d6370-175">DLL</span><span class="sxs-lookup"><span data-stu-id="d6370-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6370-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6370-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

