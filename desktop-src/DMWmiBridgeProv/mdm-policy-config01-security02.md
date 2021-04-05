---
title: Classe MDM_Policy_Config01_Security02
description: La \_ \_ classe Config01 Security02 dei criteri MDM \_ rappresenta i criteri di sicurezza disponibili.
ms.assetid: 8db74f3f-a7a5-4e93-8aeb-111dcf2111fa
keywords:
- Classe MDM_Policy_Config01_Security02
- Classe MDM_Policy_Config01_Security02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Security02
- MDM_Policy_Config01_Security02.InstanceID
- MDM_Policy_Config01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268e1e01cddb72ddd85e3c18369bdb998bb315aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048417"
---
# <a name="mdm_policy_config01_security02-class"></a><span data-ttu-id="7e251-105">\_ \_ Classe Config01 Security02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="7e251-105">MDM\_Policy\_Config01\_Security02 class</span></span>

<span data-ttu-id="7e251-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="7e251-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7e251-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="7e251-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7e251-108">La **classe \_ \_ Config01 \_ Security02 dei criteri MDM** rappresenta i criteri di sicurezza disponibili.</span><span class="sxs-lookup"><span data-stu-id="7e251-108">The **MDM\_Policy\_Config01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="7e251-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7e251-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e251-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e251-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="7e251-111">Members</span><span class="sxs-lookup"><span data-stu-id="7e251-111">Members</span></span>

<span data-ttu-id="7e251-112">La **classe \_ \_ Config01 \_ Security02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7e251-112">The **MDM\_Policy\_Config01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="7e251-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e251-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e251-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e251-114">Properties</span></span>

<span data-ttu-id="7e251-115">La **classe \_ \_ \_ Security02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e251-115">The **MDM\_Policy\_Config01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7e251-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="7e251-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e251-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="7e251-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e251-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="7e251-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e251-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e251-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7e251-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e251-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e251-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e251-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e251-129">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="7e251-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="7e251-130">Per questa classe la stringa è "Security".</span><span class="sxs-lookup"><span data-stu-id="7e251-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="7e251-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7e251-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7e251-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e251-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e251-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e251-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e251-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="7e251-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="7e251-136">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="7e251-136">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="7e251-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="7e251-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e251-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="7e251-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e251-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="7e251-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e251-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="7e251-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e251-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e251-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e251-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7e251-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e251-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e251-149">Requirements</span></span>



| <span data-ttu-id="7e251-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e251-150">Requirement</span></span> | <span data-ttu-id="7e251-151">Valore</span><span class="sxs-lookup"><span data-stu-id="7e251-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e251-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e251-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7e251-153">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7e251-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e251-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e251-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7e251-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7e251-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7e251-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e251-156">Namespace</span></span><br/>                | <span data-ttu-id="7e251-157">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="7e251-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7e251-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7e251-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e251-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e251-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e251-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7e251-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e251-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e251-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e251-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e251-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e251-163">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="7e251-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

