---
title: Classe MDM_Policy_Config01_RemoteProcedureCall02
description: La \_ \_ classe Config01 RemoteProcedureCall02 dei criteri MDM \_ Configura i criteri di chiamata a procedura remota.
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- Classe MDM_Policy_Config01_RemoteProcedureCall02
- Classe MDM_Policy_Config01_RemoteProcedureCall02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1c1a188afd3694273080c6c369a8dc37abb22a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476606"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a><span data-ttu-id="f2045-105">\_ \_ Classe Config01 RemoteProcedureCall02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="f2045-105">MDM\_Policy\_Config01\_RemoteProcedureCall02 class</span></span>

<span data-ttu-id="f2045-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f2045-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2045-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f2045-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2045-108">La \_ \_ classe Config01 RemoteProcedureCall02 dei criteri MDM \_ Configura i criteri di chiamata a procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f2045-108">The MDM\_Policy\_Config01\_RemoteProcedureCall02 class configures the remote procedure call policies.</span></span>

<span data-ttu-id="f2045-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f2045-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2045-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2045-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="f2045-111">Members</span><span class="sxs-lookup"><span data-stu-id="f2045-111">Members</span></span>

<span data-ttu-id="f2045-112">La **classe \_ \_ Config01 \_ RemoteProcedureCall02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f2045-112">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these types of members:</span></span>

-   [<span data-ttu-id="f2045-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2045-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2045-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2045-114">Properties</span></span>

<span data-ttu-id="f2045-115">La **classe \_ \_ \_ RemoteProcedureCall02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f2045-115">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2045-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2045-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2045-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2045-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2045-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f2045-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2045-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2045-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2045-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2045-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2045-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2045-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2045-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f2045-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2045-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2045-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2045-124">RestrictUnauthenticatedRPCClients</span><span class="sxs-lookup"><span data-stu-id="f2045-124">RestrictUnauthenticatedRPCClients</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2045-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2045-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2045-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2045-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2045-127">RPCEndpointMapperClientAuthentication</span><span class="sxs-lookup"><span data-stu-id="f2045-127">RPCEndpointMapperClientAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2045-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f2045-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2045-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f2045-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2045-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2045-130">Requirements</span></span>



| <span data-ttu-id="f2045-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2045-131">Requirement</span></span> | <span data-ttu-id="f2045-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f2045-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2045-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2045-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2045-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f2045-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2045-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2045-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2045-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2045-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2045-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2045-137">Namespace</span></span><br/>                | <span data-ttu-id="f2045-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f2045-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f2045-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f2045-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2045-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2045-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2045-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f2045-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2045-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2045-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

