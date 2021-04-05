---
title: Metodi di proprietà IADsAccessControlEntry (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsAccessControlEntry ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsAccessControlEntry ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740527"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="ddd95-105">Metodi di proprietà IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="ddd95-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="ddd95-106">I metodi di proprietà dell'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ddd95-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="ddd95-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ddd95-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ddd95-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ddd95-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ddd95-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ddd95-109">**AccessMask**</span></span>
<span data-ttu-id="ddd95-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-111">Contiene un set di flag che specifica i privilegi di accesso per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddd95-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="ddd95-112">I valori validi per gli oggetti Active Directory sono definiti nell'enumerazione [**Ads \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="ddd95-113">Per ulteriori informazioni e per un elenco di valori possibili per oggetti condivisione file o file, vedere [sicurezza dei file e diritti di accesso](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="ddd95-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="ddd95-114">Per ulteriori informazioni e un elenco di valori possibili per gli oggetti del registro di sistema, vedere [sicurezza e diritti di accesso della chiave del registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="ddd95-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="ddd95-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-116">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ddd95-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="ddd95-117">**AceFlags**</span></span>
<span data-ttu-id="ddd95-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-119">Contiene un set di flag che specifica se altri contenitori o oggetti possono ereditare la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ddd95-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="ddd95-120">I valori validi per Active Directory oggetto sono definiti nell'enumerazione [**Ads \_ ACEFLAG \_ enum**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="ddd95-121">Per ulteriori informazioni e possibili valori per file, condivisione file e oggetti del registro di sistema, vedere il membro **AceFlags** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="ddd95-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-123">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ddd95-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="ddd95-124">**AceType**</span></span>
<span data-ttu-id="ddd95-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-126">Contiene un valore che indica il tipo di voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ddd95-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="ddd95-127">I valori validi per gli oggetti Active Directory sono definiti nell'enumerazione [**Ads \_ ACETYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="ddd95-128">Per ulteriori informazioni e possibili valori per file, condivisione file e oggetti del registro di sistema, vedere il membro **AceType** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="ddd95-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-130">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ddd95-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-131">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ddd95-131">**Flags**</span></span>
<span data-ttu-id="ddd95-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-133">Flag che indica se la voce ACE ha un tipo di oggetto o un tipo di oggetto ereditato.</span><span class="sxs-lookup"><span data-stu-id="ddd95-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="ddd95-134">I flag validi sono definiti nell'enumerazione [**Ads \_ FLAGTYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="ddd95-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-136">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ddd95-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-137">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="ddd95-137">**InheritedObjectType**</span></span>
<span data-ttu-id="ddd95-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-139">Flag che indica il tipo di un oggetto figlio di un oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="ddd95-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="ddd95-140">Il valore è un **GUID** di un oggetto in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="ddd95-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="ddd95-141">Quando viene impostato un **GUID** di questo tipo, la voce ACE si applica solo all'oggetto a cui fa riferimento il **GUID**.</span><span class="sxs-lookup"><span data-stu-id="ddd95-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="ddd95-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-143">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ddd95-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="ddd95-144">**ObjectType**</span></span>
<span data-ttu-id="ddd95-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-146">Flag che indica il tipo di oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="ddd95-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="ddd95-147">Il valore è un **GUID** di una proprietà o di un oggetto in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="ddd95-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="ddd95-148">Il **GUID** fa riferimento a una proprietà quando vengono usati **Ads \_ Rights \_ DS \_ Read \_ prop** e **Ads \_ Rights \_ DS \_ Write \_ prop** Access masks.</span><span class="sxs-lookup"><span data-stu-id="ddd95-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="ddd95-149">Il **GUID** specifica un oggetto quando vengono usati **Ads \_ Rights \_ DS \_ Create \_ child** e **Ads \_ Rights \_ DS \_ Delete \_ child** Access masks.</span><span class="sxs-lookup"><span data-stu-id="ddd95-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="ddd95-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-151">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ddd95-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddd95-152">**Fiduciario**</span><span class="sxs-lookup"><span data-stu-id="ddd95-152">**Trustee**</span></span>
<span data-ttu-id="ddd95-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ddd95-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="ddd95-154">Contiene il nome dell'account a cui viene applicata la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ddd95-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="ddd95-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddd95-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ddd95-156">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ddd95-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ddd95-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="ddd95-157">Examples</span></span>

<span data-ttu-id="ddd95-158">Nell'esempio di codice seguente viene illustrato come aggiungere voci a un ACL discrezionale usando i metodi della proprietà [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="ddd95-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="ddd95-159">Nell'esempio di codice seguente vengono visualizzate le voci di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="ddd95-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ddd95-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddd95-160">Requirements</span></span>



| <span data-ttu-id="ddd95-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddd95-161">Requirement</span></span> | <span data-ttu-id="ddd95-162">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd95-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd95-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd95-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd95-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddd95-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ddd95-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd95-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd95-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddd95-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ddd95-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddd95-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd95-168"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd95-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="ddd95-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ddd95-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddd95-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddd95-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ddd95-171">IID</span><span class="sxs-lookup"><span data-stu-id="ddd95-171">IID</span></span><br/>                      | <span data-ttu-id="ddd95-172">IID \_ IADsAccessControlEntry è definito come B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="ddd95-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddd95-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddd95-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd95-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="ddd95-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="ddd95-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="ddd95-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="ddd95-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ddd95-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

