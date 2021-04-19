---
description: La proprietà Methods \_ dell'oggetto SWbemObject restituisce un oggetto SWbemMethodSet che è una raccolta di metodi per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Methods_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317541"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="6dbff-104">Proprietà SWbemObject. methods \_</span><span class="sxs-lookup"><span data-stu-id="6dbff-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="6dbff-105">La **proprietà \_ Methods** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemMethodSet**](swbemmethodset.md) che è una raccolta di metodi per la classe o l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="6dbff-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="6dbff-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6dbff-106">This property is read-only.</span></span>

<span data-ttu-id="6dbff-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6dbff-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6dbff-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6dbff-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dbff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dbff-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="6dbff-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6dbff-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6dbff-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="6dbff-111">Examples</span></span>

<span data-ttu-id="6dbff-112">Nell' [esempio di codice](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)riportato di seguito, tratto dalla raccolta TechNet, viene descritto come elencare tutti i metodi di una classe.</span><span class="sxs-lookup"><span data-stu-id="6dbff-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="6dbff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dbff-113">Requirements</span></span>



| <span data-ttu-id="6dbff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dbff-114">Requirement</span></span> | <span data-ttu-id="6dbff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6dbff-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dbff-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dbff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbff-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dbff-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6dbff-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dbff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbff-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dbff-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6dbff-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6dbff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dbff-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dbff-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dbff-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6dbff-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="6dbff-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6dbff-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6dbff-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6dbff-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dbff-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dbff-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6dbff-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="6dbff-126">CLSID</span></span><br/>                    | <span data-ttu-id="6dbff-127">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="6dbff-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6dbff-128">IID</span><span class="sxs-lookup"><span data-stu-id="6dbff-128">IID</span></span><br/>                      | <span data-ttu-id="6dbff-129">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="6dbff-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




