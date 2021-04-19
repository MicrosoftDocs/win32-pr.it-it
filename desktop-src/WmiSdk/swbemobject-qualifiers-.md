---
description: La proprietà Qualifiers \_ dell'oggetto SWbemObject restituisce un oggetto dell'SWbemQualifierSet che è una raccolta di qualificatori per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Qualifiers_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309818"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="40ba6-104">SWbemObject. Qualifiers ( \_ proprietà)</span><span class="sxs-lookup"><span data-stu-id="40ba6-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="40ba6-105">La proprietà **Qualifiers \_** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che è una raccolta di qualificatori per la classe o l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="40ba6-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="40ba6-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="40ba6-106">This property is read-only.</span></span>

<span data-ttu-id="40ba6-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="40ba6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="40ba6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="40ba6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ba6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40ba6-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="40ba6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="40ba6-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="40ba6-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="40ba6-111">Examples</span></span>

<span data-ttu-id="40ba6-112">L' [elenco tutti i qualificatori per un](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) esempio di codice VBScript della classe WMI nella raccolta TechNet usa la \_ Proprietà Qualifier per elencare i qualificatori di classe per una classe WMI specificata.</span><span class="sxs-lookup"><span data-stu-id="40ba6-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="40ba6-113">L'esempio di codice [elenco tutte le classi astratte in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript nella raccolta TechNet elenca tutte le classi astratte WMI definite nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="40ba6-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="40ba6-114">L'esempio [List all Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code usa la \_ Proprietà Qualifier per elencare tutte le classi dinamiche WMI (incluse le classi Association) definite nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="40ba6-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="40ba6-115">L'esempio di codice [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell nella raccolta TechNet elenca tutte le proprietà scrivibili nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="40ba6-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ba6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40ba6-116">Requirements</span></span>



| <span data-ttu-id="40ba6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="40ba6-117">Requirement</span></span> | <span data-ttu-id="40ba6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="40ba6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ba6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ba6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="40ba6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40ba6-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40ba6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ba6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="40ba6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40ba6-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40ba6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40ba6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ba6-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40ba6-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40ba6-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="40ba6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="40ba6-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40ba6-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40ba6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="40ba6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ba6-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ba6-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40ba6-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="40ba6-129">CLSID</span></span><br/>                    | <span data-ttu-id="40ba6-130">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="40ba6-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="40ba6-131">IID</span><span class="sxs-lookup"><span data-stu-id="40ba6-131">IID</span></span><br/>                      | <span data-ttu-id="40ba6-132">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="40ba6-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




