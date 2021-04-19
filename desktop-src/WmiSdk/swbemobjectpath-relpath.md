---
description: La proprietà relpath dell'oggetto SWbemObjectPath contiene il percorso relativo del percorso completo.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. RelPath (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316985"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="71ebd-103">Proprietà SWbemObjectPath. RelPath</span><span class="sxs-lookup"><span data-stu-id="71ebd-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="71ebd-104">La proprietà **RelPath** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene il percorso relativo del percorso completo.</span><span class="sxs-lookup"><span data-stu-id="71ebd-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="71ebd-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="71ebd-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="71ebd-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="71ebd-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ebd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71ebd-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="71ebd-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71ebd-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="71ebd-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="71ebd-109">Examples</span></span>

<span data-ttu-id="71ebd-110">Nell'esempio di codice VBScript riportato di seguito viene illustrata la differenza tra i dati ottenuti da [**SWbemObject. Path \_**](swbemobject-path-.md) e **SWbemObjectPath. RelPath**.</span><span class="sxs-lookup"><span data-stu-id="71ebd-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="71ebd-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71ebd-111">Requirements</span></span>



| <span data-ttu-id="71ebd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ebd-112">Requirement</span></span> | <span data-ttu-id="71ebd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="71ebd-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ebd-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71ebd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="71ebd-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71ebd-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71ebd-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71ebd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="71ebd-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71ebd-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71ebd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71ebd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ebd-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ebd-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="71ebd-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="71ebd-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="71ebd-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="71ebd-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="71ebd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="71ebd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71ebd-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ebd-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="71ebd-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="71ebd-124">CLSID</span></span><br/>                    | <span data-ttu-id="71ebd-125">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="71ebd-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="71ebd-126">IID</span><span class="sxs-lookup"><span data-stu-id="71ebd-126">IID</span></span><br/>                      | <span data-ttu-id="71ebd-127">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="71ebd-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




