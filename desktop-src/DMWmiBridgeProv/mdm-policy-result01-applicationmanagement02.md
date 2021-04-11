---
title: Classe MDM_Policy_Result01_ApplicationManagement02
description: La \_ \_ classe Result01 ApplicationManagement02 dei criteri MDM \_ rappresenta i criteri di gestione delle applicazioni disponibili. \_Criteri MDM \_ Result01 \_ ApplicationManagement02 classe rappresenta i criteri di gestione delle applicazioni disponibili.
ms.assetid: 141614e4-b2b1-49d9-879c-f6f86bee070c
keywords:
- Classe MDM_Policy_Result01_ApplicationManagement02
- Classe MDM_Policy_Result01_ApplicationManagement02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477e4e58216c912aa14ec17b8e5879643e3de83f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119903"
---
# <a name="mdm_policy_result01_applicationmanagement02-class"></a><span data-ttu-id="02d5c-105">\_ \_ Classe Result01 ApplicationManagement02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="02d5c-105">MDM\_Policy\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="02d5c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="02d5c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="02d5c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="02d5c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="02d5c-108">La **classe \_ \_ Result01 \_ ApplicationManagement02 dei criteri MDM** rappresenta i criteri di gestione delle applicazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="02d5c-108">The **MDM\_Policy\_Result01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="02d5c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="02d5c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d5c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02d5c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="02d5c-111">Members</span><span class="sxs-lookup"><span data-stu-id="02d5c-111">Members</span></span>

<span data-ttu-id="02d5c-112">La **classe \_ \_ Result01 \_ ApplicationManagement02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02d5c-112">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="02d5c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02d5c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02d5c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02d5c-114">Properties</span></span>

<span data-ttu-id="02d5c-115">La **classe \_ \_ \_ ApplicationManagement02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="02d5c-115">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="02d5c-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="02d5c-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-119">AllowAppStoreAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="02d5c-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-122">AllowDeveloperUnlock</span><span class="sxs-lookup"><span data-stu-id="02d5c-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-125">AllowGameDVR</span><span class="sxs-lookup"><span data-stu-id="02d5c-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-128">AllowSharedUserAppData</span><span class="sxs-lookup"><span data-stu-id="02d5c-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-131">DisableStoreOriginatedApps</span><span class="sxs-lookup"><span data-stu-id="02d5c-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="02d5c-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="02d5c-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="02d5c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="02d5c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02d5c-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02d5c-138">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="02d5c-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="02d5c-139">Per questa classe la stringa è "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="02d5c-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="02d5c-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="02d5c-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="02d5c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="02d5c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02d5c-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02d5c-144">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="02d5c-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="02d5c-145">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="02d5c-145">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="02d5c-146">RestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="02d5c-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d5c-149">RestrictAppToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="02d5c-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d5c-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d5c-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d5c-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="02d5c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02d5c-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02d5c-152">Requirements</span></span>



| <span data-ttu-id="02d5c-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d5c-153">Requirement</span></span> | <span data-ttu-id="02d5c-154">Valore</span><span class="sxs-lookup"><span data-stu-id="02d5c-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d5c-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02d5c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="02d5c-156">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="02d5c-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02d5c-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02d5c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="02d5c-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02d5c-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="02d5c-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02d5c-159">Namespace</span></span><br/>                | <span data-ttu-id="02d5c-160">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="02d5c-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="02d5c-161">MOF</span><span class="sxs-lookup"><span data-stu-id="02d5c-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02d5c-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02d5c-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="02d5c-163">DLL</span><span class="sxs-lookup"><span data-stu-id="02d5c-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02d5c-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d5c-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d5c-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02d5c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d5c-166">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="02d5c-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

