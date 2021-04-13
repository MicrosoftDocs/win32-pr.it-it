---
title: Classe MDM_Reboot_Schedule01
description: Il \_ Schedule01class di riavvio MDM \_ viene usato per configurare un momento specifico per il riavvio di un dispositivo.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Classe MDM_Reboot_Schedule01
- Classe MDM_Reboot_Schedule01, descritta
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475292"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="217d9-105">\_Classe Schedule01 di riavvio MDM \_</span><span class="sxs-lookup"><span data-stu-id="217d9-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="217d9-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="217d9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="217d9-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="217d9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="217d9-108">La **classe \_ \_ Schedule01 di riavvio MDM** viene usata per configurare un momento specifico per il riavvio di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="217d9-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="217d9-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="217d9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="217d9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="217d9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="217d9-111">Members</span><span class="sxs-lookup"><span data-stu-id="217d9-111">Members</span></span>

<span data-ttu-id="217d9-112">La **classe \_ \_ Schedule01 di riavvio MDM** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="217d9-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="217d9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="217d9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="217d9-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="217d9-114">Properties</span></span>

<span data-ttu-id="217d9-115">La **classe \_ \_ Schedule01 per il riavvio MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="217d9-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="217d9-116">DailyRecurrent</span><span class="sxs-lookup"><span data-stu-id="217d9-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="217d9-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="217d9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217d9-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="217d9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="217d9-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="217d9-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="217d9-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="217d9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217d9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="217d9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="217d9-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="217d9-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="217d9-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="217d9-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="217d9-124">Per questa classe la stringa è "Schedule".</span><span class="sxs-lookup"><span data-stu-id="217d9-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="217d9-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="217d9-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="217d9-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="217d9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217d9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="217d9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="217d9-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="217d9-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="217d9-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="217d9-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="217d9-130">Per questa classe la stringa è "./Vendor/MSFT/Reboot"</span><span class="sxs-lookup"><span data-stu-id="217d9-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="217d9-131">Singolo</span><span class="sxs-lookup"><span data-stu-id="217d9-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="217d9-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="217d9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="217d9-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="217d9-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="217d9-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="217d9-134">Requirements</span></span>



| <span data-ttu-id="217d9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="217d9-135">Requirement</span></span> | <span data-ttu-id="217d9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="217d9-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217d9-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="217d9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="217d9-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="217d9-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="217d9-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="217d9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="217d9-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="217d9-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="217d9-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="217d9-141">Namespace</span></span><br/>                | <span data-ttu-id="217d9-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="217d9-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="217d9-143">MOF</span><span class="sxs-lookup"><span data-stu-id="217d9-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="217d9-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="217d9-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="217d9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="217d9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="217d9-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="217d9-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

