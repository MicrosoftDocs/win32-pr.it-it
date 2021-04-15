---
title: Metodi di proprietà IADs (IADs. h)
description: I metodi di proprietà dell'interfaccia IADs ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517433"
---
# <a name="iads-property-methods"></a>Metodi di proprietà IADs

I metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

Stringa ADsPath di questo oggetto. La stringa identifica in modo univoco l'oggetto in un ambiente di rete. L'oggetto può essere sempre recuperato utilizzando questo percorso.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Classe**
</dt> <dd> <dl>

Nome della classe dello schema dell'oggetto.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

Identificatore univoco globale dell'oggetto directory. L'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) converte il **GUID** da una stringa di ottetto, archiviata in un server di directory, in un formato stringa.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Nome**
</dt> <dd> <dl>

Nome relativo dell'oggetto come denominato all'interno del servizio directory sottostante. Questo nome distingue questo oggetto dagli elementi di pari livello.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Parent**
</dt> <dd> <dl>

Stringa ADsPath del contenitore padre. Active Directory non consente la creazione di ADsPath di un determinato oggetto concatenando le proprietà **Parent** e **Name** . Sebbene questa operazione potrebbe funzionare in alcuni provider, non è garantito che funzioni per tutte le implementazioni. ADsPath è sicuramente valido e deve essere usato sempre per recuperare il puntatore all'interfaccia di un oggetto.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Schema**
</dt> <dd> <dl>

Stringa ADsPath dell'oggetto della classe dello schema di questo oggetto.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

In Active Directory il **GUID** restituito dal GUID è una stringa di esadecimali. Usare il **GUID** risultante per eseguire l'associazione diretta all'oggetto.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



dove xxx è il valore restituito dalla proprietà GUID. Per ulteriori informazioni, vedere [utilizzo di objectGUID per l'associazione a un oggetto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Si noti che se si utilizza un GUID per eseguire l'associazione a un oggetto, il metodo di proprietà **ADsPath** restituisce valori diversi dai valori normali che verrebbero restituiti se è stato utilizzato un nome distinto (DN) per eseguire l'associazione allo stesso oggetto. Ad esempio, nella tabella seguente sono elencati i valori restituiti quando si utilizzano i due diversi metodi di associazione per associare lo stesso oggetto utente.



|             | Binding con DN                                           | Associa tramite GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Nome**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **Parent**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> Il provider WinNT non supporta l'associazione mediante il **GUID** dell'oggetto e restituisce la proprietà **GUID** in un formato di stringa leggermente diverso.

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come recuperare i dati oggetto utilizzando metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



Nell'esempio di codice seguente viene illustrato come recuperare i dati oggetto utilizzando metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



Nell'esempio di codice seguente viene illustrato come utilizzare i metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADs è definito come FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

