---
title: Classe MDM_Policy_Result01_ErrorReporting02
description: La \_ classe ErrorReporting02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di segnalazione degli errori.
ms.assetid: 8cc8c570-70d7-4dcb-a558-122604a14110
keywords:
- Classe MDM_Policy_Result01_ErrorReporting02
- Classe MDM_Policy_Result01_ErrorReporting02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ErrorReporting02
- MDM_Policy_Result01_ErrorReporting02.InstanceID
- MDM_Policy_Result01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1435e86f4e957a420a76c79f574939cb45df2a4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225211"
---
# <a name="mdm_policy_result01_errorreporting02-class"></a><span data-ttu-id="eecb2-105">\_ \_ Classe Result01 ErrorReporting02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="eecb2-105">MDM\_Policy\_Result01\_ErrorReporting02 class</span></span>

<span data-ttu-id="eecb2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="eecb2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eecb2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="eecb2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eecb2-108">La \_ classe ErrorReporting02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di segnalazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="eecb2-108">The MDM\_Policy\_Result01\_ErrorReporting02 class represents the error reporting policies.</span></span>

<span data-ttu-id="eecb2-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eecb2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecb2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eecb2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ErrorReporting02
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

## <a name="members"></a><span data-ttu-id="eecb2-111">Members</span><span class="sxs-lookup"><span data-stu-id="eecb2-111">Members</span></span>

<span data-ttu-id="eecb2-112">La **classe \_ \_ Result01 \_ ErrorReporting02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eecb2-112">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="eecb2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eecb2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eecb2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eecb2-114">Properties</span></span>

<span data-ttu-id="eecb2-115">La **classe \_ \_ \_ ErrorReporting02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eecb2-115">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eecb2-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="eecb2-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eecb2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eecb2-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="eecb2-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eecb2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eecb2-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="eecb2-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eecb2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eecb2-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="eecb2-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eecb2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eecb2-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eecb2-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eecb2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eecb2-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eecb2-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eecb2-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eecb2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eecb2-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eecb2-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="eecb2-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb2-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eecb2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb2-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eecb2-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eecb2-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eecb2-139">Requirements</span></span>



| <span data-ttu-id="eecb2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="eecb2-140">Requirement</span></span> | <span data-ttu-id="eecb2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="eecb2-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eecb2-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eecb2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eecb2-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="eecb2-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eecb2-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eecb2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eecb2-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eecb2-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eecb2-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eecb2-146">Namespace</span></span><br/>                | <span data-ttu-id="eecb2-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="eecb2-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eecb2-148">MOF</span><span class="sxs-lookup"><span data-stu-id="eecb2-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eecb2-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eecb2-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eecb2-150">DLL</span><span class="sxs-lookup"><span data-stu-id="eecb2-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eecb2-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eecb2-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

