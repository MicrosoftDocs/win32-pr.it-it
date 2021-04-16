---
title: Classe MDM_EnterpriseDataProtection_Settings01
description: La \_ classe MDM EnterpriseDataProtection \_ Settings01 viene usata per configurare le impostazioni specifiche di Windows Information Protection (WIP) (precedentemente note come protezione dei dati aziendali).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- Classe MDM_EnterpriseDataProtection_Settings01
- Classe MDM_EnterpriseDataProtection_Settings01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478065"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="9d284-105">\_Classe MDM EnterpriseDataProtection \_ Settings01</span><span class="sxs-lookup"><span data-stu-id="9d284-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="9d284-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9d284-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9d284-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9d284-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9d284-108">La classe **MDM \_ EnterpriseDataProtection \_ Settings01** viene usata per configurare le impostazioni specifiche di Windows Information Protection (WIP) (precedentemente note come protezione dei dati aziendali).</span><span class="sxs-lookup"><span data-stu-id="9d284-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="9d284-109">Per altre informazioni su WIP, vedere [proteggere i dati aziendali mediante EDP (Enterprise Data Protection)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="9d284-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="9d284-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9d284-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d284-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d284-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="9d284-112">Members</span><span class="sxs-lookup"><span data-stu-id="9d284-112">Members</span></span>

<span data-ttu-id="9d284-113">La classe **MDM \_ EnterpriseDataProtection \_ Settings01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d284-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="9d284-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d284-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d284-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d284-115">Properties</span></span>

<span data-ttu-id="9d284-116">La classe **MDM \_ EnterpriseDataProtection \_ Settings01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d284-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9d284-117">AllowAzureRMSForEDP</span><span class="sxs-lookup"><span data-stu-id="9d284-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d284-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-120">AllowUserDecryption</span><span class="sxs-lookup"><span data-stu-id="9d284-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d284-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-123">DataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="9d284-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d284-126">Qualificatori: **OctetString**</span><span class="sxs-lookup"><span data-stu-id="9d284-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="9d284-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d284-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-130">EDPShowIcons</span><span class="sxs-lookup"><span data-stu-id="9d284-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d284-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="9d284-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d284-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d284-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d284-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d284-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d284-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d284-140">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9d284-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="9d284-141">Per questa classe la stringa è "Settings".</span><span class="sxs-lookup"><span data-stu-id="9d284-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="9d284-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9d284-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d284-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d284-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d284-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d284-146">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9d284-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="9d284-147">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="9d284-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="9d284-148">RevokeOnUnenroll</span><span class="sxs-lookup"><span data-stu-id="9d284-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-149">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d284-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-151">RMSTemplateIDForEDP</span><span class="sxs-lookup"><span data-stu-id="9d284-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d284-154">SMBAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="9d284-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d284-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d284-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d284-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d284-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d284-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d284-157">Requirements</span></span>



| <span data-ttu-id="9d284-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d284-158">Requirement</span></span> | <span data-ttu-id="9d284-159">Valore</span><span class="sxs-lookup"><span data-stu-id="9d284-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d284-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d284-160">Minimum supported client</span></span><br/> | <span data-ttu-id="9d284-161">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9d284-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9d284-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d284-162">Minimum supported server</span></span><br/> | <span data-ttu-id="9d284-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9d284-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="9d284-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d284-164">Namespace</span></span><br/>                | <span data-ttu-id="9d284-165">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9d284-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="9d284-166">MOF</span><span class="sxs-lookup"><span data-stu-id="9d284-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d284-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d284-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="9d284-168">DLL</span><span class="sxs-lookup"><span data-stu-id="9d284-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d284-169"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d284-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

