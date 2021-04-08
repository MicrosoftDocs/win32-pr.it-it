---
title: Classe MDM_SharedPC
description: La \_ classe MDM SharedPC viene utilizzata per configurare le impostazioni per l'utilizzo dei computer condivisi.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- Classe MDM_SharedPC
- Classe MDM_SharedPC, descritta
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047894"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="f7886-105">MDM \_ SharedPC (classe)</span><span class="sxs-lookup"><span data-stu-id="f7886-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="f7886-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f7886-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7886-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f7886-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7886-108">La \_ classe MDM SharedPC viene utilizzata per configurare le impostazioni per l'utilizzo dei computer condivisi.</span><span class="sxs-lookup"><span data-stu-id="f7886-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="f7886-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f7886-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7886-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7886-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="f7886-111">Members</span><span class="sxs-lookup"><span data-stu-id="f7886-111">Members</span></span>

<span data-ttu-id="f7886-112">La classe **MDM \_ SharedPC** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7886-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="f7886-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7886-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7886-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7886-114">Properties</span></span>

<span data-ttu-id="f7886-115">La classe **MDM \_ SharedPC** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7886-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f7886-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="f7886-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-119">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7886-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-123">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="f7886-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-125">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-127">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="f7886-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-131">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="f7886-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-135">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="f7886-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-139">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="f7886-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-143">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="f7886-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7886-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7886-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7886-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7886-147">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7886-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7886-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="f7886-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7886-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-151">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="f7886-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7886-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-155">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="f7886-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-157">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-159">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="f7886-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-161">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-163">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="f7886-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f7886-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7886-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7886-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7886-167">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7886-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7886-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="f7886-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-169">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-171">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="f7886-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-173">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-175">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-176">SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="f7886-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-177">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-179">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="f7886-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-181">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7886-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-183">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="f7886-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="f7886-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7886-185">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7886-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7886-186">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7886-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7886-187">Per ulteriori informazioni, vedere [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="f7886-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7886-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7886-188">Requirements</span></span>



| <span data-ttu-id="f7886-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7886-189">Requirement</span></span> | <span data-ttu-id="f7886-190">Valore</span><span class="sxs-lookup"><span data-stu-id="f7886-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7886-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7886-191">Minimum supported client</span></span><br/> | <span data-ttu-id="f7886-192">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7886-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7886-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7886-193">Minimum supported server</span></span><br/> | <span data-ttu-id="f7886-194">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7886-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f7886-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7886-195">Namespace</span></span><br/>                | <span data-ttu-id="f7886-196">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f7886-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="f7886-197">MOF</span><span class="sxs-lookup"><span data-stu-id="f7886-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7886-198"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7886-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7886-199">DLL</span><span class="sxs-lookup"><span data-stu-id="f7886-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7886-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7886-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

