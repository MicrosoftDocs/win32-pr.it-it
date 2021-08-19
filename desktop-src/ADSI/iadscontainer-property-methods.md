---
title: Metodi della proprietà IADsContainer (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsContainer ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni e una discussione generale sui metodi di proprietà, vedere Metodi delle proprietà di interfaccia.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsContainer ADSI
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
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428086"
---
# <a name="iadscontainer-property-methods"></a>Metodi della proprietà IADsContainer

I metodi di proprietà [**dell'interfaccia IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni e una discussione generale sui metodi di proprietà, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Count**
</dt> <dd> <dl>

Recupera il numero di elementi nel contenitore. Quando **l'opzione** Filter è **impostata, Count** restituisce solo il numero di elementi filtrati.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
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

Recupera o imposta il filtro utilizzato per selezionare le classi di oggetti in una determinata enumerazione. Si tratta di una matrice variant, di cui ogni elemento è il nome di una classe dello schema. Se **Filter** non è impostato su vuoto, tutti gli oggetti di tutte le classi vengono recuperati dall'enumeratore.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **VARIANT**
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

Matrice variant di **stringhe BSTR.** Ogni elemento identifica il nome di una proprietà trovata nella definizione dello schema. Il *parametro vHints* consente al client di indicare quali attributi caricare per ogni oggetto enumerato. Questi dati possono essere usati per ottimizzare l'accesso alla rete. L'implementazione esatta, tuttavia, è specifica del provider e attualmente non viene usata dal provider WinNT.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **VARIANT**
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

I processi di enumerazione in [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) e **IADsContainer::get \_ Count** vengono eseguiti sugli oggetti contenuti nella cache. Quando un contenitore contiene un numero elevato di oggetti, le prestazioni potrebbero essere influenzate. Per migliorare le prestazioni, disattivare la cache, impostare dimensioni di pagina appropriate e usare [**l'interfaccia IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Per questo motivo, la **\_ proprietà get Count** non è supportata nel provider LDAP Microsoft.

## <a name="examples"></a>Esempio

L'Visual Basic di codice seguente illustra come usare i metodi di proprietà [**di IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer)


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



L'esempio di codice C++ seguente illustra come usare i metodi delle proprietà di [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Per brevità, il controllo degli errori viene omesso.


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
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer è definito come 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





