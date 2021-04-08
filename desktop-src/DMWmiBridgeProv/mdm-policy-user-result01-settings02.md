---
title: Classe MDM_Policy_User_Result01_Settings02
description: La \_ \_ classe Result01 Settings02 utente dei criteri MDM \_ \_ ottiene le impostazioni per i calendari aggiuntivi nella barra delle applicazioni.
ms.assetid: 84121b24-590a-4b0b-946f-8a107eaed6c6
keywords:
- Classe MDM_Policy_User_Result01_Settings02
- Classe MDM_Policy_User_Result01_Settings02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Settings02
- MDM_Policy_User_Result01_Settings02.InstanceID
- MDM_Policy_User_Result01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b38956121d6391433fd2727048ce95eb0b5646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047901"
---
# <a name="mdm_policy_user_result01_settings02-class"></a><span data-ttu-id="b1b71-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Settings02</span><span class="sxs-lookup"><span data-stu-id="b1b71-105">MDM\_Policy\_User\_Result01\_Settings02 class</span></span>

<span data-ttu-id="b1b71-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b1b71-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b1b71-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b1b71-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b1b71-108">La \_ \_ classe Result01 Settings02 utente dei criteri MDM \_ \_ ottiene le impostazioni per i calendari aggiuntivi nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b1b71-108">The MDM\_Policy\_User\_Result01\_Settings02 class gets the settings for additional calendars in the taskbar.</span></span>

<span data-ttu-id="b1b71-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b1b71-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b71-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1b71-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="b1b71-111">Members</span><span class="sxs-lookup"><span data-stu-id="b1b71-111">Members</span></span>

<span data-ttu-id="b1b71-112">La **classe \_ \_ \_ Result01 \_ Settings02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1b71-112">The **MDM\_Policy\_User\_Result01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="b1b71-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1b71-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1b71-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1b71-114">Properties</span></span>

<span data-ttu-id="b1b71-115">La **classe \_ \_ \_ Result01 \_ Settings02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1b71-115">The **MDM\_Policy\_User\_Result01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b1b71-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="b1b71-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b71-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1b71-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1b71-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b1b71-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1b71-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1b71-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b71-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1b71-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1b71-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1b71-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1b71-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1b71-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1b71-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b1b71-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b71-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1b71-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1b71-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1b71-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1b71-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1b71-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1b71-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1b71-127">Requirements</span></span>



| <span data-ttu-id="b1b71-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b71-128">Requirement</span></span> | <span data-ttu-id="b1b71-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b1b71-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b71-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b71-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b71-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b1b71-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1b71-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b71-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b71-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b1b71-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b1b71-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1b71-134">Namespace</span></span><br/>                | <span data-ttu-id="b1b71-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b1b71-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b1b71-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b1b71-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1b71-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1b71-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1b71-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b1b71-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1b71-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1b71-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

