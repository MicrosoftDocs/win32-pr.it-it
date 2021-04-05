---
title: Classe MDM_DeviceStatus_Antispyware01
description: La \_ classe MDM DeviceStatus \_ Antispyware01 viene usata dall'azienda per eseguire query sullo stato della conformità antispyware dei dispositivi con i criteri aziendali.
ms.assetid: 53275aa1-ff7d-4630-b6c5-aedce3f4665a
keywords:
- Classe MDM_DeviceStatus_Antispyware01
- Classe MDM_DeviceStatus_Antispyware01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01.InstanceID
- MDM_DeviceStatus_Antispyware01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91468c98981c93e211b3e3bee99564574f7a56cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874194"
---
# <a name="mdm_devicestatus_antispyware01-class"></a><span data-ttu-id="be7de-105">\_Classe MDM DeviceStatus \_ Antispyware01</span><span class="sxs-lookup"><span data-stu-id="be7de-105">MDM\_DeviceStatus\_Antispyware01 class</span></span>

<span data-ttu-id="be7de-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="be7de-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="be7de-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="be7de-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="be7de-108">La classe **MDM \_ DeviceStatus \_ Antispyware01** viene usata dall'azienda per eseguire query sullo stato della conformità antispyware dei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="be7de-108">The **MDM\_DeviceStatus\_Antispyware01** class is used by the enterprise to query the state of antispyware compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="be7de-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="be7de-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7de-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be7de-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antispyware01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="be7de-111">Members</span><span class="sxs-lookup"><span data-stu-id="be7de-111">Members</span></span>

<span data-ttu-id="be7de-112">La classe **MDM \_ DeviceStatus \_ Antispyware01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="be7de-112">The **MDM\_DeviceStatus\_Antispyware01** class has these types of members:</span></span>

-   [<span data-ttu-id="be7de-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="be7de-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be7de-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="be7de-114">Properties</span></span>

<span data-ttu-id="be7de-115">La classe **MDM \_ DeviceStatus \_ Antispyware01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="be7de-115">The **MDM\_DeviceStatus\_Antispyware01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be7de-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be7de-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7de-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be7de-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7de-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be7de-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7de-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be7de-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="be7de-120">Nodo per la query antispyware.</span><span class="sxs-lookup"><span data-stu-id="be7de-120">Node for the antispyware query.</span></span>

</dd> <dt>

<span data-ttu-id="be7de-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="be7de-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7de-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be7de-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be7de-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be7de-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be7de-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be7de-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="be7de-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="be7de-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="be7de-126">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="be7de-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="be7de-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="be7de-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7de-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="be7de-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7de-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="be7de-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be7de-130">Status</span><span class="sxs-lookup"><span data-stu-id="be7de-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be7de-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="be7de-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="be7de-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="be7de-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be7de-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be7de-133">Requirements</span></span>



| <span data-ttu-id="be7de-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7de-134">Requirement</span></span> | <span data-ttu-id="be7de-135">Valore</span><span class="sxs-lookup"><span data-stu-id="be7de-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7de-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be7de-136">Minimum supported client</span></span><br/> | <span data-ttu-id="be7de-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="be7de-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be7de-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be7de-138">Minimum supported server</span></span><br/> | <span data-ttu-id="be7de-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="be7de-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="be7de-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="be7de-140">Namespace</span></span><br/>                | <span data-ttu-id="be7de-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="be7de-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="be7de-142">MOF</span><span class="sxs-lookup"><span data-stu-id="be7de-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be7de-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be7de-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="be7de-144">DLL</span><span class="sxs-lookup"><span data-stu-id="be7de-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7de-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7de-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

