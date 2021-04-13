---
title: Classe CIM_LogicalElement (Servizi Desktop remoto)
description: Classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- Classe CIM_LogicalElement Servizi Desktop remoto
- Classe CIM_LogicalElement Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400338"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="da4a8-105">Classe CIM_LogicalElement (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="da4a8-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="da4a8-106">Classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="da4a8-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="da4a8-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="da4a8-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4a8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da4a8-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="da4a8-109">Members</span><span class="sxs-lookup"><span data-stu-id="da4a8-109">Members</span></span>

<span data-ttu-id="da4a8-110">La classe **CIM \_ LogicalElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da4a8-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="da4a8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da4a8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da4a8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da4a8-112">Properties</span></span>

<span data-ttu-id="da4a8-113">La classe **CIM \_ LogicalElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da4a8-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da4a8-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="da4a8-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4a8-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da4a8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da4a8-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da4a8-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da4a8-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da4a8-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="da4a8-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4a8-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="da4a8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4a8-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da4a8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da4a8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4a8-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da4a8-123">Description of the object.</span></span>

<span data-ttu-id="da4a8-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4a8-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da4a8-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4a8-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da4a8-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da4a8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="da4a8-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="da4a8-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da4a8-129">The date the object was installed.</span></span> <span data-ttu-id="da4a8-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="da4a8-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="da4a8-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4a8-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="da4a8-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4a8-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da4a8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da4a8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4a8-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da4a8-135">The name of the object.</span></span>

<span data-ttu-id="da4a8-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4a8-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="da4a8-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4a8-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da4a8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da4a8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da4a8-140">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="da4a8-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="da4a8-141">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da4a8-141">Current status of the object.</span></span> <span data-ttu-id="da4a8-142">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="da4a8-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="da4a8-143">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="da4a8-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="da4a8-144">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="da4a8-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="da4a8-145">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="da4a8-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="da4a8-146">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="da4a8-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="da4a8-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="da4a8-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="da4a8-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-149">("Errore")</span><span class="sxs-lookup"><span data-stu-id="da4a8-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-150">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="da4a8-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-151">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="da4a8-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-152">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="da4a8-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-153">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="da4a8-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-154">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="da4a8-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da4a8-155">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="da4a8-155">("Service")</span></span>


<span data-ttu-id="da4a8-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="da4a8-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="da4a8-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da4a8-157">Requirements</span></span>



| <span data-ttu-id="da4a8-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4a8-158">Requirement</span></span> | <span data-ttu-id="da4a8-159">Valore</span><span class="sxs-lookup"><span data-stu-id="da4a8-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da4a8-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da4a8-160">Minimum supported client</span></span><br/> | <span data-ttu-id="da4a8-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da4a8-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da4a8-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da4a8-162">Minimum supported server</span></span><br/> | <span data-ttu-id="da4a8-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da4a8-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da4a8-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da4a8-164">Namespace</span></span><br/>                | <span data-ttu-id="da4a8-165">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="da4a8-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da4a8-166">MOF</span><span class="sxs-lookup"><span data-stu-id="da4a8-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da4a8-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da4a8-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da4a8-168">DLL</span><span class="sxs-lookup"><span data-stu-id="da4a8-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da4a8-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da4a8-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4a8-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da4a8-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4a8-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="da4a8-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

