---
title: Classe MDM_DeviceManageability_Provider01_01
description: La \_ classe MDM DeviceManageability \_ Provider01 \_ 01 viene usata per recuperare le informazioni generali sulle funzionalità di configurazione MDM sul dispositivo.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- Classe MDM_DeviceManageability_Provider01_01
- Classe MDM_DeviceManageability_Provider01_01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874197"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="fb243-105">\_Classe MDM DeviceManageability \_ Provider01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="fb243-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="fb243-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="fb243-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb243-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="fb243-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb243-108">La \_ classe MDM DeviceManageability \_ Provider01 \_ 01 viene usata per recuperare le informazioni generali sulle funzionalità di configurazione MDM sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb243-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="fb243-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fb243-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb243-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb243-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="fb243-111">Members</span><span class="sxs-lookup"><span data-stu-id="fb243-111">Members</span></span>

<span data-ttu-id="fb243-112">La classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fb243-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fb243-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb243-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb243-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb243-114">Properties</span></span>

<span data-ttu-id="fb243-115">La classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb243-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fb243-116">ConfigInfo</span><span class="sxs-lookup"><span data-stu-id="fb243-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb243-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb243-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb243-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fb243-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fb243-119">È necessario impostare il valore su WMI \_ Bridge \_ Server.</span><span class="sxs-lookup"><span data-stu-id="fb243-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="fb243-120">Il chiamante non è in grado di impostare in modo dinamico l'ID del provider.</span><span class="sxs-lookup"><span data-stu-id="fb243-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="fb243-121">EnrollmentInfo</span><span class="sxs-lookup"><span data-stu-id="fb243-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb243-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb243-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb243-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fb243-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb243-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb243-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb243-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb243-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb243-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb243-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb243-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb243-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb243-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fb243-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb243-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb243-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb243-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb243-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb243-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb243-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb243-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb243-132">Requirements</span></span>



| <span data-ttu-id="fb243-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb243-133">Requirement</span></span> | <span data-ttu-id="fb243-134">Valore</span><span class="sxs-lookup"><span data-stu-id="fb243-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb243-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb243-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fb243-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fb243-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb243-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb243-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fb243-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb243-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="fb243-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb243-139">Namespace</span></span><br/>                | <span data-ttu-id="fb243-140">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="fb243-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="fb243-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fb243-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb243-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb243-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb243-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fb243-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb243-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb243-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

