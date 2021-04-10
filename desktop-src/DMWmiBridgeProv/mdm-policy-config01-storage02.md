---
title: Classe MDM_Policy_Config01_Storage02
description: La \_ \_ classe Config01 Storage02 dei criteri MDM \_ Configura i criteri di archiviazione.
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- Classe MDM_Policy_Config01_Storage02
- Classe MDM_Policy_Config01_Storage02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119914"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="43dd2-105">\_ \_ Classe Config01 Storage02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="43dd2-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="43dd2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="43dd2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="43dd2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="43dd2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="43dd2-108">La \_ \_ classe Config01 Storage02 dei criteri MDM \_ Configura i criteri di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43dd2-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="43dd2-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="43dd2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43dd2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43dd2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="43dd2-111">Members</span><span class="sxs-lookup"><span data-stu-id="43dd2-111">Members</span></span>

<span data-ttu-id="43dd2-112">La **classe \_ \_ Config01 \_ Storage02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43dd2-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="43dd2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43dd2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43dd2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43dd2-114">Properties</span></span>

<span data-ttu-id="43dd2-115">La **classe \_ \_ \_ Storage02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="43dd2-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="43dd2-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="43dd2-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="43dd2-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="43dd2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="43dd2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="43dd2-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="43dd2-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="43dd2-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43dd2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="43dd2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43dd2-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="43dd2-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43dd2-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43dd2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43dd2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="43dd2-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43dd2-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="43dd2-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43dd2-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="43dd2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="43dd2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43dd2-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="43dd2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43dd2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43dd2-130">Requirements</span></span>



| <span data-ttu-id="43dd2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="43dd2-131">Requirement</span></span> | <span data-ttu-id="43dd2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="43dd2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43dd2-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43dd2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="43dd2-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="43dd2-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43dd2-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43dd2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="43dd2-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="43dd2-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="43dd2-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43dd2-137">Namespace</span></span><br/>                | <span data-ttu-id="43dd2-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="43dd2-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="43dd2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="43dd2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43dd2-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43dd2-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="43dd2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="43dd2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43dd2-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43dd2-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

