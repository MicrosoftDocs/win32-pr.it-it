---
title: Classe MDM_DeviceStatus_OS01
description: La \_ classe MDM DeviceStatus \_ OS01 viene usata dall'azienda per eseguire una query sul sistema operativo nei dispositivi con i criteri aziendali.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Classe MDM_DeviceStatus_OS01
- Classe MDM_DeviceStatus_OS01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120651"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="e8d68-105">\_Classe MDM DeviceStatus \_ OS01</span><span class="sxs-lookup"><span data-stu-id="e8d68-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="e8d68-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e8d68-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8d68-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e8d68-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8d68-108">La classe **MDM \_ DeviceStatus \_ OS01** viene usata dall'azienda per eseguire una query sul sistema operativo nei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="e8d68-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="e8d68-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e8d68-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d68-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8d68-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="e8d68-111">Members</span><span class="sxs-lookup"><span data-stu-id="e8d68-111">Members</span></span>

<span data-ttu-id="e8d68-112">La classe **MDM \_ DeviceStatus \_ OS01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e8d68-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="e8d68-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8d68-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8d68-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8d68-114">Properties</span></span>

<span data-ttu-id="e8d68-115">La classe **MDM \_ DeviceStatus \_ OS01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e8d68-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e8d68-116">Edizione</span><span class="sxs-lookup"><span data-stu-id="e8d68-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d68-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e8d68-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d68-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e8d68-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8d68-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d68-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e8d68-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d68-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8d68-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d68-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8d68-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e8d68-123">Nodo per la query del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8d68-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="e8d68-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d68-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e8d68-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d68-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8d68-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d68-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8d68-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e8d68-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e8d68-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="e8d68-129">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="e8d68-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8d68-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8d68-130">Requirements</span></span>



| <span data-ttu-id="e8d68-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d68-131">Requirement</span></span> | <span data-ttu-id="e8d68-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e8d68-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d68-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d68-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d68-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8d68-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8d68-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d68-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d68-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e8d68-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e8d68-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8d68-137">Namespace</span></span><br/>                | <span data-ttu-id="e8d68-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e8d68-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e8d68-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e8d68-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8d68-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8d68-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8d68-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e8d68-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8d68-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8d68-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

