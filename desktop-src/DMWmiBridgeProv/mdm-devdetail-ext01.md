---
title: Classe MDM_DevDetail_Ext01
description: La \_ classe MDM DEVDETAIL \_ Ext01 gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- Classe MDM_DevDetail_Ext01
- Classe MDM_DevDetail_Ext01, descritta
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742634"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="5918b-105">\_Classe MDM DEVDETAIL \_ Ext01</span><span class="sxs-lookup"><span data-stu-id="5918b-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="5918b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5918b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5918b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5918b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5918b-108">La classe **MDM \_ DEVDETAIL \_ Ext01** gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.</span><span class="sxs-lookup"><span data-stu-id="5918b-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="5918b-109">Questi parametri del dispositivo non vengono inviati automaticamente dal client al server, ma possono essere sottoposti a query dai server che usano i comandi del DM OMA.</span><span class="sxs-lookup"><span data-stu-id="5918b-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="5918b-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5918b-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5918b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5918b-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="5918b-112">Members</span><span class="sxs-lookup"><span data-stu-id="5918b-112">Members</span></span>

<span data-ttu-id="5918b-113">La classe **MDM \_ DEVDETAIL \_ Ext01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5918b-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="5918b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5918b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5918b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5918b-115">Properties</span></span>

<span data-ttu-id="5918b-116">La classe **MDM \_ DEVDETAIL \_ Ext01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5918b-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5918b-117">DeviceHardwareData</span><span class="sxs-lookup"><span data-stu-id="5918b-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5918b-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5918b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5918b-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5918b-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5918b-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5918b-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5918b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5918b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5918b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5918b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5918b-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5918b-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5918b-124">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5918b-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="5918b-125">Per questa classe la stringa è "EXT"</span><span class="sxs-lookup"><span data-stu-id="5918b-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="5918b-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5918b-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5918b-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5918b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5918b-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5918b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5918b-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5918b-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5918b-130">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5918b-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="5918b-131">Per questa classe la stringa è "./DevDetail/"</span><span class="sxs-lookup"><span data-stu-id="5918b-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="5918b-132">WLANMACAddress</span><span class="sxs-lookup"><span data-stu-id="5918b-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5918b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5918b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5918b-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5918b-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5918b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5918b-135">Requirements</span></span>



| <span data-ttu-id="5918b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5918b-136">Requirement</span></span> | <span data-ttu-id="5918b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5918b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5918b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5918b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5918b-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5918b-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5918b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5918b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5918b-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5918b-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5918b-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5918b-142">Namespace</span></span><br/>                | <span data-ttu-id="5918b-143">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5918b-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5918b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5918b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5918b-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5918b-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5918b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5918b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5918b-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5918b-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5918b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5918b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5918b-149">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5918b-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

