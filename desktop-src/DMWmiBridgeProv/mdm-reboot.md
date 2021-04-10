---
title: Classe MDM_Reboot
description: Il \_ REBOOTCLASS MDM viene usato per configurare le impostazioni di riavvio.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- Classe MDM_Reboot
- Classe MDM_Reboot, descritta
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047900"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="9fd12-105">\_Classe di riavvio MDM</span><span class="sxs-lookup"><span data-stu-id="9fd12-105">MDM\_Reboot class</span></span>

<span data-ttu-id="9fd12-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9fd12-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9fd12-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9fd12-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9fd12-108">La classe di **\_ riavvio MDM** viene utilizzata per configurare le impostazioni di riavvio.</span><span class="sxs-lookup"><span data-stu-id="9fd12-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="9fd12-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9fd12-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd12-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fd12-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="9fd12-111">Members</span><span class="sxs-lookup"><span data-stu-id="9fd12-111">Members</span></span>

<span data-ttu-id="9fd12-112">La classe di **\_ riavvio MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9fd12-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="9fd12-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="9fd12-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9fd12-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fd12-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9fd12-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="9fd12-115">Methods</span></span>

<span data-ttu-id="9fd12-116">La classe di **\_ riavvio MDM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9fd12-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="9fd12-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="9fd12-117">Method</span></span>                                                | <span data-ttu-id="9fd12-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fd12-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="9fd12-119">**RebootNowMethod**</span><span class="sxs-lookup"><span data-stu-id="9fd12-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="9fd12-120">Questo metodo esegue un riavvio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fd12-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9fd12-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fd12-121">Properties</span></span>

<span data-ttu-id="9fd12-122">La classe di **\_ riavvio MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9fd12-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fd12-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9fd12-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fd12-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9fd12-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fd12-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fd12-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fd12-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9fd12-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9fd12-127">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9fd12-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="9fd12-128">Per questa classe la stringa è "reboot".</span><span class="sxs-lookup"><span data-stu-id="9fd12-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="9fd12-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9fd12-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fd12-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9fd12-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fd12-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fd12-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fd12-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9fd12-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9fd12-133">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9fd12-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="9fd12-134">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="9fd12-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fd12-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fd12-135">Requirements</span></span>



| <span data-ttu-id="9fd12-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd12-136">Requirement</span></span> | <span data-ttu-id="9fd12-137">Valore</span><span class="sxs-lookup"><span data-stu-id="9fd12-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd12-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fd12-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd12-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9fd12-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9fd12-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fd12-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd12-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9fd12-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="9fd12-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fd12-142">Namespace</span></span><br/>                | <span data-ttu-id="9fd12-143">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9fd12-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="9fd12-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9fd12-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fd12-145"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fd12-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="9fd12-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9fd12-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fd12-147"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9fd12-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

