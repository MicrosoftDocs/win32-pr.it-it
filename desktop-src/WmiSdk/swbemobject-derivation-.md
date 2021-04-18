---
description: La proprietà di derivazione \_ dell'oggetto SWbemObject contiene una matrice di stringhe che descrivono la gerarchia di derivazione della classe per l'istanza a cui si fa riferimento.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Derivation_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314566"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="9c51e-103">Proprietà SWbemObject. Derivation \_</span><span class="sxs-lookup"><span data-stu-id="9c51e-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="9c51e-104">La proprietà di **derivazione \_** dell'oggetto [**SWbemObject**](swbemobject.md) contiene una matrice di stringhe che descrivono la gerarchia di derivazione della classe per l'istanza a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="9c51e-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="9c51e-105">Il primo elemento nella matrice definisce la classe padre e l'ultimo elemento definisce la classe Dynasty.</span><span class="sxs-lookup"><span data-stu-id="9c51e-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="9c51e-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9c51e-106">This property is read-only.</span></span>

<span data-ttu-id="9c51e-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9c51e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9c51e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9c51e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c51e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c51e-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="9c51e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9c51e-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="9c51e-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c51e-111">Examples</span></span>

<span data-ttu-id="9c51e-112">Nell'esempio VBScript seguente viene descritto come recuperare la gerarchia di classi per Win32 \_ disco logico.</span><span class="sxs-lookup"><span data-stu-id="9c51e-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="9c51e-113">nel seguente esempio Perl viene descritto come recuperare la gerarchia di classi per Win32 \_ disco logico.</span><span class="sxs-lookup"><span data-stu-id="9c51e-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="9c51e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c51e-114">Requirements</span></span>



| <span data-ttu-id="9c51e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c51e-115">Requirement</span></span> | <span data-ttu-id="9c51e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9c51e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c51e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c51e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c51e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c51e-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c51e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c51e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c51e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c51e-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c51e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c51e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c51e-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c51e-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c51e-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9c51e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c51e-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c51e-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c51e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9c51e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c51e-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c51e-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c51e-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="9c51e-127">CLSID</span></span><br/>                    | <span data-ttu-id="9c51e-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="9c51e-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9c51e-129">IID</span><span class="sxs-lookup"><span data-stu-id="9c51e-129">IID</span></span><br/>                      | <span data-ttu-id="9c51e-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="9c51e-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




