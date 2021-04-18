---
description: La \_ Proprietà Properties dell'oggetto SWbemObject restituisce un oggetto SWbemPropertySet che è una raccolta di proprietà per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Properties_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309821"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="54674-104">Proprietà SWbemObject. Properties \_</span><span class="sxs-lookup"><span data-stu-id="54674-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="54674-105">La **proprietà \_ Properties** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemPropertySet**](swbempropertyset.md) che è una raccolta di proprietà per la classe o l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="54674-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="54674-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="54674-106">This property is read-only.</span></span>

<span data-ttu-id="54674-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="54674-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="54674-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="54674-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54674-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54674-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="54674-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="54674-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="54674-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="54674-111">Examples</span></span>

<span data-ttu-id="54674-112">L'esempio di codice PowerShell [Genera script di classe WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) nella raccolta TechNet usa la \_ proprietà proprietà per generare uno script per ognuna delle classi WMI che elenca il nome della classe WMI e le proprietà.</span><span class="sxs-lookup"><span data-stu-id="54674-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="54674-113">Il codice seguente, tratto dall' [elenco di tutte le proprietà di un](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) esempio di codice VBScript della classe WMI nella raccolta TechNet, elenca le proprietà di una classe WMI specificata.</span><span class="sxs-lookup"><span data-stu-id="54674-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="54674-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54674-114">Requirements</span></span>



| <span data-ttu-id="54674-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="54674-115">Requirement</span></span> | <span data-ttu-id="54674-116">Valore</span><span class="sxs-lookup"><span data-stu-id="54674-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54674-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54674-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54674-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54674-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54674-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54674-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54674-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54674-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54674-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54674-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="54674-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54674-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54674-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="54674-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="54674-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54674-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54674-125">DLL</span><span class="sxs-lookup"><span data-stu-id="54674-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54674-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54674-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="54674-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="54674-127">CLSID</span></span><br/>                    | <span data-ttu-id="54674-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="54674-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="54674-129">IID</span><span class="sxs-lookup"><span data-stu-id="54674-129">IID</span></span><br/>                      | <span data-ttu-id="54674-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="54674-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




