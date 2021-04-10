---
title: Classe MDM_Policy_Result01_Search02
description: La \_ \_ classe Result01 Search02 dei criteri MDM \_ rappresenta i criteri di ricerca disponibili.
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- Classe MDM_Policy_Result01_Search02
- Classe MDM_Policy_Result01_Search02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048062"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="ca120-105">\_ \_ Classe Result01 Search02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="ca120-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="ca120-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ca120-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca120-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ca120-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca120-108">La **classe \_ \_ Result01 \_ Search02 dei criteri MDM** rappresenta i criteri di ricerca disponibili.</span><span class="sxs-lookup"><span data-stu-id="ca120-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="ca120-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ca120-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca120-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca120-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="ca120-111">Members</span><span class="sxs-lookup"><span data-stu-id="ca120-111">Members</span></span>

<span data-ttu-id="ca120-112">La **classe \_ \_ Result01 \_ Search02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca120-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="ca120-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca120-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca120-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca120-114">Properties</span></span>

<span data-ttu-id="ca120-115">La **classe \_ \_ \_ Search02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca120-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ca120-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="ca120-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="ca120-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="ca120-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="ca120-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="ca120-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="ca120-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="ca120-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="ca120-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="ca120-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca120-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca120-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca120-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca120-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca120-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca120-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca120-147">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ca120-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="ca120-148">Per questa classe la stringa è "Search".</span><span class="sxs-lookup"><span data-stu-id="ca120-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="ca120-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ca120-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca120-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca120-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca120-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca120-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca120-153">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ca120-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="ca120-154">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="ca120-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="ca120-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="ca120-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca120-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="ca120-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca120-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca120-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca120-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca120-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca120-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca120-161">Requirements</span></span>



| <span data-ttu-id="ca120-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca120-162">Requirement</span></span> | <span data-ttu-id="ca120-163">Valore</span><span class="sxs-lookup"><span data-stu-id="ca120-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca120-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca120-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ca120-165">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ca120-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca120-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca120-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ca120-167">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ca120-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca120-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca120-168">Namespace</span></span><br/>                | <span data-ttu-id="ca120-169">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ca120-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ca120-170">MOF</span><span class="sxs-lookup"><span data-stu-id="ca120-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca120-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca120-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca120-172">DLL</span><span class="sxs-lookup"><span data-stu-id="ca120-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca120-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca120-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca120-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca120-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca120-175">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="ca120-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

