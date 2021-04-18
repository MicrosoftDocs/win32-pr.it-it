---
title: Classe MDM_DeviceStatus_Battery01
description: La \_ classe MDM DeviceStatus \_ Battery01 viene usata dall'azienda per eseguire query sullo stato della conformità della batteria dei dispositivi con i criteri aziendali.
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- Classe MDM_DeviceStatus_Battery01
- Classe MDM_DeviceStatus_Battery01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302120"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="f234b-105">\_Classe MDM DeviceStatus \_ Battery01</span><span class="sxs-lookup"><span data-stu-id="f234b-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="f234b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f234b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f234b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f234b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f234b-108">La classe **MDM \_ DeviceStatus \_ Battery01** viene usata dall'azienda per eseguire query sullo stato della conformità della batteria dei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="f234b-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="f234b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f234b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f234b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f234b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="f234b-111">Members</span><span class="sxs-lookup"><span data-stu-id="f234b-111">Members</span></span>

<span data-ttu-id="f234b-112">La classe **MDM \_ DeviceStatus \_ Battery01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f234b-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="f234b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f234b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f234b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f234b-114">Properties</span></span>

<span data-ttu-id="f234b-115">La classe **MDM \_ DeviceStatus \_ Battery01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f234b-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f234b-116">EstimatedChargeRemaining</span><span class="sxs-lookup"><span data-stu-id="f234b-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f234b-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f234b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f234b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f234b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f234b-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="f234b-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f234b-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f234b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f234b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f234b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f234b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f234b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f234b-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f234b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f234b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f234b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f234b-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f234b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f234b-126">Nodo per la query della batteria.</span><span class="sxs-lookup"><span data-stu-id="f234b-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="f234b-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f234b-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f234b-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f234b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f234b-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f234b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f234b-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f234b-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f234b-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f234b-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="f234b-132">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="f234b-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="f234b-133">Status</span><span class="sxs-lookup"><span data-stu-id="f234b-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f234b-134">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f234b-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f234b-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f234b-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f234b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f234b-136">Requirements</span></span>



| <span data-ttu-id="f234b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f234b-137">Requirement</span></span> | <span data-ttu-id="f234b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="f234b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f234b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f234b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f234b-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f234b-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f234b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f234b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f234b-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f234b-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f234b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f234b-143">Namespace</span></span><br/>                | <span data-ttu-id="f234b-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f234b-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f234b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f234b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f234b-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f234b-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f234b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f234b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f234b-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f234b-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

