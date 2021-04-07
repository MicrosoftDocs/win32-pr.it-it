---
title: Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: La \_ classe MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 viene usata per gestire le licenze per le app dello Store.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048587"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="84434-105">\_Classe MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="84434-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="84434-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="84434-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84434-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="84434-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84434-108">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** viene usata per gestire le licenze per le app dello Store.</span><span class="sxs-lookup"><span data-stu-id="84434-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="84434-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="84434-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84434-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84434-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="84434-111">Members</span><span class="sxs-lookup"><span data-stu-id="84434-111">Members</span></span>

<span data-ttu-id="84434-112">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84434-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="84434-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="84434-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="84434-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84434-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84434-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="84434-115">Methods</span></span>

<span data-ttu-id="84434-116">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="84434-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="84434-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="84434-117">Method</span></span>                                                                                                              | <span data-ttu-id="84434-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84434-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="84434-119">**AddLicenseMethod**</span><span class="sxs-lookup"><span data-stu-id="84434-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="84434-120">Metodo per l'aggiunta di una licenza.</span><span class="sxs-lookup"><span data-stu-id="84434-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="84434-121">**GetLicenseFromStoreMethod**</span><span class="sxs-lookup"><span data-stu-id="84434-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="84434-122">Metodo per ottenere una licenza dallo Store.</span><span class="sxs-lookup"><span data-stu-id="84434-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84434-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84434-123">Properties</span></span>

<span data-ttu-id="84434-124">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84434-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84434-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84434-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84434-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84434-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84434-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84434-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84434-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84434-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84434-129">Nodo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84434-129">Optional node.</span></span> <span data-ttu-id="84434-130">ID licenza per un'app Store installata.</span><span class="sxs-lookup"><span data-stu-id="84434-130">License ID for a store installed app.</span></span> <span data-ttu-id="84434-131">L'ID di licenza è in genere il PFN dell'app.</span><span class="sxs-lookup"><span data-stu-id="84434-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="84434-132">Le operazioni supportate sono Add, Get e DELETE.</span><span class="sxs-lookup"><span data-stu-id="84434-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="84434-133">LicenseCategory</span><span class="sxs-lookup"><span data-stu-id="84434-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84434-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84434-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84434-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84434-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84434-136">LicenseUsage</span><span class="sxs-lookup"><span data-stu-id="84434-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84434-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84434-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84434-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84434-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84434-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="84434-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84434-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84434-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84434-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84434-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84434-142">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84434-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84434-143">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="84434-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="84434-144">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span><span class="sxs-lookup"><span data-stu-id="84434-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="84434-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="84434-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84434-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84434-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84434-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84434-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84434-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84434-148">Requirements</span></span>



| <span data-ttu-id="84434-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="84434-149">Requirement</span></span> | <span data-ttu-id="84434-150">Valore</span><span class="sxs-lookup"><span data-stu-id="84434-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84434-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84434-151">Minimum supported client</span></span><br/> | <span data-ttu-id="84434-152">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84434-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84434-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84434-153">Minimum supported server</span></span><br/> | <span data-ttu-id="84434-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="84434-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84434-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84434-155">Namespace</span></span><br/>                | <span data-ttu-id="84434-156">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="84434-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="84434-157">MOF</span><span class="sxs-lookup"><span data-stu-id="84434-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84434-158"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84434-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84434-159">DLL</span><span class="sxs-lookup"><span data-stu-id="84434-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84434-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84434-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84434-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84434-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84434-162">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="84434-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

