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
# <a name="iadsaccesscontrolentry-property-methods"></a>Metodi di proprietà IADsAccessControlEntry

I metodi di proprietà dell'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**AccessMask**
</dt> <dd> <dl>

Contiene un set di flag che specifica i privilegi di accesso per l'oggetto. I valori validi per gli oggetti Active Directory sono definiti nell'enumerazione [**Ads \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .

Per ulteriori informazioni e per un elenco di valori possibili per oggetti condivisione file o file, vedere [sicurezza dei file e diritti di accesso](/windows/desktop/FileIO/file-security-and-access-rights).

Per ulteriori informazioni e un elenco di valori possibili per gli oggetti del registro di sistema, vedere [sicurezza e diritti di accesso della chiave del registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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

**AceFlags**
</dt> <dd> <dl>

Contiene un set di flag che specifica se altri contenitori o oggetti possono ereditare la voce ACE. I valori validi per Active Directory oggetto sono definiti nell'enumerazione [**Ads \_ ACEFLAG \_ enum**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .

Per ulteriori informazioni e possibili valori per file, condivisione file e oggetti del registro di sistema, vedere il membro **AceFlags** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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

**AceType**
</dt> <dd> <dl>

Contiene un valore che indica il tipo di voce ACE. I valori validi per gli oggetti Active Directory sono definiti nell'enumerazione [**Ads \_ ACETYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .

Per ulteriori informazioni e possibili valori per file, condivisione file e oggetti del registro di sistema, vedere il membro **AceType** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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

**Flag**
</dt> <dd> <dl>

Flag che indica se la voce ACE ha un tipo di oggetto o un tipo di oggetto ereditato. I flag validi sono definiti nell'enumerazione [**Ads \_ FLAGTYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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

**InheritedObjectType**
</dt> <dd> <dl>

Flag che indica il tipo di un oggetto figlio di un oggetto ADSI. Il valore è un **GUID** di un oggetto in formato stringa. Quando viene impostato un **GUID** di questo tipo, la voce ACE si applica solo all'oggetto a cui fa riferimento il **GUID**.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
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

**ObjectType**
</dt> <dd> <dl>

Flag che indica il tipo di oggetto ADSI. Il valore è un **GUID** di una proprietà o di un oggetto in formato stringa. Il **GUID** fa riferimento a una proprietà quando vengono usati **Ads \_ Rights \_ DS \_ Read \_ prop** e **Ads \_ Rights \_ DS \_ Write \_ prop** Access masks. Il **GUID** specifica un oggetto quando vengono usati **Ads \_ Rights \_ DS \_ Create \_ child** e **Ads \_ Rights \_ DS \_ Delete \_ child** Access masks.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
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

**Fiduciario**
</dt> <dd> <dl>

Contiene il nome dell'account a cui viene applicata la voce ACE.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
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

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come aggiungere voci a un ACL discrezionale usando i metodi della proprietà [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .


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



Nell'esempio di codice seguente vengono visualizzate le voci di controllo di accesso.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsAccessControlEntry è definito come B4F3A14C-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

