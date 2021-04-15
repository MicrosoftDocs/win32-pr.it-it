---
title: Classe MDM_DeviceStatus_Antivirus01
description: La \_ classe MDM DeviceStatus \_ Antivirus01 viene usata dall'azienda per eseguire query sullo stato della conformità antivirus dei dispositivi con i criteri aziendali.
ms.assetid: 8b3145a6-b836-4750-a0c3-88472f9a12c5
keywords:
- Classe MDM_DeviceStatus_Antivirus01
- Classe MDM_DeviceStatus_Antivirus01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antivirus01
- MDM_DeviceStatus_Antivirus01.InstanceID
- MDM_DeviceStatus_Antivirus01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3197dddb9bea498de63d08a025050963d4348054
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478077"
---
# <a name="mdm_devicestatus_antivirus01-class"></a><span data-ttu-id="35c49-105">\_Classe MDM DeviceStatus \_ Antivirus01</span><span class="sxs-lookup"><span data-stu-id="35c49-105">MDM\_DeviceStatus\_Antivirus01 class</span></span>

<span data-ttu-id="35c49-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="35c49-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="35c49-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="35c49-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="35c49-108">La classe **MDM \_ DeviceStatus \_ Antivirus01** viene usata dall'azienda per eseguire query sullo stato della conformità antivirus dei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="35c49-108">The **MDM\_DeviceStatus\_Antivirus01** class is used by the enterprise to query the state of antivirus compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="35c49-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="35c49-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c49-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35c49-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antivirus01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="35c49-111">Members</span><span class="sxs-lookup"><span data-stu-id="35c49-111">Members</span></span>

<span data-ttu-id="35c49-112">La classe **MDM \_ DeviceStatus \_ Antivirus01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35c49-112">The **MDM\_DeviceStatus\_Antivirus01** class has these types of members:</span></span>

-   [<span data-ttu-id="35c49-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35c49-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35c49-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35c49-114">Properties</span></span>

<span data-ttu-id="35c49-115">La classe **MDM \_ DeviceStatus \_ Antivirus01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="35c49-115">The **MDM\_DeviceStatus\_Antivirus01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35c49-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35c49-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c49-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c49-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c49-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c49-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c49-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35c49-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35c49-120">Nodo per la query antivirus.</span><span class="sxs-lookup"><span data-stu-id="35c49-120">Node for the antivirus query.</span></span>

</dd> <dt>

<span data-ttu-id="35c49-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="35c49-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c49-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c49-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c49-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c49-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c49-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35c49-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35c49-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="35c49-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="35c49-126">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="35c49-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="35c49-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="35c49-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c49-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="35c49-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35c49-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="35c49-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="35c49-130">Status</span><span class="sxs-lookup"><span data-stu-id="35c49-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c49-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="35c49-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35c49-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="35c49-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35c49-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35c49-133">Requirements</span></span>



| <span data-ttu-id="35c49-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c49-134">Requirement</span></span> | <span data-ttu-id="35c49-135">Valore</span><span class="sxs-lookup"><span data-stu-id="35c49-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c49-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35c49-136">Minimum supported client</span></span><br/> | <span data-ttu-id="35c49-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="35c49-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35c49-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35c49-138">Minimum supported server</span></span><br/> | <span data-ttu-id="35c49-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35c49-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="35c49-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35c49-140">Namespace</span></span><br/>                | <span data-ttu-id="35c49-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="35c49-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="35c49-142">MOF</span><span class="sxs-lookup"><span data-stu-id="35c49-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35c49-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35c49-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="35c49-144">DLL</span><span class="sxs-lookup"><span data-stu-id="35c49-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c49-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c49-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

