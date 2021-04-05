---
title: Classe MDM_Policy_Result01_Storage02
description: La \_ classe Storage02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di archiviazione disponibili.
ms.assetid: e0e3b867-38b5-4b10-a13e-6f99b8ff6db3
keywords:
- Classe MDM_Policy_Result01_Storage02
- Classe MDM_Policy_Result01_Storage02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Storage02
- MDM_Policy_Result01_Storage02.InstanceID
- MDM_Policy_Result01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63381b34c88ebc590577eec9a11f603ea5325649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048243"
---
# <a name="mdm_policy_result01_storage02-class"></a><span data-ttu-id="626b3-105">\_ \_ Classe Result01 Storage02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="626b3-105">MDM\_Policy\_Result01\_Storage02 class</span></span>

<span data-ttu-id="626b3-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="626b3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="626b3-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="626b3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="626b3-108">La \_ classe Storage02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di archiviazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="626b3-108">The MDM\_Policy\_Result01\_Storage02 class represents the available storage policies.</span></span>

<span data-ttu-id="626b3-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="626b3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="626b3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="626b3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="626b3-111">Members</span><span class="sxs-lookup"><span data-stu-id="626b3-111">Members</span></span>

<span data-ttu-id="626b3-112">La **classe \_ \_ Result01 \_ Storage02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="626b3-112">The **MDM\_Policy\_Result01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="626b3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="626b3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="626b3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="626b3-114">Properties</span></span>

<span data-ttu-id="626b3-115">La **classe \_ \_ \_ Storage02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="626b3-115">The **MDM\_Policy\_Result01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="626b3-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="626b3-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="626b3-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="626b3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="626b3-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="626b3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="626b3-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="626b3-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="626b3-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="626b3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626b3-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="626b3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="626b3-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="626b3-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626b3-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="626b3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626b3-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="626b3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626b3-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="626b3-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="626b3-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="626b3-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626b3-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="626b3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626b3-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="626b3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626b3-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="626b3-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="626b3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="626b3-130">Requirements</span></span>



| <span data-ttu-id="626b3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="626b3-131">Requirement</span></span> | <span data-ttu-id="626b3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="626b3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="626b3-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="626b3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="626b3-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="626b3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="626b3-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="626b3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="626b3-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="626b3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="626b3-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="626b3-137">Namespace</span></span><br/>                | <span data-ttu-id="626b3-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="626b3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="626b3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="626b3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="626b3-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="626b3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="626b3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="626b3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626b3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="626b3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

