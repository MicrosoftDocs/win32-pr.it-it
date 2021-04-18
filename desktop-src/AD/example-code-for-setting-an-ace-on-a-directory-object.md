---
title: Codice di esempio per l'impostazione di una voce ACE in un oggetto directory
description: Questo argomento include diversi esempi di codice che aggiungono una voce di controllo di accesso (ACE) all'elenco di controllo di accesso discrezionale (DACL) del descrittore di sicurezza di un oggetto directory.
ms.assetid: fb1ad9f5-af2f-4ad1-a58b-6439cca6fd23
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, impostazione di una voce ACE in un oggetto directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16180a2e1216c749c35d68ff607e81320a1482c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299579"
---
# <a name="example-code-for-setting-an-ace-on-a-directory-object"></a>Codice di esempio per l'impostazione di una voce ACE in un oggetto directory

## <a name="define-the-setright-function"></a>Definire la funzione Seright

Nell'esempio di codice seguente viene definita una funzione che aggiunge una voce di controllo di accesso (ACE) all'elenco di controllo di accesso discrezionale (DACL) del descrittore di sicurezza di un oggetto specificato in Active Directory Domain Services. La subroutine consente di:

-   Concedere o negare l'accesso all'intero oggetto.
-   Concedere o negare l'accesso a una proprietà specifica dell'oggetto.
-   Concedere o negare l'accesso a un set di proprietà nell'oggetto.
-   Concedere o negare il diritto di creare un tipo specifico di oggetto figlio.
-   Impostare una voce ACE che può essere ereditata da tutti gli oggetti figlio o da oggetti figlio di una classe di oggetti specificata.

Seguendo questo Visual Basic esempio di codice sono disponibili diversi esempi di codice che illustrano come usare la funzione **Seright** per impostare tipi diversi di ACE.


```VB
Const ACL_REVISION_DS = &H4

Public Function SetRight(objectDN As String, _
               accessrights As Long, _
               accesstype As Long, _
               aceinheritflags As Long, _
               objectGUID As String, _
               inheritedObjectGUID As String, _
               trustee As String) As Boolean
             
Dim dsobject As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim newace As New AccessControlEntry
Dim lflags As Long

On Error GoTo Cleanup
 
' Bind to the specified object.
Set dsobject = GetObject(objectDN)
 
' Read the security descriptor on the object.
Set sd = dsobject.Get("ntSecurityDescriptor")
 
' Get the DACL from the security descriptor.
Set dacl = sd.DiscretionaryAcl
 
' Set the properties of the new ACE.
newace.AccessMask = accessrights
newace.AceType = accesstype
newace.AceFlags = aceinheritflags
newace.trustee = trustee
 
' Set the GUID for the object type or inherited object type.
lflags = 0

If Not objectGUID = vbNullString Then
   newace.ObjectType = objectGUID
   lflags = lflags Or &H1 'ADS_FLAG_OBJECT_TYPE_PRESENT
End If

If Not inheritedObjectGUID = vbNullString Then
   newace.InheritedObjectType = inheritedObjectGUID
   lflags = lflags Or &H2 'ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT
End If

If Not (lflags = 0) Then newace.Flags = lflags
 
' Set the ACL Revision.
dacl.AclRevision = ACL_REVISION_DS

' Add the ACE to the DACL and to the security descriptor.
dacl.AddAce newace
sd.DiscretionaryAcl = dacl
 
' Apply it to the object.
dsobject.Put "ntSecurityDescriptor", sd
dsobject.SetInfo
SetRight = True
Exit Function

Cleanup:
Set dsobject = Nothing
Set sd = Nothing
Set dacl = Nothing
Set newace = Nothing
SetRight = False

End Function
```




