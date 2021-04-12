---
title: Classe MDM_Policy_Config01_Bluetooth02
description: La \_ classe Bluetooth02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di gestione Bluetooth disponibili.
ms.assetid: 8544c8df-a57b-4e21-87ee-f819aeddc071
keywords:
- Classe MDM_Policy_Config01_Bluetooth02
- Classe MDM_Policy_Config01_Bluetooth02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Bluetooth02
- MDM_Policy_Config01_Bluetooth02.InstanceID
- MDM_Policy_Config01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceeea1cd099fa00d6138a0ff1d37123725f0be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119423"
---
# <a name="mdm_policy_config01_bluetooth02-class"></a><span data-ttu-id="de989-105">\_ \_ Classe Config01 Bluetooth02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="de989-105">MDM\_Policy\_Config01\_Bluetooth02 class</span></span>

<span data-ttu-id="de989-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="de989-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de989-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="de989-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de989-108">La **classe \_ \_ \_ Bluetooth02 dei criteri MDM Config01** rappresenta i criteri di gestione Bluetooth disponibili.</span><span class="sxs-lookup"><span data-stu-id="de989-108">The **MDM\_Policy\_Config01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="de989-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="de989-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de989-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de989-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="de989-111">Members</span><span class="sxs-lookup"><span data-stu-id="de989-111">Members</span></span>

<span data-ttu-id="de989-112">La **classe \_ \_ Config01 \_ Bluetooth02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="de989-112">The **MDM\_Policy\_Config01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="de989-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="de989-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de989-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="de989-114">Properties</span></span>

<span data-ttu-id="de989-115">La **classe \_ \_ \_ Bluetooth02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="de989-115">The **MDM\_Policy\_Config01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="de989-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="de989-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de989-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de989-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de989-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de989-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="de989-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de989-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de989-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de989-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de989-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="de989-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de989-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de989-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de989-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de989-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de989-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="de989-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de989-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="de989-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de989-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de989-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de989-129">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="de989-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="de989-130">Per questa classe la stringa è "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="de989-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="de989-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="de989-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="de989-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de989-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de989-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de989-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="de989-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="de989-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de989-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="de989-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de989-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de989-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de989-138">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="de989-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="de989-139">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="de989-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="de989-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="de989-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de989-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="de989-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de989-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de989-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de989-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de989-143">Requirements</span></span>



| <span data-ttu-id="de989-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="de989-144">Requirement</span></span> | <span data-ttu-id="de989-145">Valore</span><span class="sxs-lookup"><span data-stu-id="de989-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de989-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de989-146">Minimum supported client</span></span><br/> | <span data-ttu-id="de989-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="de989-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de989-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de989-148">Minimum supported server</span></span><br/> | <span data-ttu-id="de989-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="de989-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de989-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de989-150">Namespace</span></span><br/>                | <span data-ttu-id="de989-151">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="de989-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="de989-152">MOF</span><span class="sxs-lookup"><span data-stu-id="de989-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de989-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de989-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de989-154">DLL</span><span class="sxs-lookup"><span data-stu-id="de989-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de989-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de989-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de989-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de989-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de989-157">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="de989-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

