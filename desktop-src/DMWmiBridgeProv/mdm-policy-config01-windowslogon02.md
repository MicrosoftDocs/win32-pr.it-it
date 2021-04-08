---
title: Classe MDM_Policy_Config01_WindowsLogon02
description: La \_ \_ classe Config01 WindowsLogon02 di criteri MDM \_ Configura la schermata di blocco e l'interfaccia utente di rete all'accesso.
ms.assetid: eb155cf8-628d-4325-8b39-f193733d4c87
keywords:
- Classe MDM_Policy_Config01_WindowsLogon02
- Classe MDM_Policy_Config01_WindowsLogon02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsLogon02
- MDM_Policy_Config01_WindowsLogon02.InstanceID
- MDM_Policy_Config01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf723729f8b90974b1ecaf5a0d8ee08eba0a3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873869"
---
# <a name="mdm_policy_config01_windowslogon02-class"></a><span data-ttu-id="23406-105">\_ \_ Classe Config01 WindowsLogon02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="23406-105">MDM\_Policy\_Config01\_WindowsLogon02 class</span></span>

<span data-ttu-id="23406-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="23406-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="23406-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="23406-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="23406-108">La \_ \_ classe Config01 WindowsLogon02 di criteri MDM \_ Configura la schermata di blocco e l'interfaccia utente di rete all'accesso.</span><span class="sxs-lookup"><span data-stu-id="23406-108">The MDM\_Policy\_Config01\_WindowsLogon02 class configures the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="23406-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23406-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23406-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23406-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="23406-111">Members</span><span class="sxs-lookup"><span data-stu-id="23406-111">Members</span></span>

<span data-ttu-id="23406-112">La **classe \_ \_ Config01 \_ WindowsLogon02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23406-112">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="23406-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23406-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23406-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23406-114">Properties</span></span>

<span data-ttu-id="23406-115">La **classe \_ \_ \_ WindowsLogon02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23406-115">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="23406-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="23406-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="23406-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23406-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23406-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="23406-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="23406-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="23406-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="23406-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23406-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23406-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="23406-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="23406-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="23406-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="23406-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="23406-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="23406-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="23406-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23406-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23406-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23406-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23406-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23406-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23406-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23406-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="23406-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23406-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="23406-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23406-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23406-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23406-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23406-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23406-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="23406-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23406-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23406-133">Requirements</span></span>



| <span data-ttu-id="23406-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="23406-134">Requirement</span></span> | <span data-ttu-id="23406-135">Valore</span><span class="sxs-lookup"><span data-stu-id="23406-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23406-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23406-136">Minimum supported client</span></span><br/> | <span data-ttu-id="23406-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="23406-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23406-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23406-138">Minimum supported server</span></span><br/> | <span data-ttu-id="23406-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="23406-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="23406-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23406-140">Namespace</span></span><br/>                | <span data-ttu-id="23406-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="23406-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="23406-142">MOF</span><span class="sxs-lookup"><span data-stu-id="23406-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23406-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23406-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="23406-144">DLL</span><span class="sxs-lookup"><span data-stu-id="23406-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23406-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23406-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

