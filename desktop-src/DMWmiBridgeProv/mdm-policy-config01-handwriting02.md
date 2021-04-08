---
title: Classe MDM_Policy_Config01_Handwriting02
description: La \_ \_ \_ classe Config01 HANDWRITING02 di criteri MDM viene utilizzata per configurare la modalità predefinita per il pannello grafia.
ms.assetid: 3b835b72-7985-45c9-afc4-b6fdc69b331b
keywords:
- Classe MDM_Policy_Config01_Handwriting02
- Classe MDM_Policy_Config01_Handwriting02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Handwriting02
- MDM_Policy_Config01_Handwriting02.InstanceID
- MDM_Policy_Config01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef2aa5f8b6563126dfcdd9e75870334853db11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874394"
---
# <a name="mdm_policy_config01_handwriting02-class"></a><span data-ttu-id="518c0-105">\_ \_ Classe Config01 Handwriting02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="518c0-105">MDM\_Policy\_Config01\_Handwriting02 class</span></span>

<span data-ttu-id="518c0-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="518c0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="518c0-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="518c0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="518c0-108">La \_ \_ \_ classe Config01 HANDWRITING02 di criteri MDM viene utilizzata per configurare la modalità predefinita per il pannello grafia.</span><span class="sxs-lookup"><span data-stu-id="518c0-108">The MDM\_Policy\_Config01\_Handwriting02 class is used to configure the default mode for the handwriting panel.</span></span>

<span data-ttu-id="518c0-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="518c0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="518c0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="518c0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="518c0-111">Members</span><span class="sxs-lookup"><span data-stu-id="518c0-111">Members</span></span>

<span data-ttu-id="518c0-112">La **classe \_ \_ Config01 \_ Handwriting02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="518c0-112">The **MDM\_Policy\_Config01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="518c0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="518c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="518c0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="518c0-114">Properties</span></span>

<span data-ttu-id="518c0-115">La **classe \_ \_ \_ Handwriting02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="518c0-115">The **MDM\_Policy\_Config01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="518c0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="518c0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518c0-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518c0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518c0-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518c0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="518c0-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="518c0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="518c0-120">PanelDefaultModeDocked</span><span class="sxs-lookup"><span data-stu-id="518c0-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="518c0-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="518c0-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="518c0-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="518c0-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="518c0-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="518c0-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518c0-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518c0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518c0-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518c0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="518c0-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="518c0-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="518c0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="518c0-127">Requirements</span></span>



| <span data-ttu-id="518c0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="518c0-128">Requirement</span></span> | <span data-ttu-id="518c0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="518c0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="518c0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="518c0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="518c0-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="518c0-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="518c0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="518c0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="518c0-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="518c0-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="518c0-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="518c0-134">Namespace</span></span><br/>                | <span data-ttu-id="518c0-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="518c0-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="518c0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="518c0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="518c0-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="518c0-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="518c0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="518c0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="518c0-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="518c0-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

