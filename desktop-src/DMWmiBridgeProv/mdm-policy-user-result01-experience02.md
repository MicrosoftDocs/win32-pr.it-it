---
title: Classe MDM_Policy_User_Result01_Experience02
description: La \_ \_ classe Result01 Experience02 utente dei criteri MDM \_ \_ rappresenta i criteri di esperienza disponibili.
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- Classe MDM_Policy_User_Result01_Experience02
- Classe MDM_Policy_User_Result01_Experience02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873854"
---
# <a name="mdm_policy_user_result01_experience02-class"></a><span data-ttu-id="63e6b-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Experience02</span><span class="sxs-lookup"><span data-stu-id="63e6b-105">MDM\_Policy\_User\_Result01\_Experience02 class</span></span>

<span data-ttu-id="63e6b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="63e6b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63e6b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="63e6b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63e6b-108">La **classe \_ \_ \_ Result01 \_ Experience02 utente dei criteri MDM** rappresenta i criteri di esperienza disponibili.</span><span class="sxs-lookup"><span data-stu-id="63e6b-108">The **MDM\_Policy\_User\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="63e6b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="63e6b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e6b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63e6b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="63e6b-111">Members</span><span class="sxs-lookup"><span data-stu-id="63e6b-111">Members</span></span>

<span data-ttu-id="63e6b-112">La **classe \_ \_ \_ Result01 \_ Experience02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="63e6b-112">The **MDM\_Policy\_User\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="63e6b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63e6b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63e6b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63e6b-114">Properties</span></span>

<span data-ttu-id="63e6b-115">La **classe \_ \_ \_ Result01 \_ Experience02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="63e6b-115">The **MDM\_Policy\_User\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="63e6b-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="63e6b-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="63e6b-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="63e6b-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="63e6b-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="63e6b-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="63e6b-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63e6b-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="63e6b-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63e6b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="63e6b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e6b-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63e6b-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63e6b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63e6b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63e6b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63e6b-141">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="63e6b-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="63e6b-142">Per questa classe la stringa è "Experience".</span><span class="sxs-lookup"><span data-stu-id="63e6b-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="63e6b-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="63e6b-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e6b-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63e6b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63e6b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e6b-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63e6b-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63e6b-147">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="63e6b-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="63e6b-148">Per questa classe la stringa è "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="63e6b-148">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63e6b-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63e6b-149">Requirements</span></span>



| <span data-ttu-id="63e6b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e6b-150">Requirement</span></span> | <span data-ttu-id="63e6b-151">Valore</span><span class="sxs-lookup"><span data-stu-id="63e6b-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e6b-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e6b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="63e6b-153">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="63e6b-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="63e6b-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e6b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="63e6b-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="63e6b-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="63e6b-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="63e6b-156">Namespace</span></span><br/>                | <span data-ttu-id="63e6b-157">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="63e6b-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="63e6b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="63e6b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63e6b-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63e6b-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="63e6b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="63e6b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e6b-161"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="63e6b-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

