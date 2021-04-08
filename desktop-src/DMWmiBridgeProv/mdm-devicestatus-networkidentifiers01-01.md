---
title: Classe MDM_DeviceStatus_NetworkIdentifiers01_01
description: La \_ classe MDM DeviceStatus \_ NetworkIdentifiers01 \_ 01 consente di eseguire una query su un dispositivo per le proprietà di rete.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530c301894d957c9a9a2db374f35cf7c1bcb5063
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048591"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a><span data-ttu-id="300da-105">\_Classe MDM DeviceStatus \_ NetworkIdentifiers01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="300da-105">MDM\_DeviceStatus\_NetworkIdentifiers01\_01 class</span></span>

<span data-ttu-id="300da-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="300da-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="300da-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="300da-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="300da-108">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** consente di eseguire una query su un dispositivo per le proprietà di rete.</span><span class="sxs-lookup"><span data-stu-id="300da-108">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class allows you to query a device for network properties.</span></span>

<span data-ttu-id="300da-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="300da-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="300da-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="300da-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a><span data-ttu-id="300da-111">Members</span><span class="sxs-lookup"><span data-stu-id="300da-111">Members</span></span>

<span data-ttu-id="300da-112">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="300da-112">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="300da-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="300da-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="300da-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="300da-114">Properties</span></span>

<span data-ttu-id="300da-115">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="300da-115">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="300da-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="300da-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="300da-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="300da-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="300da-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="300da-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="300da-120">Nodo per le query sulle proprietà della rete e del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="300da-120">Node for queries on network and device properties.</span></span>

</dd> <dt>

[<span data-ttu-id="300da-121">IPAddressV4</span><span class="sxs-lookup"><span data-stu-id="300da-121">IPAddressV4</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="300da-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="300da-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="300da-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="300da-124">IPAddressV6</span><span class="sxs-lookup"><span data-stu-id="300da-124">IPAddressV6</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="300da-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="300da-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="300da-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="300da-127">IsConnected</span><span class="sxs-lookup"><span data-stu-id="300da-127">IsConnected</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="300da-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="300da-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="300da-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="300da-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="300da-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="300da-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="300da-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="300da-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="300da-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="300da-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="300da-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="300da-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="300da-135">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="300da-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="300da-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="300da-136">Type</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="300da-137">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="300da-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="300da-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="300da-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="300da-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="300da-139">Requirements</span></span>



| <span data-ttu-id="300da-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="300da-140">Requirement</span></span> | <span data-ttu-id="300da-141">Valore</span><span class="sxs-lookup"><span data-stu-id="300da-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300da-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300da-142">Minimum supported client</span></span><br/> | <span data-ttu-id="300da-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="300da-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="300da-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300da-144">Minimum supported server</span></span><br/> | <span data-ttu-id="300da-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="300da-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="300da-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="300da-146">Namespace</span></span><br/>                | <span data-ttu-id="300da-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="300da-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="300da-148">MOF</span><span class="sxs-lookup"><span data-stu-id="300da-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="300da-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="300da-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="300da-150">DLL</span><span class="sxs-lookup"><span data-stu-id="300da-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="300da-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="300da-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="300da-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="300da-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300da-153">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="300da-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

