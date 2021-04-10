---
title: Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 viene usata per installare le app da Windows Store o da una posizione ospitata.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964616"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="e59d1-105">\_Classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="e59d1-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="e59d1-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e59d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e59d1-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e59d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e59d1-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** viene usata per installare le app da Windows Store o da una posizione ospitata.</span><span class="sxs-lookup"><span data-stu-id="e59d1-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="e59d1-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e59d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59d1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e59d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="e59d1-111">Members</span><span class="sxs-lookup"><span data-stu-id="e59d1-111">Members</span></span>

<span data-ttu-id="e59d1-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e59d1-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e59d1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e59d1-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e59d1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e59d1-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e59d1-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="e59d1-115">Methods</span></span>

<span data-ttu-id="e59d1-116">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e59d1-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="e59d1-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="e59d1-117">Method</span></span>                                                                                                    | <span data-ttu-id="e59d1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e59d1-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e59d1-119">**HostedInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="e59d1-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="e59d1-120">Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato. può trattarsi di un'unità locale, di un'origine dati UNC o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e59d1-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="e59d1-121">**StoreInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="e59d1-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="e59d1-122">Metodo per eseguire un'installazione di un'app e una licenza da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e59d1-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="e59d1-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e59d1-123">Properties</span></span>

<span data-ttu-id="e59d1-124">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e59d1-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e59d1-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e59d1-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e59d1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e59d1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e59d1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e59d1-129">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e59d1-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="e59d1-130">Per questa classe la stringa è "AppInstallation".</span><span class="sxs-lookup"><span data-stu-id="e59d1-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="e59d1-131">LastError</span><span class="sxs-lookup"><span data-stu-id="e59d1-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e59d1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e59d1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e59d1-134">LastErrorDesc</span><span class="sxs-lookup"><span data-stu-id="e59d1-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e59d1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e59d1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e59d1-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e59d1-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e59d1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e59d1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e59d1-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e59d1-141">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e59d1-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="e59d1-142">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span><span class="sxs-lookup"><span data-stu-id="e59d1-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="e59d1-143">ProgressStatus</span><span class="sxs-lookup"><span data-stu-id="e59d1-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e59d1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e59d1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e59d1-146">Status</span><span class="sxs-lookup"><span data-stu-id="e59d1-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59d1-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e59d1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e59d1-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e59d1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e59d1-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e59d1-149">Requirements</span></span>



| <span data-ttu-id="e59d1-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="e59d1-150">Requirement</span></span> | <span data-ttu-id="e59d1-151">Valore</span><span class="sxs-lookup"><span data-stu-id="e59d1-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e59d1-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e59d1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e59d1-153">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e59d1-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e59d1-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e59d1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e59d1-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e59d1-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e59d1-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e59d1-156">Namespace</span></span><br/>                | <span data-ttu-id="e59d1-157">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e59d1-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e59d1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="e59d1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e59d1-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e59d1-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e59d1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e59d1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e59d1-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e59d1-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59d1-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e59d1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59d1-163">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="e59d1-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

