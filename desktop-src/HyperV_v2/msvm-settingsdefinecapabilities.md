---
description: Fornisce un collegamento tra l'istanza di funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308206"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="18fd6-103">\_Classe MSVM SettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="18fd6-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="18fd6-104">Fornisce un collegamento tra l'istanza di funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="18fd6-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="18fd6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="18fd6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fd6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18fd6-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="18fd6-107">Members</span><span class="sxs-lookup"><span data-stu-id="18fd6-107">Members</span></span>

<span data-ttu-id="18fd6-108">La **classe \_ SettingsDefineCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="18fd6-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="18fd6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18fd6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18fd6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18fd6-110">Properties</span></span>

<span data-ttu-id="18fd6-111">La **classe \_ SettingsDefineCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="18fd6-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18fd6-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="18fd6-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-113">Tipo di dati: **[ **\_ funzionalità CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="18fd6-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-115">Istanza delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="18fd6-115">The capabilities instance.</span></span> <span data-ttu-id="18fd6-116">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18fd6-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18fd6-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="18fd6-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-118">Tipo di dati: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="18fd6-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-120">Impostazione utilizzata per definire l'istanza delle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="18fd6-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="18fd6-121">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18fd6-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18fd6-122">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="18fd6-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18fd6-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-125">Indica se le proprietà non null e non chiave dell'istanza dei dati di impostazione associata vengono gestite in modo indipendente o come set correlato.</span><span class="sxs-lookup"><span data-stu-id="18fd6-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="18fd6-126">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) ed è sempre impostata su 0 (Independent).</span><span class="sxs-lookup"><span data-stu-id="18fd6-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="18fd6-127">**SupportStatement**</span><span class="sxs-lookup"><span data-stu-id="18fd6-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18fd6-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-130">Identifica l'istruzione di supporto.</span><span class="sxs-lookup"><span data-stu-id="18fd6-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="18fd6-131">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="18fd6-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="18fd6-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produzione** (0)</span><span class="sxs-lookup"><span data-stu-id="18fd6-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="18fd6-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versione preliminare** (1)</span><span class="sxs-lookup"><span data-stu-id="18fd6-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="18fd6-134">Non è **prodotto** in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="18fd6-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="18fd6-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="18fd6-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18fd6-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="18fd6-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18fd6-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-139">Qualsiasi altra semantica sull'interpretazione di tutte le proprietà non null e non chiave dei dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="18fd6-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="18fd6-140">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18fd6-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18fd6-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="18fd6-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18fd6-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18fd6-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18fd6-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18fd6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18fd6-144">Qualsiasi altra semantica sull'interpretazione delle proprietà non null e non chiave dei dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="18fd6-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="18fd6-145">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18fd6-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18fd6-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="18fd6-146">Remarks</span></span>

<span data-ttu-id="18fd6-147">I valori per le proprietà **ValueRole** e **ValueRange** vengono usati nelle coppie seguenti:</span><span class="sxs-lookup"><span data-stu-id="18fd6-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="18fd6-148">Punto/predefinito (0/0)</span><span class="sxs-lookup"><span data-stu-id="18fd6-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="18fd6-149">Minima/supportata (1/3)</span><span class="sxs-lookup"><span data-stu-id="18fd6-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="18fd6-150">Massimo/supportato (2/3)</span><span class="sxs-lookup"><span data-stu-id="18fd6-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="18fd6-151">Incrementi/supportati (3/3).</span><span class="sxs-lookup"><span data-stu-id="18fd6-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="18fd6-152">"Point" indica che ognuna delle proprietà dell'oggetto **PartComponent** rappresenta l'impostazione predefinita della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="18fd6-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="18fd6-153">"Minimums" e "Maximers" indicano che ognuna delle proprietà nell'oggetto **PartComponent** rappresenta i valori più piccoli e massimi possibili per queste proprietà supportate dalla piattaforma in base alla configurazione del computer corrente.</span><span class="sxs-lookup"><span data-stu-id="18fd6-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="18fd6-154">"Incrementi" indica la granularità in cui è possibile aumentare o diminuire le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="18fd6-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="18fd6-155">L'accesso alla **classe \_ SettingsDefineCapabilities di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="18fd6-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="18fd6-156">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="18fd6-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="18fd6-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18fd6-157">Requirements</span></span>



| <span data-ttu-id="18fd6-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="18fd6-158">Requirement</span></span> | <span data-ttu-id="18fd6-159">Valore</span><span class="sxs-lookup"><span data-stu-id="18fd6-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fd6-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18fd6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="18fd6-161">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="18fd6-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18fd6-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18fd6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="18fd6-163">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="18fd6-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18fd6-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18fd6-164">Namespace</span></span><br/>                | <span data-ttu-id="18fd6-165">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="18fd6-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18fd6-166">MOF</span><span class="sxs-lookup"><span data-stu-id="18fd6-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18fd6-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18fd6-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18fd6-168">DLL</span><span class="sxs-lookup"><span data-stu-id="18fd6-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18fd6-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18fd6-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18fd6-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18fd6-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18fd6-171">**\_SETTINGSDEFINECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="18fd6-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="18fd6-172">[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18fd6-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="18fd6-173">**MSVM \_ SettingsDefineCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="18fd6-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="18fd6-174">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="18fd6-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

