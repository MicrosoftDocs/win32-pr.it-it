---
title: Classe MDM_Policy_Result01_TextInput02
description: La \_ \_ classe Result01 TextInput02 dei criteri MDM \_ rappresenta i criteri di input di testo disponibili.
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- Classe MDM_Policy_Result01_TextInput02
- Classe MDM_Policy_Result01_TextInput02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476264"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="b9442-105">\_ \_ Classe Result01 TextInput02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="b9442-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="b9442-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b9442-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9442-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b9442-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9442-108">La **classe \_ \_ Result01 \_ TextInput02 dei criteri MDM** rappresenta i criteri di input di testo disponibili.</span><span class="sxs-lookup"><span data-stu-id="b9442-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="b9442-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b9442-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9442-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9442-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
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

## <a name="members"></a><span data-ttu-id="b9442-111">Members</span><span class="sxs-lookup"><span data-stu-id="b9442-111">Members</span></span>

<span data-ttu-id="b9442-112">La **classe \_ \_ Result01 \_ TextInput02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b9442-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="b9442-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9442-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9442-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9442-114">Properties</span></span>

<span data-ttu-id="b9442-115">La **classe \_ \_ \_ TextInput02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b9442-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b9442-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="b9442-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-119">Attiva allowimenetworkaccess</span><span class="sxs-lookup"><span data-stu-id="b9442-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-122">Attiva allowinputpanel</span><span class="sxs-lookup"><span data-stu-id="b9442-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-125">Attiva allowjapaneseimesurrogatepaircharacters</span><span class="sxs-lookup"><span data-stu-id="b9442-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-128">Attiva allowjapaneseivscharacters</span><span class="sxs-lookup"><span data-stu-id="b9442-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-131">Attiva allowjapanesenonpublishingstandardglyph</span><span class="sxs-lookup"><span data-stu-id="b9442-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-134">Attiva allowjapaneseuserdictionary</span><span class="sxs-lookup"><span data-stu-id="b9442-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-137">Attiva allowkeyboardtextsuggestions</span><span class="sxs-lookup"><span data-stu-id="b9442-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-140">Attiva allowlanguagefeaturesuninstall</span><span class="sxs-lookup"><span data-stu-id="b9442-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-143">Attiva excludejapaneseimeexceptjis0208</span><span class="sxs-lookup"><span data-stu-id="b9442-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-146">Attiva excludejapaneseimeexceptjis0208andeudc</span><span class="sxs-lookup"><span data-stu-id="b9442-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9442-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="b9442-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9442-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b9442-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9442-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9442-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b9442-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b9442-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9442-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9442-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9442-156">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b9442-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="b9442-157">Per questa classe la stringa è "TextInput"</span><span class="sxs-lookup"><span data-stu-id="b9442-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="b9442-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b9442-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9442-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b9442-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9442-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b9442-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9442-161">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9442-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9442-162">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b9442-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="b9442-163">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="b9442-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9442-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9442-164">Requirements</span></span>



| <span data-ttu-id="b9442-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9442-165">Requirement</span></span> | <span data-ttu-id="b9442-166">Valore</span><span class="sxs-lookup"><span data-stu-id="b9442-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9442-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9442-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b9442-168">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b9442-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9442-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9442-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b9442-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b9442-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b9442-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9442-171">Namespace</span></span><br/>                | <span data-ttu-id="b9442-172">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b9442-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b9442-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b9442-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9442-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9442-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9442-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b9442-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9442-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9442-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9442-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9442-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9442-178">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="b9442-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

