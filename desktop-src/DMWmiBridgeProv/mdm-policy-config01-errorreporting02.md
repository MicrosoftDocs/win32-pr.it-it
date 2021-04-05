---
title: Classe MDM_Policy_Config01_ErrorReporting02
description: La \_ \_ classe Config01 ErrorReporting02 dei criteri MDM \_ Configura i criteri di segnalazione errori.
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- Classe MDM_Policy_Config01_ErrorReporting02
- Classe MDM_Policy_Config01_ErrorReporting02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048167"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="90e53-105">\_ \_ Classe Config01 ErrorReporting02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="90e53-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="90e53-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="90e53-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90e53-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="90e53-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90e53-108">La \_ \_ classe Config01 ErrorReporting02 dei criteri MDM \_ Configura i criteri di segnalazione errori.</span><span class="sxs-lookup"><span data-stu-id="90e53-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="90e53-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="90e53-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e53-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90e53-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="90e53-111">Members</span><span class="sxs-lookup"><span data-stu-id="90e53-111">Members</span></span>

<span data-ttu-id="90e53-112">La **classe \_ \_ Config01 \_ ErrorReporting02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="90e53-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="90e53-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="90e53-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90e53-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="90e53-114">Properties</span></span>

<span data-ttu-id="90e53-115">La **classe \_ \_ \_ ErrorReporting02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="90e53-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="90e53-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="90e53-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="90e53-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90e53-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="90e53-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="90e53-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90e53-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="90e53-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="90e53-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90e53-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="90e53-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="90e53-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90e53-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90e53-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="90e53-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e53-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90e53-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90e53-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="90e53-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="90e53-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e53-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90e53-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90e53-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="90e53-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e53-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="90e53-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e53-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="90e53-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90e53-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90e53-139">Requirements</span></span>



| <span data-ttu-id="90e53-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="90e53-140">Requirement</span></span> | <span data-ttu-id="90e53-141">Valore</span><span class="sxs-lookup"><span data-stu-id="90e53-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e53-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90e53-142">Minimum supported client</span></span><br/> | <span data-ttu-id="90e53-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="90e53-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90e53-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90e53-144">Minimum supported server</span></span><br/> | <span data-ttu-id="90e53-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="90e53-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="90e53-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90e53-146">Namespace</span></span><br/>                | <span data-ttu-id="90e53-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="90e53-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="90e53-148">MOF</span><span class="sxs-lookup"><span data-stu-id="90e53-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90e53-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90e53-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90e53-150">DLL</span><span class="sxs-lookup"><span data-stu-id="90e53-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90e53-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90e53-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

