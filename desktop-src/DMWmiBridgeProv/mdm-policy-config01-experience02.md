---
title: Classe MDM_Policy_Config01_Experience02
description: La \_ \_ classe Config01 Experience02 dei criteri MDM \_ rappresenta i criteri di esperienza disponibili.
ms.assetid: 21052983-696c-4137-9c72-16ea3b4a1eb7
keywords:
- Classe MDM_Policy_Config01_Experience02
- Classe MDM_Policy_Config01_Experience02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02.InstanceID
- MDM_Policy_Config01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38885dbc22c51bfa9e1653f81dba38255f6ba6a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121131"
---
# <a name="mdm_policy_config01_experience02-class"></a><span data-ttu-id="9eb1e-105">\_ \_ Classe Config01 Experience02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="9eb1e-105">MDM\_Policy\_Config01\_Experience02 class</span></span>

<span data-ttu-id="9eb1e-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9eb1e-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9eb1e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9eb1e-108">La **classe \_ \_ Config01 \_ Experience02 dei criteri MDM** rappresenta i criteri di esperienza disponibili.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-108">The **MDM\_Policy\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="9eb1e-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb1e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb1e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="9eb1e-111">Members</span><span class="sxs-lookup"><span data-stu-id="9eb1e-111">Members</span></span>

<span data-ttu-id="9eb1e-112">La **classe \_ \_ Config01 \_ Experience02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9eb1e-112">The **MDM\_Policy\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="9eb1e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9eb1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9eb1e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9eb1e-114">Properties</span></span>

<span data-ttu-id="9eb1e-115">La **classe \_ \_ \_ Experience02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-115">The **MDM\_Policy\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9eb1e-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="9eb1e-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="9eb1e-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="9eb1e-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="9eb1e-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="9eb1e-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eb1e-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="9eb1e-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="9eb1e-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eb1e-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="9eb1e-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="9eb1e-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="9eb1e-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eb1e-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="9eb1e-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eb1e-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9eb1e-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9eb1e-153">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="9eb1e-154">Per questa classe la stringa è "Experience".</span><span class="sxs-lookup"><span data-stu-id="9eb1e-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eb1e-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9eb1e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9eb1e-158">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9eb1e-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9eb1e-159">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="9eb1e-160">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="9eb1e-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9eb1e-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb1e-161">Requirements</span></span>



| <span data-ttu-id="9eb1e-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb1e-162">Requirement</span></span> | <span data-ttu-id="9eb1e-163">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb1e-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb1e-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb1e-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb1e-165">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9eb1e-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9eb1e-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb1e-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb1e-167">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9eb1e-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9eb1e-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9eb1e-168">Namespace</span></span><br/>                | <span data-ttu-id="9eb1e-169">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9eb1e-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9eb1e-170">MOF</span><span class="sxs-lookup"><span data-stu-id="9eb1e-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eb1e-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1e-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eb1e-172">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb1e-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb1e-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1e-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb1e-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eb1e-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb1e-175">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9eb1e-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

