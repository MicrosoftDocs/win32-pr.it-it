---
title: Classe MDM_Policy_User_Config01_Settings02
description: La \_ \_ classe Config01 Settings02 utente dei criteri MDM \_ \_ Configura calendari aggiuntivi nella barra delle applicazioni.
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- Classe MDM_Policy_User_Config01_Settings02
- Classe MDM_Policy_User_Config01_Settings02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119894"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="ed42a-105">\_Utente criteri \_ MDM \_ Config01 \_ classe Settings02</span><span class="sxs-lookup"><span data-stu-id="ed42a-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="ed42a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ed42a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed42a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ed42a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed42a-108">La \_ \_ classe Config01 Settings02 utente dei criteri MDM \_ \_ Configura calendari aggiuntivi nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ed42a-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="ed42a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ed42a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed42a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed42a-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="ed42a-111">Members</span><span class="sxs-lookup"><span data-stu-id="ed42a-111">Members</span></span>

<span data-ttu-id="ed42a-112">La **classe \_ \_ \_ Config01 \_ Settings02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ed42a-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="ed42a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed42a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed42a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed42a-114">Properties</span></span>

<span data-ttu-id="ed42a-115">La **classe \_ \_ \_ Config01 \_ Settings02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed42a-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ed42a-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="ed42a-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed42a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed42a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed42a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed42a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed42a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed42a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed42a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed42a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed42a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed42a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed42a-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed42a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed42a-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed42a-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed42a-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed42a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed42a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed42a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed42a-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed42a-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed42a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed42a-127">Requirements</span></span>



| <span data-ttu-id="ed42a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed42a-128">Requirement</span></span> | <span data-ttu-id="ed42a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed42a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed42a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed42a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed42a-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ed42a-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed42a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed42a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed42a-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed42a-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ed42a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed42a-134">Namespace</span></span><br/>                | <span data-ttu-id="ed42a-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ed42a-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ed42a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ed42a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed42a-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed42a-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed42a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed42a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed42a-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed42a-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

