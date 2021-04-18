---
title: Classe CIM_Setting (Servizi Desktop remoto)
description: Rappresenta i parametri operativi e relativi alla configurazione per uno o più elementi di sistema gestiti.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- Classe CIM_Setting Servizi Desktop remoto
- Classe CIM_Setting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301135"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="d6fc2-105">Classe CIM_Setting (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="d6fc2-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="d6fc2-106">Rappresenta i parametri operativi e relativi alla configurazione per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="d6fc2-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fc2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6fc2-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d6fc2-109">Members</span><span class="sxs-lookup"><span data-stu-id="d6fc2-109">Members</span></span>

<span data-ttu-id="d6fc2-110">La classe di **\_ Impostazioni CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d6fc2-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="d6fc2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6fc2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6fc2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6fc2-112">Properties</span></span>

<span data-ttu-id="d6fc2-113">La classe di **\_ Impostazioni CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6fc2-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc2-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6fc2-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d6fc2-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d6fc2-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d6fc2-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6fc2-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc2-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6fc2-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6fc2-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-123">Description of the object.</span></span>

<span data-ttu-id="d6fc2-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6fc2-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc2-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6fc2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d6fc2-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-129">The date the object was installed.</span></span> <span data-ttu-id="d6fc2-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d6fc2-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6fc2-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc2-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6fc2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6fc2-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-135">The name of the object.</span></span>

<span data-ttu-id="d6fc2-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6fc2-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc2-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d6fc2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6fc2-140">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d6fc2-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d6fc2-141">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-141">Current status of the object.</span></span> <span data-ttu-id="d6fc2-142">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d6fc2-143">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d6fc2-144">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d6fc2-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d6fc2-145">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d6fc2-146">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d6fc2-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d6fc2-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-149">("Errore")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-150">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-151">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-152">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-153">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-154">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d6fc2-155">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="d6fc2-155">("Service")</span></span>


<span data-ttu-id="d6fc2-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d6fc2-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d6fc2-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6fc2-157">Requirements</span></span>



| <span data-ttu-id="d6fc2-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6fc2-158">Requirement</span></span> | <span data-ttu-id="d6fc2-159">Valore</span><span class="sxs-lookup"><span data-stu-id="d6fc2-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fc2-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6fc2-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fc2-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6fc2-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6fc2-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6fc2-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fc2-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6fc2-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6fc2-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6fc2-164">Namespace</span></span><br/>                | <span data-ttu-id="d6fc2-165">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d6fc2-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d6fc2-166">MOF</span><span class="sxs-lookup"><span data-stu-id="d6fc2-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6fc2-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6fc2-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6fc2-168">DLL</span><span class="sxs-lookup"><span data-stu-id="d6fc2-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6fc2-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6fc2-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fc2-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6fc2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fc2-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d6fc2-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

