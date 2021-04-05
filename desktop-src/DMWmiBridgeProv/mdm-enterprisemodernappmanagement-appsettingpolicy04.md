---
title: Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppSettingPolicy04 specifica tutti i valori delle impostazioni dell'app gestita.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048588"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="9e9cb-105">\_Classe MDM EnterpriseModernAppManagement \_ AppSettingPolicy04</span><span class="sxs-lookup"><span data-stu-id="9e9cb-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="9e9cb-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9e9cb-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9e9cb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9e9cb-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04** specifica tutti i valori delle impostazioni dell'app gestita.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="9e9cb-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9cb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e9cb-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="9e9cb-111">Members</span><span class="sxs-lookup"><span data-stu-id="9e9cb-111">Members</span></span>

<span data-ttu-id="9e9cb-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e9cb-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="9e9cb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e9cb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e9cb-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e9cb-114">Properties</span></span>

<span data-ttu-id="9e9cb-115">La classe **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e9cb-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9cb-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e9cb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e9cb-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9e9cb-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="9e9cb-121">Per questa classe, la stringa "AppSettingPolicy".</span><span class="sxs-lookup"><span data-stu-id="9e9cb-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="9e9cb-122">IsVariableLeaf</span><span class="sxs-lookup"><span data-stu-id="9e9cb-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9cb-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e9cb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e9cb-125">Aggiunta in Windows 10, versione 1511.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="9e9cb-126">**SettingValue** e i dati rappresentano una coppia chiave-valore da configurare per l'app.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="9e9cb-127">Il nodo rappresenta il nome della chiave e i dati rappresentano il valore.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="9e9cb-128">È possibile trovare questo valore in LocalSettings nel contenitore Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="9e9cb-129">Questa impostazione funziona solo per le app che supportano la funzionalità ed è supportata solo nel contesto utente.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="9e9cb-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9cb-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e9cb-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e9cb-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9e9cb-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9e9cb-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="9e9cb-135">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*packageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="9e9cb-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="9e9cb-136">**Valore**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9cb-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e9cb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e9cb-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9e9cb-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e9cb-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e9cb-139">Requirements</span></span>



| <span data-ttu-id="9e9cb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9cb-140">Requirement</span></span> | <span data-ttu-id="9e9cb-141">Valore</span><span class="sxs-lookup"><span data-stu-id="9e9cb-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9cb-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e9cb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9cb-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9e9cb-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e9cb-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e9cb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9cb-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9e9cb-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9e9cb-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e9cb-146">Namespace</span></span><br/>                | <span data-ttu-id="9e9cb-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9e9cb-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9e9cb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9e9cb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e9cb-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e9cb-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e9cb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9cb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e9cb-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9cb-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9cb-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e9cb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9cb-153">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9e9cb-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

