---
title: Modifica dell'utente non può modificare la password (provider LDAP)
description: La possibilità di modificare la propria password da parte di un utente è un'autorizzazione che può essere concessa o negata.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Modifica dell'utente non può modificare la password (provider LDAP) ADSI
- L'utente non può modificare la password (provider LDAP) ADSI, modificando
- LDAP provider ADSI, esempi di gestione degli utenti, è necessario modificare la password all'accesso successivo, modificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730274"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>Modifica dell'utente non può modificare la password (provider LDAP)

La possibilità di modificare la propria password da parte di un utente è un'autorizzazione che può essere concessa o negata. Per negare questa autorizzazione, impostare due voci ACE nell'elenco di controllo di accesso discrezionale (DACL) del descrittore di sicurezza dell'oggetto utente con il tipo di ACE degli **\_ \_ oggetti di accesso \_ negato \_ ACETYPE ADS** . Una voce ACE nega l'autorizzazione all'utente e un'altra ACE nega l'autorizzazione al gruppo Everyone. Entrambe le voci ACE sono ACE Deny specifiche dell'oggetto che specificano il GUID dell'autorizzazione estesa per la modifica delle password. Per concedere questa autorizzazione, impostare le stesse voci ACE con il tipo di **\_ oggetto ACE ACETYPE \_ accesso \_ consentito \_ ADS** .

Nella procedura riportata di seguito viene descritto come modificare o aggiungere ACE per questa autorizzazione.

**Per modificare o aggiungere le voci ACE per questa autorizzazione**

1.  Eseguire l'associazione all'oggetto utente.
2.  Ottenere l'oggetto [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) dalla proprietà **ntSecurityDescriptor** dell'oggetto utente.
3.  Ottenere un'interfaccia [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) per il descrittore di sicurezza dalla proprietà [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .
4.  Enumerare le voci ACE per l'oggetto e cercare le voci ACE con il GUID della password di modifica ({AB721A53-1E2F-11D0-9819-00AA0040529B}) per la proprietà [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) e "Everyone" o "NT Authority \\ self" per la proprietà **IADsAccessControlEntry. Trustee** .

    > [!Note]  
    > Le stringhe "Everyone" e "NT AUTHORITY \\ self" sono localizzate in base alla lingua del primo controller di dominio nel dominio. Per questo motivo, le stringhe non devono essere utilizzate direttamente. I nomi degli account devono essere ottenuti in fase di esecuzione chiamando la funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) con il SID per le entità di sicurezza note "Everyone" ("s-1-1-0") e "NT Authority \\ self" ("s-1-5-10"). Le funzioni di esempio **GetSidAccountName**, **GetSidAccountName \_ Everyone** e **GetSidAccountName \_ self** C++ visualizzate in [Reading User not change password (provider LDAP)](reading-user-cannot-change-password-ldap-provider.md) dimostrano come eseguire questa operazione.

     

5.  Modificare la proprietà [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) delle voci ACE trovate in **Ads \_ AceType \_ accesso \_ negato \_** se l'utente non è in grado di modificare la password o l' **\_ oggetto ADS AceType \_ accesso \_ consentito \_** se l'utente può modificare la password.
6.  Se la voce ACE "Everyone" non viene trovata, creare un nuovo oggetto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) che contenga i valori della proprietà indicati nella tabella seguente e aggiungere la nuova voce all'ACL con il metodo [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
7.  Se l'ACE "NT AUTHORITY \\ self" non viene trovata, creare un nuovo oggetto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) con gli stessi valori della proprietà indicati nella tabella seguente, ad eccezione della proprietà [**trustee**](iadsaccesscontrolentry-property-methods.md) che contiene il nome dell'account per SID "S-1-5-10" ("NT Authority \\ self"). Aggiungere la voce all'ACL con il metodo [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
8.  Per aggiornare la proprietà **ntSecurityDescriptor** dell'oggetto, chiamare il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) con lo stesso [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) ottenuto nel passaggio 2.
9.  Eseguire il commit delle modifiche locali nel server con il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .
10. Se una delle voci ACE è stata creata, è necessario riordinare l'ACL in modo che le voci ACE siano nell'ordine corretto. A tale scopo, chiamare la funzione [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) con il ADsPath LDAP dell'oggetto e quindi la funzione [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) con lo stesso DACL. Il riordino verrà eseguito automaticamente quando vengono aggiunte le voci ACE.

Nella tabella seguente sono elencati i valori delle proprietà dell'oggetto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .



| Proprietà IADsAccessControlEntry                                        | Valore                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](iadsaccesscontrolentry-property-methods.md)          | **\_ \_ \_ accesso al controllo DS Rights Ads \_**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **Annunci \_ \_Oggetto accesso \_ negato \_ ACETYPE** se l'utente non è in grado di modificare la password o l' **\_ oggetto ADS ACETYPE \_ accesso \_ consentito \_** se l'utente può modificare la password. |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**Bandiere**](iadsaccesscontrolentry-property-methods.md)               | **\_tipo di \_ oggetto flag Ads \_ \_ presente**                                                                                                                                  |
| [**ObjectType**](iadsaccesscontrolentry-property-methods.md)          | "{AB721A53-1E2F-11D0-9819-00AA0040529B}" che è il GUID della modifica della password in formato stringa.                                                                            |
| [**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) | Non usato                                                                                                                                                              |
| [**Fiduciario**](iadsaccesscontrolentry-property-methods.md)             | Nome account per SID "S-1-1-0" (Everyone).                                                                                                                            |



 

## <a name="example-code"></a>Codice di esempio

Nell'esempio di codice seguente viene illustrato come ottenere un'interfaccia per modificare un DACL. L'interfaccia [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) può essere utilizzata impostando l'opzione di **\_ \_ \_ elenco DACL informazioni di sicurezza ADS** .

> [!Note]  
> Per usare il codice descritto in questo esempio, sarà necessario essere un amministratore. Se non si è un amministratore, sarà necessario aggiungere altro codice che userà un'interfaccia che consentirà a un utente di modificare il modo in cui la cache sul lato client viene scaricata al servizio Dominio di Active Directory.

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



Nell'esempio di codice riportato di seguito viene illustrato come modificare l'autorizzazione di modifica della password dell'utente tramite il provider LDAP. Questo esempio di codice usa la funzione di utilità **GetObjectACE** definita in precedenza.

Questo esempio usa le funzioni di esempio **GetSidAccountName \_ Everyone** e **GetSidAccountName \_ self** C++ visualizzate in [Reading User not change password (provider LDAP)](reading-user-cannot-change-password-ldap-provider.md).


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



Nell'esempio di codice riportato di seguito viene illustrato come modificare l'autorizzazione di modifica della password dell'utente tramite il provider LDAP.

> [!Note]  
> L'esempio seguente funziona solo per i domini in cui la lingua primaria è l'inglese perché le stringhe "Everyone" e "NT AUTHORITY \\ self" sono localizzate in base alla lingua del primo controller di dominio nel dominio. Non è possibile Visual Basic ottenere i nomi di account per un'entità di sicurezza nota senza chiamare la funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . Se si utilizza Visual Basic, si consiglia di utilizzare il provider WinNT per modificare l'autorizzazione di modifica della password dell'utente, come illustrato in [modifica dell'utente non è possibile modificare la password (provider WinNT)](modifying-user-cannot-change-password-winnt-provider.md).

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 