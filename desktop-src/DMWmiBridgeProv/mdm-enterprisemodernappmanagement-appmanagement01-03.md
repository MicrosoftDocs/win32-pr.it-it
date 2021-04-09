---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03 fornisce informazioni specifiche sull'app, ad esempio il nome, la versione e il server di pubblicazione.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120642"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="452a5-105">\_Classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03</span><span class="sxs-lookup"><span data-stu-id="452a5-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="452a5-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="452a5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="452a5-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="452a5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="452a5-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** fornisce informazioni specifiche sull'app, ad esempio il nome, la versione e il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="452a5-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="452a5-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="452a5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="452a5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="452a5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="452a5-111">Members</span><span class="sxs-lookup"><span data-stu-id="452a5-111">Members</span></span>

<span data-ttu-id="452a5-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="452a5-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="452a5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="452a5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="452a5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="452a5-114">Properties</span></span>

<span data-ttu-id="452a5-115">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="452a5-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="452a5-116">Architettura</span><span class="sxs-lookup"><span data-stu-id="452a5-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="452a5-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="452a5-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="452a5-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="452a5-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="452a5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452a5-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="452a5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="452a5-129">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="452a5-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="452a5-130">Per questa classe, la stringa corrisponde all'istanza del nome completo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="452a5-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="452a5-131">Aggregazione</span><span class="sxs-lookup"><span data-stu-id="452a5-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="452a5-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-134">Framework</span><span class="sxs-lookup"><span data-stu-id="452a5-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="452a5-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-137">Con provisioning</span><span class="sxs-lookup"><span data-stu-id="452a5-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="452a5-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-140">Nome</span><span class="sxs-lookup"><span data-stu-id="452a5-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-143">PackageStatus</span><span class="sxs-lookup"><span data-stu-id="452a5-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="452a5-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="452a5-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="452a5-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="452a5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452a5-149">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="452a5-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="452a5-150">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="452a5-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="452a5-151">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID* / *packageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="452a5-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="452a5-152">Autore</span><span class="sxs-lookup"><span data-stu-id="452a5-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-155">RequiresReinstall</span><span class="sxs-lookup"><span data-stu-id="452a5-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="452a5-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="452a5-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-161">Utenti</span><span class="sxs-lookup"><span data-stu-id="452a5-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="452a5-164">Versione</span><span class="sxs-lookup"><span data-stu-id="452a5-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="452a5-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="452a5-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452a5-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="452a5-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="452a5-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="452a5-167">Requirements</span></span>



| <span data-ttu-id="452a5-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="452a5-168">Requirement</span></span> | <span data-ttu-id="452a5-169">Valore</span><span class="sxs-lookup"><span data-stu-id="452a5-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="452a5-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452a5-170">Minimum supported client</span></span><br/> | <span data-ttu-id="452a5-171">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="452a5-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="452a5-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452a5-172">Minimum supported server</span></span><br/> | <span data-ttu-id="452a5-173">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="452a5-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="452a5-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="452a5-174">Namespace</span></span><br/>                | <span data-ttu-id="452a5-175">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="452a5-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="452a5-176">MOF</span><span class="sxs-lookup"><span data-stu-id="452a5-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="452a5-177"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="452a5-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="452a5-178">DLL</span><span class="sxs-lookup"><span data-stu-id="452a5-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="452a5-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="452a5-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452a5-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="452a5-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452a5-181">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="452a5-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

