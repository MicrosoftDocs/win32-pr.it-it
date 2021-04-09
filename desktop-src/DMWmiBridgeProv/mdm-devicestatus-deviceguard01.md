---
title: Classe MDM_DeviceStatus_DeviceGuard01
description: La \_ classe MDM DeviceStatus \_ DeviceGuard01 viene usata dall'azienda per tenere traccia dell'inventario dei dispositivi ed eseguire query sullo stato di conformità di questi dispositivi con i criteri aziendali.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- Classe MDM_DeviceStatus_DeviceGuard01
- Classe MDM_DeviceStatus_DeviceGuard01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964620"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="c9506-105">\_Classe MDM DeviceStatus \_ DeviceGuard01</span><span class="sxs-lookup"><span data-stu-id="c9506-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="c9506-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c9506-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c9506-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c9506-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c9506-108">La \_ classe MDM DeviceStatus \_ DeviceGuard01 viene usata dall'azienda per tenere traccia dell'inventario dei dispositivi ed eseguire query sullo stato di conformità di questi dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="c9506-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="c9506-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c9506-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9506-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9506-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="c9506-111">Members</span><span class="sxs-lookup"><span data-stu-id="c9506-111">Members</span></span>

<span data-ttu-id="c9506-112">La classe **MDM \_ DeviceStatus \_ DeviceGuard01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c9506-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="c9506-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9506-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9506-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9506-114">Properties</span></span>

<span data-ttu-id="c9506-115">La classe **MDM \_ DeviceStatus \_ DeviceGuard01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9506-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9506-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9506-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9506-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c9506-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9506-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c9506-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9506-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9506-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9506-120">LsaCfgCredGuardStatus</span><span class="sxs-lookup"><span data-stu-id="c9506-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9506-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c9506-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9506-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9506-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9506-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c9506-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9506-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c9506-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9506-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c9506-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9506-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9506-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9506-127">VirtualizationBasedSecurityHwReq</span><span class="sxs-lookup"><span data-stu-id="c9506-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9506-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c9506-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9506-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9506-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9506-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="c9506-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9506-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c9506-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9506-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9506-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9506-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9506-133">Requirements</span></span>



| <span data-ttu-id="c9506-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9506-134">Requirement</span></span> | <span data-ttu-id="c9506-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c9506-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9506-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9506-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c9506-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c9506-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9506-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9506-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c9506-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c9506-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c9506-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c9506-140">Namespace</span></span><br/>                | <span data-ttu-id="c9506-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c9506-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c9506-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c9506-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9506-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9506-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c9506-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9506-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

