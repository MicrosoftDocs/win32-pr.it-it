---
title: Classe MDM_Policy_Config01_TextInput02
description: La \_ \_ classe Config01 TextInput02 dei criteri MDM \_ rappresenta i criteri di input di testo disponibili.
ms.assetid: e5a8d331-40ec-49f2-aedd-5941fe59092f
keywords:
- Classe MDM_Policy_Config01_TextInput02
- Classe MDM_Policy_Config01_TextInput02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02.InstanceID
- MDM_Policy_Config01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f79d750973edf501ca292d042e04bf4dc27ef42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476919"
---
# <a name="mdm_policy_config01_textinput02-class"></a><span data-ttu-id="5ae3d-105">\_ \_ Classe Config01 TextInput02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="5ae3d-105">MDM\_Policy\_Config01\_TextInput02 class</span></span>

<span data-ttu-id="5ae3d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ae3d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5ae3d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5ae3d-108">La **classe \_ \_ Config01 \_ TextInput02 dei criteri MDM** rappresenta i criteri di input di testo disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-108">The **MDM\_Policy\_Config01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="5ae3d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae3d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ae3d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="5ae3d-111">Members</span><span class="sxs-lookup"><span data-stu-id="5ae3d-111">Members</span></span>

<span data-ttu-id="5ae3d-112">La **classe \_ \_ Config01 \_ TextInput02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ae3d-112">The **MDM\_Policy\_Config01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="5ae3d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ae3d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ae3d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ae3d-114">Properties</span></span>

<span data-ttu-id="5ae3d-115">La **classe \_ \_ \_ TextInput02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-115">The **MDM\_Policy\_Config01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5ae3d-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="5ae3d-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-119">Attiva allowimenetworkaccess</span><span class="sxs-lookup"><span data-stu-id="5ae3d-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-122">Attiva allowinputpanel</span><span class="sxs-lookup"><span data-stu-id="5ae3d-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-125">Attiva allowjapaneseimesurrogatepaircharacters</span><span class="sxs-lookup"><span data-stu-id="5ae3d-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-128">Attiva allowjapaneseivscharacters</span><span class="sxs-lookup"><span data-stu-id="5ae3d-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-131">Attiva allowjapanesenonpublishingstandardglyph</span><span class="sxs-lookup"><span data-stu-id="5ae3d-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-134">Attiva allowjapaneseuserdictionary</span><span class="sxs-lookup"><span data-stu-id="5ae3d-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-137">Attiva allowkeyboardtextsuggestions</span><span class="sxs-lookup"><span data-stu-id="5ae3d-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-140">Attiva allowlanguagefeaturesuninstall</span><span class="sxs-lookup"><span data-stu-id="5ae3d-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-143">Attiva excludejapaneseimeexceptjis0208</span><span class="sxs-lookup"><span data-stu-id="5ae3d-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-146">Attiva excludejapaneseimeexceptjis0208andeudc</span><span class="sxs-lookup"><span data-stu-id="5ae3d-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5ae3d-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="5ae3d-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5ae3d-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ae3d-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ae3d-156">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="5ae3d-157">Per questa classe la stringa è "TextInput"</span><span class="sxs-lookup"><span data-stu-id="5ae3d-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="5ae3d-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae3d-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ae3d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae3d-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae3d-161">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ae3d-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ae3d-162">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5ae3d-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="5ae3d-163">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="5ae3d-163">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ae3d-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ae3d-164">Requirements</span></span>



| <span data-ttu-id="5ae3d-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae3d-165">Requirement</span></span> | <span data-ttu-id="5ae3d-166">Valore</span><span class="sxs-lookup"><span data-stu-id="5ae3d-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae3d-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ae3d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae3d-168">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ae3d-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ae3d-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ae3d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae3d-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ae3d-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5ae3d-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ae3d-171">Namespace</span></span><br/>                | <span data-ttu-id="5ae3d-172">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5ae3d-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5ae3d-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5ae3d-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ae3d-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ae3d-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ae3d-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5ae3d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae3d-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae3d-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae3d-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ae3d-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae3d-178">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5ae3d-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

