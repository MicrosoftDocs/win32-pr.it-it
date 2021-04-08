---
title: Classe MDM_DeviceStatus_CellularIdentities01_01
description: La \_ classe MDM DeviceStatus \_ CellularIdentities01 \_ 01 consente di eseguire una query per verificare se i dispositivi sono conformi ai criteri di crittografia dell'organizzazione.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- Classe MDM_DeviceStatus_CellularIdentities01_01
- Classe MDM_DeviceStatus_CellularIdentities01_01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874193"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="c5c81-105">\_Classe MDM DeviceStatus \_ CellularIdentities01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="c5c81-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="c5c81-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c5c81-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c5c81-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c5c81-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c5c81-108">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** consente di eseguire una query per verificare se i dispositivi sono conformi ai criteri di crittografia dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c5c81-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="c5c81-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c5c81-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c81-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5c81-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="c5c81-111">Members</span><span class="sxs-lookup"><span data-stu-id="c5c81-111">Members</span></span>

<span data-ttu-id="c5c81-112">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c5c81-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c5c81-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5c81-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5c81-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5c81-114">Properties</span></span>

<span data-ttu-id="c5c81-115">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5c81-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c5c81-116">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="c5c81-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c81-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="c5c81-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c81-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="c5c81-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5c81-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c5c81-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5c81-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5c81-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5c81-129">Nodo per le query sulle schede SIM.</span><span class="sxs-lookup"><span data-stu-id="c5c81-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="c5c81-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c5c81-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5c81-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5c81-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5c81-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c5c81-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="c5c81-135">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="c5c81-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="c5c81-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c5c81-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5c81-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c81-139">RoamingCompliance</span><span class="sxs-lookup"><span data-stu-id="c5c81-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5c81-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c81-142">RoamingStatus</span><span class="sxs-lookup"><span data-stu-id="c5c81-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c81-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5c81-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5c81-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c5c81-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5c81-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5c81-145">Requirements</span></span>



| <span data-ttu-id="c5c81-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c81-146">Requirement</span></span> | <span data-ttu-id="c5c81-147">Valore</span><span class="sxs-lookup"><span data-stu-id="c5c81-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c81-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c81-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c81-149">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c5c81-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5c81-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c81-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c81-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c5c81-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c5c81-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5c81-152">Namespace</span></span><br/>                | <span data-ttu-id="c5c81-153">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c5c81-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c5c81-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c5c81-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5c81-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5c81-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5c81-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c5c81-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c81-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c81-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c81-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5c81-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c81-159">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="c5c81-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

