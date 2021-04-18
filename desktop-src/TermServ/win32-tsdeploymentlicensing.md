---
title: Classe Win32_TSDeploymentLicensing
description: Impostazioni di gestione licenze per la distribuzione di Desktop remoto Virtualization (RDV).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSDeploymentLicensing Servizi Desktop remoto
- Classe Win32_TSDeploymentLicensing Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302429"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="5a349-105">Win32 \_ TSDeploymentLicensing (classe)</span><span class="sxs-lookup"><span data-stu-id="5a349-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="5a349-106">Impostazioni di gestione licenze per la distribuzione di Desktop remoto Virtualization (RDV).</span><span class="sxs-lookup"><span data-stu-id="5a349-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="5a349-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5a349-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a349-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a349-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="5a349-109">Members</span><span class="sxs-lookup"><span data-stu-id="5a349-109">Members</span></span>

<span data-ttu-id="5a349-110">La classe **Win32 \_ TSDeploymentLicensing** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a349-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="5a349-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a349-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a349-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a349-112">Properties</span></span>

<span data-ttu-id="5a349-113">La classe **Win32 \_ TSDeploymentLicensing** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a349-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a349-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5a349-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a349-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a349-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a349-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a349-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a349-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a349-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5a349-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a349-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a349-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5a349-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a349-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a349-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a349-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a349-123">Description of the object.</span></span>

<span data-ttu-id="5a349-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a349-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a349-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a349-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a349-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a349-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a349-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5a349-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5a349-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a349-129">The date the object was installed.</span></span> <span data-ttu-id="5a349-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5a349-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5a349-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a349-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a349-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="5a349-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5a349-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="5a349-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a349-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a349-135">Specifica i server licenze da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5a349-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="5a349-136">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="5a349-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a349-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a349-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a349-139">Modalità di gestione licenze</span><span class="sxs-lookup"><span data-stu-id="5a349-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="5a349-140">**Per dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="5a349-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="5a349-141">**Per utente** (4)</span><span class="sxs-lookup"><span data-stu-id="5a349-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="5a349-142">**Non ancora configurata** (5)</span><span class="sxs-lookup"><span data-stu-id="5a349-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a349-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5a349-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a349-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a349-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a349-146">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a349-146">The name of the object.</span></span>

<span data-ttu-id="5a349-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a349-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a349-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="5a349-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a349-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a349-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a349-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5a349-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5a349-152">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a349-152">Current status of the object.</span></span> <span data-ttu-id="5a349-153">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="5a349-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5a349-154">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="5a349-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5a349-155">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5a349-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5a349-156">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5a349-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5a349-157">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5a349-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5a349-158">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a349-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5a349-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="5a349-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-160">("Errore")</span><span class="sxs-lookup"><span data-stu-id="5a349-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-161">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="5a349-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-162">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5a349-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-163">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="5a349-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-164">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="5a349-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-165">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="5a349-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5a349-166">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="5a349-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a349-167">**UseCentralLicensingSettings**</span><span class="sxs-lookup"><span data-stu-id="5a349-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a349-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a349-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a349-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a349-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a349-170">Specifica se utilizzare le impostazioni di gestione licenze a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a349-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="5a349-171">**True** per utilizzare queste impostazioni per tutti i server in questa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a349-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="5a349-172">**false** per impostarli per server.</span><span class="sxs-lookup"><span data-stu-id="5a349-172">**false** to set them per-server.</span></span> <span data-ttu-id="5a349-173">Se è impostato su **false**, tutte le altre impostazioni di licenza verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="5a349-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a349-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a349-174">Requirements</span></span>



| <span data-ttu-id="5a349-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a349-175">Requirement</span></span> | <span data-ttu-id="5a349-176">Valore</span><span class="sxs-lookup"><span data-stu-id="5a349-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a349-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a349-177">Minimum supported client</span></span><br/> | <span data-ttu-id="5a349-178">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5a349-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5a349-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a349-179">Minimum supported server</span></span><br/> | <span data-ttu-id="5a349-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a349-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="5a349-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a349-181">Namespace</span></span><br/>                | <span data-ttu-id="5a349-182">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5a349-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5a349-183">MOF</span><span class="sxs-lookup"><span data-stu-id="5a349-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a349-184"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a349-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5a349-185">DLL</span><span class="sxs-lookup"><span data-stu-id="5a349-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a349-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a349-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

