---
description: Restituisce un oggetto SWbemPropertySet che contiene la raccolta di proprietà di sistema WMI che si applicano all'oggetto.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: Proprietà SWbemObjectEx.SystemProperties_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233672"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="18d88-103">SWbemObjectEx.Sys\_ Proprietà temProperties</span><span class="sxs-lookup"><span data-stu-id="18d88-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="18d88-104">La **proprietà \_ SystemProperties** dell'oggetto [**SWbemObjectEx**](swbemobjectex.md) restituisce un oggetto [**SWbemPropertySet**](swbempropertyset.md) che contiene la raccolta di [proprietà di sistema WMI](wmi-system-properties.md) che si applicano all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18d88-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="18d88-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="18d88-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="18d88-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="18d88-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d88-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18d88-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="18d88-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="18d88-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="18d88-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="18d88-109">Examples</span></span>

<span data-ttu-id="18d88-110">Nell'esempio di codice seguente vengono recuperati i valori delle proprietà per la \_ classe del processo Win32.</span><span class="sxs-lookup"><span data-stu-id="18d88-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="18d88-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18d88-111">Requirements</span></span>



| <span data-ttu-id="18d88-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d88-112">Requirement</span></span> | <span data-ttu-id="18d88-113">Valore</span><span class="sxs-lookup"><span data-stu-id="18d88-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18d88-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d88-114">Minimum supported client</span></span><br/> | <span data-ttu-id="18d88-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18d88-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18d88-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d88-116">Minimum supported server</span></span><br/> | <span data-ttu-id="18d88-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18d88-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18d88-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18d88-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d88-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d88-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="18d88-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="18d88-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="18d88-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18d88-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18d88-122">DLL</span><span class="sxs-lookup"><span data-stu-id="18d88-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d88-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d88-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="18d88-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="18d88-124">CLSID</span></span><br/>                    | <span data-ttu-id="18d88-125">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="18d88-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="18d88-126">IID</span><span class="sxs-lookup"><span data-stu-id="18d88-126">IID</span></span><br/>                      | <span data-ttu-id="18d88-127">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="18d88-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="18d88-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18d88-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d88-129">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="18d88-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




