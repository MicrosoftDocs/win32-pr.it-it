---
description: La proprietà Namespace dell'oggetto SWbemObjectPath contiene il nome dello spazio dei nomi che fa parte del percorso dell'oggetto.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Namespace (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232021"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="8807a-103">Proprietà SWbemObjectPath. Namespace</span><span class="sxs-lookup"><span data-stu-id="8807a-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="8807a-104">La proprietà **namespace** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene il nome dello spazio dei nomi che fa parte del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8807a-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="8807a-105">Ad esempio, il percorso seguente mostra la proprietà Namespace che restituisce la radice \\ CIMV2:</span><span class="sxs-lookup"><span data-stu-id="8807a-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="8807a-106">Per la spiegazione della sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8807a-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8807a-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8807a-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8807a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8807a-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="8807a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8807a-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="8807a-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="8807a-110">Examples</span></span>

<span data-ttu-id="8807a-111">Nell'esempio seguente viene illustrato come ottenere il nome dello spazio dei nomi da istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) che sono dischi rigidi.</span><span class="sxs-lookup"><span data-stu-id="8807a-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="8807a-112">Lo script si connette allo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8807a-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="8807a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8807a-113">Requirements</span></span>



| <span data-ttu-id="8807a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8807a-114">Requirement</span></span> | <span data-ttu-id="8807a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8807a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8807a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8807a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8807a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8807a-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8807a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8807a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8807a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8807a-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8807a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8807a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8807a-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8807a-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8807a-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8807a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8807a-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8807a-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8807a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8807a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8807a-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8807a-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8807a-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="8807a-126">CLSID</span></span><br/>                    | <span data-ttu-id="8807a-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="8807a-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="8807a-128">IID</span><span class="sxs-lookup"><span data-stu-id="8807a-128">IID</span></span><br/>                      | <span data-ttu-id="8807a-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="8807a-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

