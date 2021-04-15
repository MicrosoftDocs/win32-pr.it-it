---
title: Classe MDM_Policy_Result01_Maps02
description: La \_ \_ classe Result01 Maps02 dei criteri MDM \_ rappresenta i criteri della mappa disponibili.
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- Classe MDM_Policy_Result01_Maps02
- Classe MDM_Policy_Result01_Maps02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476270"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="bdd0f-105">\_ \_ Classe Result01 Maps02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="bdd0f-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="bdd0f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bdd0f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="bdd0f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bdd0f-108">La **classe \_ \_ Result01 \_ Maps02 dei criteri MDM** rappresenta i criteri della mappa disponibili.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="bdd0f-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd0f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdd0f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="bdd0f-111">Members</span><span class="sxs-lookup"><span data-stu-id="bdd0f-111">Members</span></span>

<span data-ttu-id="bdd0f-112">La **classe \_ \_ Result01 \_ Maps02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bdd0f-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="bdd0f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bdd0f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bdd0f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bdd0f-114">Properties</span></span>

<span data-ttu-id="bdd0f-115">La **classe \_ \_ \_ Maps02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bdd0f-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="bdd0f-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdd0f-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bdd0f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bdd0f-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bdd0f-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdd0f-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bdd0f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bdd0f-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdd0f-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bdd0f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bdd0f-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bdd0f-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="bdd0f-127">Per questa classe la stringa è "Maps".</span><span class="sxs-lookup"><span data-stu-id="bdd0f-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="bdd0f-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdd0f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bdd0f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bdd0f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bdd0f-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bdd0f-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bdd0f-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="bdd0f-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="bdd0f-133">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="bdd0f-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdd0f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdd0f-134">Requirements</span></span>



| <span data-ttu-id="bdd0f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd0f-135">Requirement</span></span> | <span data-ttu-id="bdd0f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bdd0f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd0f-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdd0f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd0f-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bdd0f-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bdd0f-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdd0f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd0f-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bdd0f-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="bdd0f-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bdd0f-141">Namespace</span></span><br/>                | <span data-ttu-id="bdd0f-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="bdd0f-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="bdd0f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bdd0f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdd0f-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdd0f-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="bdd0f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bdd0f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdd0f-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bdd0f-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

