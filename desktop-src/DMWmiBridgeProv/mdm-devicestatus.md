---
title: Classe MDM_DeviceStatus
description: La \_ classe MDM DeviceStatus viene usata dall'azienda per tenere traccia dell'inventario dei dispositivi ed eseguire query sullo stato di conformità di questi dispositivi con i criteri aziendali.
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- Classe MDM_DeviceStatus
- Classe MDM_DeviceStatus, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120647"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="6fb77-105">MDM \_ DeviceStatus (classe)</span><span class="sxs-lookup"><span data-stu-id="6fb77-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="6fb77-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6fb77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6fb77-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6fb77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6fb77-108">La classe **MDM \_ DeviceStatus** viene usata dall'azienda per tenere traccia dell'inventario dei dispositivi ed eseguire query sullo stato di conformità di questi dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="6fb77-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="6fb77-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6fb77-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb77-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fb77-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="6fb77-111">Members</span><span class="sxs-lookup"><span data-stu-id="6fb77-111">Members</span></span>

<span data-ttu-id="6fb77-112">La classe **MDM \_ DeviceStatus** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6fb77-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="6fb77-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fb77-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fb77-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fb77-114">Properties</span></span>

<span data-ttu-id="6fb77-115">La classe **MDM \_ DeviceStatus** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6fb77-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6fb77-116">NomeDominio</span><span class="sxs-lookup"><span data-stu-id="6fb77-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb77-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fb77-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6fb77-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6fb77-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6fb77-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb77-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fb77-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fb77-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6fb77-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6fb77-123">Nodo radice per il provider del servizio di configurazione DeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="6fb77-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="6fb77-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6fb77-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb77-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fb77-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fb77-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6fb77-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6fb77-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6fb77-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="6fb77-129">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="6fb77-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="6fb77-130">SecureBootState</span><span class="sxs-lookup"><span data-stu-id="6fb77-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb77-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6fb77-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb77-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6fb77-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fb77-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fb77-133">Requirements</span></span>



| <span data-ttu-id="6fb77-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb77-134">Requirement</span></span> | <span data-ttu-id="6fb77-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6fb77-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb77-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fb77-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb77-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6fb77-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fb77-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fb77-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb77-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6fb77-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6fb77-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fb77-140">Namespace</span></span><br/>                | <span data-ttu-id="6fb77-141">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6fb77-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6fb77-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6fb77-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fb77-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fb77-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fb77-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb77-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fb77-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb77-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb77-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fb77-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb77-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="6fb77-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