```C++
HRESULT SetRight(
          IADs *pObject,
          long lAccessMask,
          long lAccessType,
          long lAccessInheritFlags,
          LPOLESTR szObjectGUID,
          LPOLESTR szInheritedObjectGUID,
          LPOLESTR szTrustee)
{
VARIANT varSD;
HRESULT hr = E_FAIL;
IADsAccessControlList *pACL = NULL;
IADsSecurityDescriptor *pSD = NULL;
IDispatch *pDispDACL = NULL;
IADsAccessControlEntry *pACE = NULL;
IDispatch *pDispACE = NULL;
long lFlags = 0L;
 
// The following code example takes the szTrustee in an expected naming format 
// and assumes it is the name for the correct trustee.
// The application should validate the specified trustee.
if (!szTrustee || !pObject)
    return E_INVALIDARG;
 
VariantInit(&varSD);
 
// Get the nTSecurityDescriptor.
// Type should be VT_DISPATCH - an IDispatch pointer to the security descriptor object.
hr = pObject->Get(_bstr_t("nTSecurityDescriptor"), &varSD);
if ( FAILED(hr) || varSD.vt != VT_DISPATCH ) {
    wprintf(L"get nTSecurityDescriptor failed: 0x%x\n", hr);
    return hr;
}
 
hr = V_DISPATCH( &varSD )->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if ( FAILED(hr) ) {
    wprintf(L"QueryInterface for IADsSecurityDescriptor failed: 0x%x\n", hr);
    goto cleanup;
}
 
// Get the DACL.
hr = pSD->get_DiscretionaryAcl(&pDispDACL);
if (SUCCEEDED(hr)) 
    hr = pDispDACL->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if ( FAILED(hr) ) {
    wprintf(L"Could not get DACL: 0x%x\n", hr);
    goto cleanup;
}
 
// Create the COM object for the new ACE.
hr  = CoCreateInstance( 
               CLSID_AccessControlEntry,
               NULL,
               CLSCTX_INPROC_SERVER,
               IID_IADsAccessControlEntry,
               (void **)&pACE
               );
if ( FAILED(hr) ) {
    wprintf(L"Could not create ACE object: 0x%x\n", hr);
    goto cleanup;
}
 
// Set the properties for the new ACE.
 
// Set the mask that specifies the access right.
hr = pACE->put_AccessMask( lAccessMask );
 
// Set the trustee.
hr = pACE->put_Trustee( szTrustee );
 
// Set AceType.
hr = pACE->put_AceType( lAccessType );
 
// Set AceFlags to specify whether other objects can inherit the ACE from the specified object.
hr = pACE->put_AceFlags( lAccessInheritFlags );
 
// If an szObjectGUID is specified, add ADS_FLAG_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the ObjectType.
if (szObjectGUID)
{
    lFlags |= ADS_FLAG_OBJECT_TYPE_PRESENT;
    hr = pACE->put_ObjectType( szObjectGUID );
}
 
// If an szInheritedObjectGUID is specified, add ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the InheritedObjectType.
if (szInheritedObjectGUID)
{
    lFlags |= ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT;
    hr = pACE->put_InheritedObjectType( szInheritedObjectGUID );
}
 
// Set flags if ObjectType or InheritedObjectType were set.
if (lFlags)
    hr = pACE->put_Flags(lFlags);
 
// Add the ACE to the ACL to the SD to the cache to the object.
// Call the QueryInterface method for the IDispatch pointer to pass to the AddAce method.
hr = pACE->QueryInterface(IID_IDispatch, (void**)&pDispACE);
if (SUCCEEDED(hr))
{
    // Set the ACL revision.
    hr = pACL->put_AclRevision(ACL_REVISION_DS);

    // Add the ACE.
    hr = pACL->AddAce(pDispACE);
    if (SUCCEEDED(hr))
    {
        // Write the DACL.
        hr = pSD->put_DiscretionaryAcl(pDispDACL);
        if (SUCCEEDED(hr))
        {
            // Write the ntSecurityDescriptor property to the property cache.
            hr = pObject->Put(CComBSTR("nTSecurityDescriptor"), varSD);
            if (SUCCEEDED(hr))
            {
                // Call SetInfo to update the property on the object in the directory.
                hr = pObject->SetInfo();
            }
        }
    }
}
 
cleanup:
if (pDispACE)
    pDispACE->Release();
if (pACE)
    pACE->Release();
if (pACL)
    pACL->Release();
if (pDispDACL)
    pDispDACL->Release();
if (pSD)
    pSD->Release();
 
VariantClear(&varSD);
return hr;
}
```



## <a name="grant-or-deny-access-to-the-entire-object"></a>Concedere o negare l'accesso all'intero oggetto

Nell'esempio di codice Visual Basic seguente viene compilata una stringa di associazione per il contenitore Users, quindi viene chiamata la funzione **Seright** per impostare una voce ACE nel contenitore Users. In questo esempio viene impostata una voce ACE che concede al trustee il diritto di leggere o scrivere qualsiasi proprietà nell'oggetto.


```VB
Dim rootDSE As IADs
Dim objectDN As String
Dim bResult As Boolean
Const ADS_RIGHT_READ_PROP = &H10
Const ADS_RIGHT_WRITE_PROP = &H20
 
' Bind to the Users container in the local domain.
Set rootDSE = GetObject("LDAP://rootDSE")
objectDN = "LDAP://cn=users," & rootDSE.Get("defaultNamingContext")
 
' Grant trustee the right to read/write any property.
bResult = SetRight objectDN, _
  ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
   ADS_ACETYPE_ACCESS_ALLOWED, _
    0, _
    vbNullString, _
    vbNullString, _
    "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write any property.")
Else
    MsgBox ("An error occurred.")
End If
```



Nell'esempio di codice C++ riportato di seguito viene impostata una voce ACE che concede al trustee l'autorizzazione per la lettura o la scrittura di qualsiasi proprietà nell'oggetto. Nell'esempio di codice si presuppone che *pObject* e *szTrustee* siano impostati su valori validi. Per ulteriori informazioni, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).


