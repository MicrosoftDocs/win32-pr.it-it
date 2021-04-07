---
title: Metodi di proprietà IADsPropertyList (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsPropertyList leggono le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 3564b61a-5950-4d00-8ea1-86fecd5c6c4e
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPropertyList ADSI
topic_type:
- apiref
api_name:
- IADsPropertyList Property Methods
- IADsPropertyList.PropertyCount
- IADsPropertyList.get_PropertyCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f13494eeb502122216ffa0c73c24d5b707588e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874518"
---
# <a name="iadspropertylist-property-methods"></a><span data-ttu-id="3fbaa-105">Metodi di proprietà IADsPropertyList</span><span class="sxs-lookup"><span data-stu-id="3fbaa-105">IADsPropertyList Property Methods</span></span>

<span data-ttu-id="3fbaa-106">I metodi di proprietà dell'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) leggono le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-106">The property methods of the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface read the properties described in the following table.</span></span> <span data-ttu-id="3fbaa-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3fbaa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3fbaa-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fbaa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3fbaa-109">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="3fbaa-109">**PropertyCount**</span></span>
<span data-ttu-id="3fbaa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3fbaa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3fbaa-111">Numero di elementi nell'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-111">The number of items in the property list.</span></span>

<dt>

<span data-ttu-id="3fbaa-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fbaa-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fbaa-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="3fbaa-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PropertyCount(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="3fbaa-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="3fbaa-114">Examples</span></span>

<span data-ttu-id="3fbaa-115">Nell'esempio di codice seguente viene illustrato come determinare il numero di elementi in un elenco di proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-115">The following code example shows how to determine number of items in a property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "Number of Properties Found: " & count

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
```



<span data-ttu-id="3fbaa-116">Nell'esempio di codice seguente viene illustrato come determinare il numero di elementi in un elenco di proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-116">The following code example shows how to determine number of items in a property list.</span></span>


```C++
int GetPropertyCacheCount(LPWSTR adsPath)
{
    IADsPropertyList *pList;
    IADs *pObj;
    HRESULT hr = S_OK;

    if(!adsPath)
    {
        _tprintf(TEXT("Invalid ADsPath."));
        return -1;
    }

    HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPropertyList,
                          (void**)&pList);
    // Initialize the property cache.
    hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
    pObj->GetInfo();
    pObj->Release();

    // Get the property count.
    hr = pList->get_PropertyCount(&count);
    pList->Release();

    // Return the property count if it succeeded, otherwise
    // return -1.

    if(SUCCEEDED(hr))
    {
        return count;
    }
    else
    {
        return -1;
    }

}
```



## <a name="requirements"></a><span data-ttu-id="3fbaa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fbaa-117">Requirements</span></span>



| <span data-ttu-id="3fbaa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fbaa-118">Requirement</span></span> | <span data-ttu-id="3fbaa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3fbaa-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbaa-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fbaa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3fbaa-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fbaa-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fbaa-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fbaa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3fbaa-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fbaa-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fbaa-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fbaa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fbaa-125"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbaa-125"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3fbaa-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3fbaa-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fbaa-127"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fbaa-127"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fbaa-128">IID</span><span class="sxs-lookup"><span data-stu-id="3fbaa-128">IID</span></span><br/>                      | <span data-ttu-id="3fbaa-129">IID \_ IADsPropertyList è definito come C6F602B6-8F69-11D0-8528-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="3fbaa-129">IID\_IADsPropertyList is defined as C6F602B6-8F69-11D0-8528-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="3fbaa-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fbaa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbaa-131">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="3fbaa-131">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="3fbaa-132">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="3fbaa-132">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





