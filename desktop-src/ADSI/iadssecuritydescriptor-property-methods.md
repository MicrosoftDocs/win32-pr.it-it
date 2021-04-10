---
title: Metodi di proprietà IADsSecurityDescriptor (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsSecurityDescriptor ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsSecurityDescriptor ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119603"
---
# <a name="iadssecuritydescriptor-property-methods"></a>Metodi di proprietà IADsSecurityDescriptor

I metodi di proprietà dell'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Controllo**
</dt> <dd> <dl>

Flag che qualificano il significato del descrittore di sicurezza. I valori vengono ricavati dalla struttura del [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

**DaclDefaulted**
</dt> <dd> <dl>

Flag del tipo BOOL che indica se l'elenco DACL deriva da un meccanismo predefinito, anziché essere specificato in modo esplicito dal provider originale del descrittore di sicurezza. Se, ad esempio, il creatore di un oggetto non specifica un DACL, l'oggetto riceve l'elenco DACL predefinito dal token di accesso del creatore. Questo flag può influire sul modo in cui il sistema considera l'elenco DACL rispetto all'ereditarietà ACE. Questo flag viene ignorato dal sistema se il \_ flag if \_ non è impostato.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **\_ bool Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**DiscretionaryAcl**
</dt> <dd> <dl>

Elenco di controllo di accesso discrezionale (DACL) che specifica i tipi di accesso concessi all'oggetto per utenti e gruppi specificati. Per ulteriori informazioni sugli elenchi DACL, vedere [DACL null e elenchi DACL vuoti](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

**Gruppo**
</dt> <dd> <dl>

Gruppo a cui appartiene l'ID di sicurezza del proprietario.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

**GroupDefaulted**
</dt> <dd> <dl>

Flag del tipo BOOL che indica se i dati di gruppo sono derivati da un meccanismo predefinito, anziché essere forniti in modo esplicito dal provider originale del descrittore di sicurezza.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **\_ bool Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

**Proprietario**
</dt> <dd> <dl>

Proprietario dell'oggetto.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**OwnerDefaulted**
</dt> <dd> <dl>

Flag del tipo BOOL che indica che i dati del proprietario sono derivati da un meccanismo predefinito, anziché essere forniti in modo esplicito dal provider originale del descrittore di sicurezza.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **\_ bool Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

**Revisione**
</dt> <dd> <dl>

Livello di revisione del descrittore di sicurezza. Questo valore viene ricavato dalla struttura delle [**\_ \_ informazioni di revisione ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Win32. Tutte le voci ACE in un ACL devono avere lo stesso livello di revisione.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

**SaclDefaulted**
</dt> <dd> <dl>

Flag del tipo BOOL che indica che l'elenco SACL è derivato da un meccanismo predefinito, anziché essere fornito in modo esplicito dal provider originale del descrittore di sicurezza. Questo flag può influire sul modo in cui il sistema gestisce l'elenco SACL, rispetto all'ereditarietà ACE. Questo flag viene ignorato dal sistema se \_ \_ non è impostato il flag se è presente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **\_ bool Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**SystemAcl**
</dt> <dd> <dl>

Elenco di controllo di accesso di sistema usato per generare record di controllo per l'oggetto.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato come enumerare un descrittore di sicurezza esistente.


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsSecurityDescriptor è definito come B8C787CA-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