```C++
HRESULT hr;
IADs *pObject;
LPWSTR szTrustee;
 
hr = SetRight(
          pObject,  // IADs pointer to the object
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED,
          0,        // Not inheritable
          NULL,     // No object type GUID
          NULL,     // No inherited object type GUID
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-specific-property-on-the-object"></a>Concedere o negare l'accesso a una proprietà specifica nell'oggetto

In questo esempio di codice viene chiamata la funzione **Seright** per concedere al trustee il diritto di leggere o scrivere una proprietà specifica dell'oggetto. Tenere presente che è necessario specificare il **schemaIDGUID** della proprietà ed è necessario specificare **Ads \_ ACETYPE \_ accesso \_ consentito \_** per indicare che si tratta di una voce ACE specifica dell'oggetto. In questo esempio di codice viene inoltre specificato il flag **\_ \_ \_ ACE ACEFLAG ereditate ADS** che indica che la voce ACE può essere ereditata dagli oggetti figlio.


```VB
' Grant trustee the right to read the Telephone-Number property
' of all child objects in the Users container. 
' {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
' the Telephone-Number property.

bResult = SetRight objectDN, _
     ADS_RIGHT_WRITE_PROP Or ADS_RIGHT_READ_PROP, _
     ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
      ADS_ACEFLAG_INHERIT_ACE, _
       "{bf967a49-0de6-11d0-a285-00aa003049e2}", _
       vbNullString, _
       "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read the telephone number property.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read the Telephone-Number property
// of all child objects in the Users container. 
// {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
// the Telephone-Number property.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE,
          L"{bf967a49-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-set-of-properties-on-the-object"></a>Concedere o negare l'accesso a un set di proprietà nell'oggetto

In questo esempio di codice viene chiamata la funzione **Seright** per concedere al trustee il diritto di leggere o scrivere un set specifico di proprietà nell'oggetto. Specificare **Ads \_ ACETYPE \_ accesso \_ consentito all' \_ oggetto** per indicare che si tratta di una voce ACE specifica dell'oggetto.

Un set di proprietà viene definito da un oggetto **controlAccessRight** nel contenitore dei diritti estesi della partizione di configurazione. Per identificare il set di proprietà nella voce ACE, specificare la proprietà **rightsGuid** di un oggetto **controlAccessRight** . Tenere presente che questo GUID del set di proprietà viene impostato anche nella proprietà **attributeSecurityGUID** di ogni oggetto **attributeSchema** incluso nel set di proprietà. Per altre informazioni, vedere [controllare i diritti di accesso](control-access-rights.md).

Questo esempio di codice consente inoltre di specificare i flag di ereditarietà che impostano la voce ACE come ereditabile dagli oggetti figlio, ma inefficace sull'oggetto immediato. Nell'esempio viene inoltre specificato il GUID della classe User, che indica che la voce ACE può essere ereditata solo dagli oggetti di tale classe.


```VB
' Grant trustee permission to read or write a set of properties.
' {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
' a property set.
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class, so this ACE is inherited only by objects of that class.

bResult = SetRight objectDN, _
        ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
          ADS_ACEFLAG_INHERIT_ACE Or ADS_ACEFLAG_INHERIT_ONLY_ACE, _
          "{77B5B886-944A-11d1-AEBD-0000F80367C1}", _
          "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
          "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write a set of properties.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read or write a set of properties.
// {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
// a property set (rightsGUID of a controlAccessRight object).
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class, so this ACE is inherited only by objects of that class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE,
          L"{77B5B886-944A-11d1-AEBD-0000F80367C1}",
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          szTrustee
          );
```



## <a name="grant-or-deny-permission-to-create-a-specific-type-of-child-object"></a>Concedere o negare l'autorizzazione per la creazione di un tipo specifico di oggetto figlio

Nell'esempio di codice seguente viene chiamata la funzione **Seright** per concedere a un trustee specificato il diritto di creare ed eliminare oggetti utente nel sottoalbero sotto l'oggetto specificato. Tenere presente che l'esempio specifica il GUID della classe utente, il che significa che la voce ACE consente solo al trustee di creare oggetti utente, non a oggetti di altre classi. Specificare **Ads \_ ACETYPE \_ accesso \_ consentito all' \_ oggetto** per indicare che si tratta di una voce ACE specifica dell'oggetto.


```VB
' Grant trustee the right to create or delete User objects 
' in the specified object. 
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class.

bResult = SetRight objectDN, _
          ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD, _
           ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
           0, _
           "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
           vbNullString, _
           "jeffsmith@fabrikam.com" 'trustee

If bResult = True Then
    MsgBox ("The trustee can create or delete User objects.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to create or delete User objects 
// in the specified object. 
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_DS_CREATE_CHILD | ADS_RIGHT_DS_DELETE_CHILD,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          0,        // Not inheritable.
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



Per ulteriori informazioni e per **schemaIDGUID** di un attributo o di una classe predefiniti, vedere la pagina relativa al riferimento all'attributo o alla classe nel riferimento allo [schema Active Directory](/windows/desktop/ADSchema/active-directory-schema) . Per altre informazioni e un esempio di codice che può essere usato per ottenere un **schemaIDGUID** a livello di codice, vedere [lettura di oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).

 

 