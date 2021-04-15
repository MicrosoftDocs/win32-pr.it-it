---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 02 specifica se si vuole impedire l'aggiornamento di un'app specifica tramite aggiornamenti automatici.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478059"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="5ff3a-105">MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 Class</span><span class="sxs-lookup"><span data-stu-id="5ff3a-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="5ff3a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ff3a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5ff3a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5ff3a-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** specifica se si vuole impedire l'aggiornamento di un'app specifica tramite aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="5ff3a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff3a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ff3a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="5ff3a-111">Members</span><span class="sxs-lookup"><span data-stu-id="5ff3a-111">Members</span></span>

<span data-ttu-id="5ff3a-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ff3a-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="5ff3a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ff3a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ff3a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ff3a-114">Properties</span></span>

<span data-ttu-id="5ff3a-115">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5ff3a-116">DoNotUpdate</span><span class="sxs-lookup"><span data-stu-id="5ff3a-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ff3a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ff3a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ff3a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ff3a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5ff3a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ff3a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ff3a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ff3a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ff3a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ff3a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ff3a-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ff3a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ff3a-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="5ff3a-124">Per questa classe, la stringa corrisponde all'istanza del nome della famiglia di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3a-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5ff3a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ff3a-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ff3a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ff3a-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ff3a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ff3a-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ff3a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ff3a-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5ff3a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="5ff3a-130">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span><span class="sxs-lookup"><span data-stu-id="5ff3a-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ff3a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ff3a-131">Requirements</span></span>



| <span data-ttu-id="5ff3a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff3a-132">Requirement</span></span> | <span data-ttu-id="5ff3a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5ff3a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff3a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ff3a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff3a-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ff3a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ff3a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ff3a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff3a-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ff3a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5ff3a-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ff3a-138">Namespace</span></span><br/>                | <span data-ttu-id="5ff3a-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5ff3a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5ff3a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5ff3a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ff3a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ff3a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ff3a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5ff3a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ff3a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ff3a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff3a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ff3a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff3a-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5ff3a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

