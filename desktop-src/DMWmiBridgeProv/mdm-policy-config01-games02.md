---
title: Classe MDM_Policy_Config01_Games02
description: La \_ \_ classe Config01 Games02 di criteri MDM \_ Configura i servizi di gioco avanzati.
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- Classe MDM_Policy_Config01_Games02
- Classe MDM_Policy_Config01_Games02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048670"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="2221d-105">\_ \_ Classe Config01 Games02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="2221d-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="2221d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2221d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2221d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2221d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2221d-108">La \_ \_ classe Config01 Games02 di criteri MDM \_ Configura i servizi di gioco avanzati.</span><span class="sxs-lookup"><span data-stu-id="2221d-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="2221d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2221d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2221d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2221d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="2221d-111">Members</span><span class="sxs-lookup"><span data-stu-id="2221d-111">Members</span></span>

<span data-ttu-id="2221d-112">La **classe \_ \_ Config01 \_ Games02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2221d-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="2221d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2221d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2221d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2221d-114">Properties</span></span>

<span data-ttu-id="2221d-115">La **classe \_ \_ \_ Games02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2221d-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2221d-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="2221d-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2221d-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2221d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2221d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2221d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2221d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2221d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2221d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2221d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2221d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2221d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2221d-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2221d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2221d-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2221d-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2221d-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2221d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2221d-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2221d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2221d-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2221d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2221d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2221d-127">Requirements</span></span>



| <span data-ttu-id="2221d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2221d-128">Requirement</span></span> | <span data-ttu-id="2221d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2221d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2221d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2221d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2221d-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2221d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2221d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2221d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2221d-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2221d-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2221d-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2221d-134">Namespace</span></span><br/>                | <span data-ttu-id="2221d-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2221d-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2221d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2221d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2221d-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2221d-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2221d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2221d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2221d-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2221d-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

