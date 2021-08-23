---
title: Creazione di utenti con il provider ADSI LDAP
description: Con il provider LDAP ADSI, è possibile creare solo un account utente globale.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- Provider LDAP ADSI, oggetto utente, creazione utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023069"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Creazione di utenti con il provider ADSI LDAP

Con il provider LDAP ADSI, è possibile creare solo un account utente globale. Gli account locali risiedono nel database SAM e devono essere creati usando il provider WinNT. Per altre informazioni sulla creazione di un oggetto utente con il provider WinNT, vedere [Oggetto utente WinNT.](winnt-user-object.md)

**Per creare un oggetto utente**

1.  Eseguire il binding al contenitore in cui risiederà l'oggetto utente e ottenere [**l'interfaccia IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per il contenitore.
2.  Usare il [**metodo IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) o [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) per creare l'oggetto utente.
3.  Gli attributi minimi necessari per creare un oggetto utente dipenderanno dal servizio directory usato. Per altre informazioni sulla creazione di un utente di Active Directory, vedere [Creazione di un utente.](/windows/desktop/AD/creating-a-user)
4.  Se viene [**usata l'interfaccia IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) il nuovo oggetto non viene effettivamente creato fino a quando non viene chiamato il metodo [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

    Se viene [**usata l'interfaccia IDirectoryObject,**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) il nuovo oggetto viene creato quando viene chiamato il metodo [**CreateDSObject.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) Gli attributi minimi, incluso [**objectClass**](/windows/desktop/ADSchema/a-objectclass), devono essere specificati nella matrice [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) passata al **metodo CreateDSObject.**

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene creato un account utente con gli attributi predefiniti.


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene creato un account utente con gli attributi predefiniti. Per brevità, il controllo degli errori viene omesso.


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 