---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 avvia la Windows Update Scan e segnala l'ultimo errore di analisi.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225217"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="34b07-105">\_Classe MDM EnterpriseModernAppManagement \_ AppManagement01</span><span class="sxs-lookup"><span data-stu-id="34b07-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="34b07-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="34b07-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="34b07-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="34b07-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="34b07-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** avvia la Windows Update Scan e segnala l'ultimo errore di analisi.</span><span class="sxs-lookup"><span data-stu-id="34b07-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="34b07-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="34b07-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b07-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34b07-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="34b07-111">Members</span><span class="sxs-lookup"><span data-stu-id="34b07-111">Members</span></span>

<span data-ttu-id="34b07-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="34b07-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="34b07-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="34b07-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="34b07-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34b07-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34b07-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="34b07-115">Methods</span></span>

<span data-ttu-id="34b07-116">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="34b07-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="34b07-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="34b07-117">Method</span></span>                                                                                               | <span data-ttu-id="34b07-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34b07-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="34b07-119">**RemovePackageMethod**</span><span class="sxs-lookup"><span data-stu-id="34b07-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="34b07-120">Metodo per la rimozione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="34b07-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="34b07-121">**UpdateScanMethod**</span><span class="sxs-lookup"><span data-stu-id="34b07-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="34b07-122">Metodo per avviare l'analisi del Windows Update.</span><span class="sxs-lookup"><span data-stu-id="34b07-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34b07-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34b07-123">Properties</span></span>

<span data-ttu-id="34b07-124">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="34b07-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="34b07-125">AppInventoryQuery</span><span class="sxs-lookup"><span data-stu-id="34b07-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34b07-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34b07-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="34b07-128">AppInventoryResults</span><span class="sxs-lookup"><span data-stu-id="34b07-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34b07-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34b07-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34b07-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="34b07-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34b07-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34b07-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34b07-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="34b07-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="34b07-135">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="34b07-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="34b07-136">Per questa classe la stringa è "AppManagement".</span><span class="sxs-lookup"><span data-stu-id="34b07-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="34b07-137">LastScanError</span><span class="sxs-lookup"><span data-stu-id="34b07-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="34b07-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34b07-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34b07-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="34b07-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34b07-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34b07-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34b07-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="34b07-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="34b07-144">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="34b07-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="34b07-145">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/"</span><span class="sxs-lookup"><span data-stu-id="34b07-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="34b07-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="34b07-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b07-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34b07-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34b07-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34b07-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34b07-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34b07-149">Requirements</span></span>



| <span data-ttu-id="34b07-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b07-150">Requirement</span></span> | <span data-ttu-id="34b07-151">Valore</span><span class="sxs-lookup"><span data-stu-id="34b07-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b07-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34b07-152">Minimum supported client</span></span><br/> | <span data-ttu-id="34b07-153">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="34b07-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34b07-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34b07-154">Minimum supported server</span></span><br/> | <span data-ttu-id="34b07-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="34b07-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="34b07-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34b07-156">Namespace</span></span><br/>                | <span data-ttu-id="34b07-157">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="34b07-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="34b07-158">MOF</span><span class="sxs-lookup"><span data-stu-id="34b07-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34b07-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34b07-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="34b07-160">DLL</span><span class="sxs-lookup"><span data-stu-id="34b07-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34b07-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34b07-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b07-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34b07-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b07-163">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="34b07-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

