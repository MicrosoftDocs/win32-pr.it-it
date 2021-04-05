---
title: Classe MDM_DeviceStatus_TPM01
description: La \_ classe MDM DeviceStatus \_ TPM01 viene usata dall'azienda per eseguire una query sulla versione TPM dei dispositivi con i criteri aziendali.
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- Classe MDM_DeviceStatus_TPM01
- Classe MDM_DeviceStatus_TPM01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874189"
---
# <a name="mdm_devicestatus_tpm01-class"></a><span data-ttu-id="3694a-105">\_Classe MDM DeviceStatus \_ TPM01</span><span class="sxs-lookup"><span data-stu-id="3694a-105">MDM\_DeviceStatus\_TPM01 class</span></span>

<span data-ttu-id="3694a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3694a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3694a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3694a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3694a-108">La classe **MDM \_ DeviceStatus \_ TPM01** viene usata dall'azienda per eseguire una query sulla versione TPM dei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="3694a-108">The **MDM\_DeviceStatus\_TPM01** class is used by the enterprise to query the TPM version of devices with their enterprise policies.</span></span>

<span data-ttu-id="3694a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3694a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3694a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3694a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a><span data-ttu-id="3694a-111">Members</span><span class="sxs-lookup"><span data-stu-id="3694a-111">Members</span></span>

<span data-ttu-id="3694a-112">La classe **MDM \_ DeviceStatus \_ TPM01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3694a-112">The **MDM\_DeviceStatus\_TPM01** class has these types of members:</span></span>

-   [<span data-ttu-id="3694a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3694a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3694a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3694a-114">Properties</span></span>

<span data-ttu-id="3694a-115">La classe **MDM \_ DeviceStatus \_ TPM01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3694a-115">The **MDM\_DeviceStatus\_TPM01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3694a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3694a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3694a-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3694a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3694a-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3694a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3694a-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3694a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3694a-120">Nodo per la query TPM.</span><span class="sxs-lookup"><span data-stu-id="3694a-120">Node for the TPM query.</span></span>

</dd> <dt>

<span data-ttu-id="3694a-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3694a-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3694a-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3694a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3694a-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3694a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3694a-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3694a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3694a-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="3694a-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="3694a-126">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="3694a-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="3694a-127">SpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="3694a-127">SpecificationVersion</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3694a-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3694a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3694a-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3694a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3694a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3694a-130">Requirements</span></span>



| <span data-ttu-id="3694a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3694a-131">Requirement</span></span> | <span data-ttu-id="3694a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3694a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3694a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3694a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3694a-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3694a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3694a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3694a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3694a-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3694a-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3694a-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3694a-137">Namespace</span></span><br/>                | <span data-ttu-id="3694a-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3694a-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3694a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3694a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3694a-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3694a-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3694a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3694a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3694a-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3694a-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

