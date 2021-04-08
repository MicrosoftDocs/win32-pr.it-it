---
title: Classe MDM_Policy_Result01_Experience02
description: La \_ \_ classe Result01 Experience02 dei criteri MDM \_ rappresenta i criteri di esperienza disponibili.
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- Classe MDM_Policy_Result01_Experience02
- Classe MDM_Policy_Result01_Experience02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047910"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="f2298-105">\_ \_ Classe Result01 Experience02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="f2298-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="f2298-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f2298-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2298-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f2298-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2298-108">La **classe \_ \_ Result01 \_ Experience02 dei criteri MDM** rappresenta i criteri di esperienza disponibili.</span><span class="sxs-lookup"><span data-stu-id="f2298-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="f2298-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f2298-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2298-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2298-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="f2298-111">Members</span><span class="sxs-lookup"><span data-stu-id="f2298-111">Members</span></span>

<span data-ttu-id="f2298-112">La **classe \_ \_ Result01 \_ Experience02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f2298-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="f2298-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2298-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2298-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2298-114">Properties</span></span>

<span data-ttu-id="f2298-115">La **classe \_ \_ \_ Experience02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f2298-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f2298-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="f2298-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="f2298-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="f2298-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="f2298-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="f2298-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2298-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="f2298-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="f2298-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2298-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="f2298-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="f2298-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="f2298-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2298-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="f2298-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2298-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2298-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2298-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2298-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2298-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f2298-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2298-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2298-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2298-153">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f2298-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="f2298-154">Per questa classe la stringa è "Experience".</span><span class="sxs-lookup"><span data-stu-id="f2298-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="f2298-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2298-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2298-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2298-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2298-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f2298-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2298-158">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2298-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2298-159">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f2298-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2298-160">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="f2298-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2298-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2298-161">Requirements</span></span>



| <span data-ttu-id="f2298-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2298-162">Requirement</span></span> | <span data-ttu-id="f2298-163">Valore</span><span class="sxs-lookup"><span data-stu-id="f2298-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2298-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2298-164">Minimum supported client</span></span><br/> | <span data-ttu-id="f2298-165">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f2298-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2298-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2298-166">Minimum supported server</span></span><br/> | <span data-ttu-id="f2298-167">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2298-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2298-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2298-168">Namespace</span></span><br/>                | <span data-ttu-id="f2298-169">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f2298-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f2298-170">MOF</span><span class="sxs-lookup"><span data-stu-id="f2298-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2298-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2298-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2298-172">DLL</span><span class="sxs-lookup"><span data-stu-id="f2298-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2298-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2298-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2298-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2298-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2298-175">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f2298-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

