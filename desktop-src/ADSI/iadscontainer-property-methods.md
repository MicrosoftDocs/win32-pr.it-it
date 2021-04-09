---
title: Metodi di proprietà IADsContainer (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsContainer ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120751"
---
# <a name="iadscontainer-property-methods"></a>Metodi di proprietà IADsContainer

I metodi di proprietà dell'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Count**
</dt> <dd> <dl>

Recupera il numero di elementi nel contenitore. Quando è impostato il **filtro** , **count** restituisce solo il numero di elementi filtrati.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Recupera o imposta il filtro utilizzato per selezionare le classi di oggetti in un'enumerazione specificata. Si tratta di una matrice Variant, ogni elemento di cui è il nome di una classe dello schema. Se **Filter** non è impostato o è impostato su Empty, tutti gli oggetti di tutte le classi vengono recuperati dall'enumeratore.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**Hint**
</dt> <dd> <dl>

Matrice Variant di stringhe **BSTR** . Ogni elemento identifica il nome di una proprietà presente nella definizione dello schema. Il parametro *vHints* consente al client di indicare gli attributi da caricare per ogni oggetto enumerato. Tali dati possono essere utilizzati per ottimizzare l'accesso alla rete. L'implementazione esatta, tuttavia, è specifica del provider e non è attualmente utilizzata dal provider WinNT.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

I processi di enumerazione in [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) e **IADsContainer:: Get \_ count** vengono eseguiti sugli oggetti contenuti nella cache. Quando un contenitore contiene un numero elevato di oggetti, le prestazioni potrebbero essere influenzate. Per migliorare le prestazioni, disattivare la cache, impostare una dimensione di pagina appropriata e usare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Per questo motivo, la proprietà **Ottieni \_ conteggio** non è supportata nel provider Microsoft LDAP.

## <a name="examples"></a>Esempio

Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare i metodi di proprietà di [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



Nell'esempio di codice C++ riportato di seguito viene illustrato come è possibile utilizzare i metodi di proprietà di [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Per brevità, il controllo degli errori viene omesso.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer è definito come 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





