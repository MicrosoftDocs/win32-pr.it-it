---
title: Classe CIM_ManagedSystemElement (Servizi Desktop remoto)
description: Classe base per la gerarchia degli elementi di sistema.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- Classe CIM_ManagedSystemElement Servizi Desktop remoto
- Classe CIM_ManagedSystemElement Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119207"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="3b0da-105">Classe CIM_ManagedSystemElement (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="3b0da-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="3b0da-106">Classe base per la gerarchia degli elementi di sistema.</span><span class="sxs-lookup"><span data-stu-id="3b0da-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="3b0da-107">Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.</span><span class="sxs-lookup"><span data-stu-id="3b0da-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="3b0da-108">Gli esempi includono componenti software, ad esempio file; dispositivi, ad esempio unità disco e controller; e componenti fisici, ad esempio chip e schede</span><span class="sxs-lookup"><span data-stu-id="3b0da-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="3b0da-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3b0da-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0da-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b0da-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="3b0da-111">Members</span><span class="sxs-lookup"><span data-stu-id="3b0da-111">Members</span></span>

<span data-ttu-id="3b0da-112">La classe **CIM \_ ManagedSystemElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b0da-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="3b0da-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b0da-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b0da-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b0da-114">Properties</span></span>

<span data-ttu-id="3b0da-115">La classe **CIM \_ ManagedSystemElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b0da-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b0da-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3b0da-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0da-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b0da-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b0da-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b0da-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b0da-120">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b0da-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="3b0da-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3b0da-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0da-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b0da-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b0da-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b0da-124">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b0da-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="3b0da-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b0da-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0da-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b0da-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b0da-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="3b0da-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3b0da-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b0da-129">The date the object was installed.</span></span> <span data-ttu-id="3b0da-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="3b0da-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="3b0da-131">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3b0da-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0da-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b0da-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b0da-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b0da-134">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b0da-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="3b0da-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="3b0da-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0da-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b0da-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b0da-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0da-138">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="3b0da-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="3b0da-139">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b0da-139">Current status of the object.</span></span> <span data-ttu-id="3b0da-140">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="3b0da-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3b0da-141">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="3b0da-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3b0da-142">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="3b0da-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3b0da-143">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="3b0da-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3b0da-144">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="3b0da-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="3b0da-145">("OK")</span><span class="sxs-lookup"><span data-stu-id="3b0da-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-146">("Errore")</span><span class="sxs-lookup"><span data-stu-id="3b0da-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-147">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="3b0da-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-148">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="3b0da-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-149">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="3b0da-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-150">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="3b0da-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-151">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="3b0da-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b0da-152">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="3b0da-152">("Service")</span></span>


<span data-ttu-id="3b0da-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3b0da-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3b0da-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b0da-154">Requirements</span></span>



| <span data-ttu-id="3b0da-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b0da-155">Requirement</span></span> | <span data-ttu-id="3b0da-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3b0da-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0da-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b0da-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0da-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b0da-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b0da-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b0da-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0da-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b0da-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b0da-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b0da-161">Namespace</span></span><br/>                | <span data-ttu-id="3b0da-162">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3b0da-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3b0da-163">MOF</span><span class="sxs-lookup"><span data-stu-id="3b0da-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b0da-164"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b0da-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b0da-165">DLL</span><span class="sxs-lookup"><span data-stu-id="3b0da-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0da-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b0da-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

