---
title: Classe MDM_Policy_Config01_Messaging02
description: La \_ classe Messaging02 dei criteri MDM \_ Config01 \_ consente di eseguire il backup e il ripristino di messaggi di testo e la messaggistica ovunque. Questo criterio consente a un'organizzazione di disabilitare queste funzionalità per evitare che le informazioni vengano archiviate nei server all'esterno del controllo.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- Classe MDM_Policy_Config01_Messaging02
- Classe MDM_Policy_Config01_Messaging02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517734"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="dd26c-106">\_ \_ Classe Config01 Messaging02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="dd26c-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="dd26c-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="dd26c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd26c-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="dd26c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd26c-109">La \_ classe Messaging02 dei criteri MDM \_ Config01 \_ consente di eseguire il backup e il ripristino di messaggi di testo e la messaggistica ovunque.</span><span class="sxs-lookup"><span data-stu-id="dd26c-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="dd26c-110">Questo criterio consente a un'organizzazione di disabilitare queste funzionalità per evitare che le informazioni vengano archiviate nei server all'esterno del controllo.</span><span class="sxs-lookup"><span data-stu-id="dd26c-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="dd26c-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dd26c-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd26c-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd26c-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="dd26c-113">Members</span><span class="sxs-lookup"><span data-stu-id="dd26c-113">Members</span></span>

<span data-ttu-id="dd26c-114">La **classe \_ \_ Config01 \_ Messaging02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd26c-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="dd26c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd26c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd26c-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd26c-116">Properties</span></span>

<span data-ttu-id="dd26c-117">La **classe \_ \_ \_ Messaging02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd26c-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd26c-118">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="dd26c-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd26c-119">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd26c-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd26c-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dd26c-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd26c-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd26c-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd26c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd26c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd26c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd26c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd26c-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd26c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd26c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd26c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd26c-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd26c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd26c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd26c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd26c-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd26c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd26c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd26c-129">Requirements</span></span>



| <span data-ttu-id="dd26c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd26c-130">Requirement</span></span> | <span data-ttu-id="dd26c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="dd26c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd26c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd26c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dd26c-133">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd26c-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd26c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd26c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dd26c-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dd26c-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd26c-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd26c-136">Namespace</span></span><br/>                | <span data-ttu-id="dd26c-137">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="dd26c-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd26c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="dd26c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd26c-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd26c-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd26c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dd26c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd26c-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd26c-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

