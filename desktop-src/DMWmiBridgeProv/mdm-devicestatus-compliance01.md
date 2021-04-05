---
title: Classe MDM_DeviceStatus_Compliance01
description: La \_ classe MDM DeviceStatus \_ Compliance01 consente di eseguire una query per verificare se i dispositivi sono conformi ai criteri di crittografia dell'organizzazione.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- Classe MDM_DeviceStatus_Compliance01
- Classe MDM_DeviceStatus_Compliance01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120655"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="f4e3e-105">\_Classe MDM DeviceStatus \_ Compliance01</span><span class="sxs-lookup"><span data-stu-id="f4e3e-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="f4e3e-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f4e3e-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f4e3e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f4e3e-108">La classe **MDM \_ DeviceStatus \_ Compliance01** consente di eseguire una query per verificare se i dispositivi sono conformi ai criteri di crittografia dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="f4e3e-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e3e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4e3e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="f4e3e-111">Members</span><span class="sxs-lookup"><span data-stu-id="f4e3e-111">Members</span></span>

<span data-ttu-id="f4e3e-112">La classe **MDM \_ DeviceStatus \_ Compliance01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f4e3e-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="f4e3e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f4e3e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4e3e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f4e3e-114">Properties</span></span>

<span data-ttu-id="f4e3e-115">La classe **MDM \_ DeviceStatus \_ Compliance01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f4e3e-116">EncryptionCompliance</span><span class="sxs-lookup"><span data-stu-id="f4e3e-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e3e-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f4e3e-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4e3e-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f4e3e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4e3e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f4e3e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e3e-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e3e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e3e-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e3e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4e3e-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4e3e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4e3e-123">Nodo per le query sulla conformità.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="f4e3e-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f4e3e-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4e3e-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f4e3e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4e3e-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f4e3e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4e3e-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4e3e-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4e3e-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="f4e3e-129">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="f4e3e-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4e3e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4e3e-130">Requirements</span></span>



| <span data-ttu-id="f4e3e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e3e-131">Requirement</span></span> | <span data-ttu-id="f4e3e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e3e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e3e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e3e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e3e-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f4e3e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4e3e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e3e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e3e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f4e3e-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f4e3e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f4e3e-137">Namespace</span></span><br/>                | <span data-ttu-id="f4e3e-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f4e3e-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f4e3e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f4e3e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4e3e-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4e3e-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4e3e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f4e3e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4e3e-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4e3e-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e3e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4e3e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e3e-144">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f4e3e-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

