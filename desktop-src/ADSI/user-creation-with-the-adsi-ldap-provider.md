---
title: Creazione di utenti con il provider LDAP ADSI
description: Con il provider LDAP ADSI è possibile creare solo un account utente globale.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI del provider LDAP, oggetto utente, creazione utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104058576"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="a6480-104">Creazione di utenti con il provider LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="a6480-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="a6480-105">Con il provider LDAP ADSI è possibile creare solo un account utente globale.</span><span class="sxs-lookup"><span data-stu-id="a6480-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="a6480-106">Gli account locali si trovano nel database SAM e devono essere creati utilizzando il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="a6480-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="a6480-107">Per ulteriori informazioni sulla creazione di un oggetto utente con il provider WinNT, vedere [oggetto utente WinNT](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="a6480-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="a6480-108">**Per creare un oggetto utente**</span><span class="sxs-lookup"><span data-stu-id="a6480-108">**To create a user object**</span></span>

1.  <span data-ttu-id="a6480-109">Eseguire l'associazione al contenitore in cui si trova l'oggetto utente e ottenere l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6480-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="a6480-110">Usare il metodo [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) per creare l'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="a6480-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="a6480-111">Gli attributi minimi necessari per creare un oggetto utente variano in base al servizio directory usato.</span><span class="sxs-lookup"><span data-stu-id="a6480-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="a6480-112">Per ulteriori informazioni sulla creazione di un utente Active Directory, vedere [creazione di un utente](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="a6480-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="a6480-113">Se viene utilizzata l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , il nuovo oggetto non viene effettivamente creato fino a quando non viene chiamato il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="a6480-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="a6480-114">Se viene utilizzata l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) , il nuovo oggetto viene creato quando viene chiamato il metodo [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="a6480-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="a6480-115">Gli attributi minimi, incluso [**objectClass**](/windows/desktop/ADSchema/a-objectclass), devono essere specificati nella matrice [**Ads \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) passata al metodo **CreateDSObject** .</span><span class="sxs-lookup"><span data-stu-id="a6480-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="a6480-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6480-116">Example 1</span></span>

<span data-ttu-id="a6480-117">Nell'esempio di codice seguente viene creato un account utente con gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a6480-117">The following code example creates a user account with the default attributes.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="a6480-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6480-118">Example 2</span></span>

<span data-ttu-id="a6480-119">Nell'esempio di codice seguente viene creato un account utente con gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a6480-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="a6480-120">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="a6480-120">For brevity, error checking is omitted.</span></span>


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



 

 