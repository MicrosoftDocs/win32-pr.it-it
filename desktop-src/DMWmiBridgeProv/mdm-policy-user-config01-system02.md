---
title: Classe MDM_Policy_User_Config01_System02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ System02 rappresenta i criteri di telemetria disponibili.
ms.assetid: 3f049152-6868-4b10-8711-dadc4cb012b4
keywords:
- Classe MDM_Policy_User_Config01_System02
- Classe MDM_Policy_User_Config01_System02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_System02
- MDM_Policy_User_Config01_System02.InstanceID
- MDM_Policy_User_Config01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eefa8a08320b79c80d4e0cb359fd1194a21ae4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119891"
---
# <a name="mdm_policy_user_config01_system02-class"></a><span data-ttu-id="cb582-105">\_Utente criteri \_ MDM \_ Config01 \_ classe System02</span><span class="sxs-lookup"><span data-stu-id="cb582-105">MDM\_Policy\_User\_Config01\_System02 class</span></span>

<span data-ttu-id="cb582-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="cb582-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cb582-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="cb582-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cb582-108">La \_ classe del criterio MDM \_ utente \_ Config01 \_ System02 rappresenta i criteri di telemetria disponibili.</span><span class="sxs-lookup"><span data-stu-id="cb582-108">The MDM\_Policy\_User\_Config01\_System02 class represents the available telemetry policies.</span></span>

<span data-ttu-id="cb582-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cb582-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb582-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb582-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTelemetry;
};
```

## <a name="members"></a><span data-ttu-id="cb582-111">Members</span><span class="sxs-lookup"><span data-stu-id="cb582-111">Members</span></span>

<span data-ttu-id="cb582-112">La **classe \_ \_ \_ Config01 \_ System02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cb582-112">The **MDM\_Policy\_User\_Config01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="cb582-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb582-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb582-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb582-114">Properties</span></span>

<span data-ttu-id="cb582-115">La **classe \_ \_ \_ Config01 \_ System02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb582-115">The **MDM\_Policy\_User\_Config01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cb582-116">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="cb582-116">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb582-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cb582-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb582-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cb582-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb582-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb582-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb582-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cb582-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb582-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cb582-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb582-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb582-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb582-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cb582-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb582-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cb582-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb582-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cb582-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb582-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb582-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb582-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb582-127">Requirements</span></span>



| <span data-ttu-id="cb582-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb582-128">Requirement</span></span> | <span data-ttu-id="cb582-129">Valore</span><span class="sxs-lookup"><span data-stu-id="cb582-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb582-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb582-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb582-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cb582-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb582-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb582-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb582-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cb582-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cb582-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cb582-134">Namespace</span></span><br/>                | <span data-ttu-id="cb582-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="cb582-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cb582-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cb582-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb582-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb582-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb582-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cb582-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb582-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb582-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

