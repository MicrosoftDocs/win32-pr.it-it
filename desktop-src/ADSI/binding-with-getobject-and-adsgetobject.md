---
title: Associazione con GetObject e ADsGetObject
description: Le funzioni GetObject e ADsGetObject vengono usate per eseguire l'associazione agli oggetti del servizio directory senza autenticazione.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI ,using,binding con GetObject e ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fe3f64368f6bbecf390d07f5258c11b6752badbf701e1f248439ca81428749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082755"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Associazione con GetObject e ADsGetObject

Le **funzioni GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) vengono usate per eseguire l'associazione agli oggetti del servizio directory senza autenticazione. L'applicazione non è necessaria per fornire le credenziali quando si accede ai dati del servizio directory. ADSI usa il contesto di sicurezza del thread chiamante. Tuttavia, se l'autenticazione protetta non riesce, ADSI tenta di eseguire un'associazione semplice con un nome utente Null e una password Null. Se l'associazione semplice ha esito positivo, il contesto utente per l'associazione è Guest. Un'associazione semplice usa l'autenticazione in testo non crittografato. Poiché nessun nome utente o password viene trasmesso in rete, non si tratta di un problema di sicurezza.

La **funzione GetObject** viene usata per eseguire l'associazione agli oggetti del servizio directory nei linguaggi che supportano l'automazione, ad esempio Visual Basic. La **funzione GetObject** richiede una stringa di moniker. In ADSI la stringa di associazione è la stringa del moniker.

Nei linguaggi che non supportano direttamente l'automazione, ad esempio C o C++, ADSI fornisce la [**funzione ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) da associare agli oggetti del servizio directory. In alternativa, è possibile usare le funzioni [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) e [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per ottenere lo stesso risultato di **GetObject**.

Per un servizio in esecuzione con l'account LocalSystem, il contesto di sicurezza usato da **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) dipende dal computer in cui è in esecuzione il servizio. Se il servizio viene eseguito come LocalSystem in un controller di dominio, il servizio dispone dell'accesso completo a livello di sistema ad Active Directory. Se il servizio non è in esecuzione in un controller di dominio, il servizio dispone dei diritti di accesso e dei privilegi concessi all'account computer per il computer in cui è in esecuzione il servizio; questo è significativamente meno potente dell'accesso a livello di sistema.

## <a name="examples"></a>Esempio

Nell'Visual Basic di codice seguente viene illustrato come usare la **funzione GetObject** per eseguire l'associazione a un oggetto .


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



Nell'esempio di codice C++ seguente viene illustrato come usare la [**funzione ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per eseguire l'associazione a un oggetto .


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 