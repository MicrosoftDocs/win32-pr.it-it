---
title: Classe MDM_Policy_Result01_Games02
description: La \_ \_ \_ classe Result01 GAMES02 di criteri MDM ottiene le impostazioni dei servizi di gioco avanzati.
ms.assetid: c8d17de7-b645-4937-af9f-94bfc039b2fc
keywords:
- Classe MDM_Policy_Result01_Games02
- Classe MDM_Policy_Result01_Games02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Games02
- MDM_Policy_Result01_Games02.InstanceID
- MDM_Policy_Result01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a0a9a216b8bb2610e25ffdbd4e233fc8b3f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119999"
---
# <a name="mdm_policy_result01_games02-class"></a><span data-ttu-id="c0270-105">\_ \_ Classe Result01 Games02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="c0270-105">MDM\_Policy\_Result01\_Games02 class</span></span>

<span data-ttu-id="c0270-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c0270-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0270-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c0270-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0270-108">La \_ \_ \_ classe Result01 GAMES02 di criteri MDM ottiene le impostazioni dei servizi di gioco avanzati.</span><span class="sxs-lookup"><span data-stu-id="c0270-108">The MDM\_Policy\_Result01\_Games02 class gets the settings of the advanced gaming services.</span></span>

<span data-ttu-id="c0270-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c0270-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0270-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0270-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="c0270-111">Members</span><span class="sxs-lookup"><span data-stu-id="c0270-111">Members</span></span>

<span data-ttu-id="c0270-112">La **classe \_ \_ Result01 \_ Games02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0270-112">The **MDM\_Policy\_Result01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="c0270-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0270-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0270-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0270-114">Properties</span></span>

<span data-ttu-id="c0270-115">La **classe \_ \_ \_ Games02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0270-115">The **MDM\_Policy\_Result01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c0270-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="c0270-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0270-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c0270-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0270-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c0270-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0270-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0270-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0270-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0270-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0270-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0270-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0270-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0270-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0270-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c0270-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0270-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c0270-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0270-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0270-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0270-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0270-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0270-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0270-127">Requirements</span></span>



| <span data-ttu-id="c0270-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0270-128">Requirement</span></span> | <span data-ttu-id="c0270-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c0270-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0270-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0270-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c0270-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c0270-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0270-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0270-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c0270-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c0270-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0270-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0270-134">Namespace</span></span><br/>                | <span data-ttu-id="c0270-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c0270-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c0270-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c0270-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0270-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0270-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0270-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c0270-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0270-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0270-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

