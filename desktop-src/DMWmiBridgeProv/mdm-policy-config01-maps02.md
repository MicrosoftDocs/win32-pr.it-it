---
title: Classe MDM_Policy_Config01_Maps02
description: La \_ \_ classe Config01 Maps02 dei criteri MDM \_ rappresenta i criteri della mappa disponibili.
ms.assetid: d2965f1f-a858-4b43-9c46-17ba718291b1
keywords:
- Classe MDM_Policy_Config01_Maps02
- Classe MDM_Policy_Config01_Maps02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Maps02
- MDM_Policy_Config01_Maps02.InstanceID
- MDM_Policy_Config01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090c8d077b3df4446054d29a8100a32923932736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119723"
---
# <a name="mdm_policy_config01_maps02-class"></a><span data-ttu-id="77cee-105">\_ \_ Classe Config01 Maps02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="77cee-105">MDM\_Policy\_Config01\_Maps02 class</span></span>

<span data-ttu-id="77cee-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="77cee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="77cee-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="77cee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="77cee-108">La **classe \_ \_ Config01 \_ Maps02 dei criteri MDM** rappresenta i criteri della mappa disponibili.</span><span class="sxs-lookup"><span data-stu-id="77cee-108">The **MDM\_Policy\_Config01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="77cee-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="77cee-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cee-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77cee-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="77cee-111">Members</span><span class="sxs-lookup"><span data-stu-id="77cee-111">Members</span></span>

<span data-ttu-id="77cee-112">La **classe \_ \_ Config01 \_ Maps02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="77cee-112">The **MDM\_Policy\_Config01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="77cee-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77cee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77cee-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77cee-114">Properties</span></span>

<span data-ttu-id="77cee-115">La **classe \_ \_ \_ Maps02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="77cee-115">The **MDM\_Policy\_Config01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="77cee-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="77cee-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cee-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="77cee-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="77cee-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77cee-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77cee-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="77cee-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cee-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="77cee-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="77cee-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77cee-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77cee-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77cee-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cee-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77cee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cee-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77cee-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cee-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77cee-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77cee-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="77cee-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="77cee-127">Per questa classe la stringa è "Maps".</span><span class="sxs-lookup"><span data-stu-id="77cee-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="77cee-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="77cee-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77cee-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77cee-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77cee-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77cee-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77cee-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77cee-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77cee-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="77cee-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="77cee-133">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="77cee-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77cee-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77cee-134">Requirements</span></span>



| <span data-ttu-id="77cee-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="77cee-135">Requirement</span></span> | <span data-ttu-id="77cee-136">Valore</span><span class="sxs-lookup"><span data-stu-id="77cee-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77cee-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77cee-137">Minimum supported client</span></span><br/> | <span data-ttu-id="77cee-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="77cee-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="77cee-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77cee-139">Minimum supported server</span></span><br/> | <span data-ttu-id="77cee-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77cee-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="77cee-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77cee-141">Namespace</span></span><br/>                | <span data-ttu-id="77cee-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="77cee-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="77cee-143">MOF</span><span class="sxs-lookup"><span data-stu-id="77cee-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77cee-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77cee-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="77cee-145">DLL</span><span class="sxs-lookup"><span data-stu-id="77cee-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77cee-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="77cee-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

