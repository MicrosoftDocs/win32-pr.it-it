---
title: Binding con GetObject e ADsGetObject
description: Le funzioni GetObject e ADsGetObject vengono utilizzate per l'associazione agli oggetti del servizio directory senza autenticazione.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associazione con GetObject e ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963444"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Binding con GetObject e ADsGetObject

Le funzioni **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) vengono utilizzate per l'associazione agli oggetti del servizio directory senza autenticazione. L'applicazione non deve fornire le credenziali per l'accesso ai dati del servizio directory. ADSI usa il contesto di sicurezza del thread chiamante. Tuttavia, se l'autenticazione protetta non riesce, ADSI tenta di eseguire un'associazione semplice con un nome utente e una password null null. Se l'associazione semplice ha esito positivo, il contesto utente per l'associazione è Guest. Un'associazione semplice usa l'autenticazione in testo non crittografato. Poiché il nome utente o la password non vengono trasmessi in rete, questo non è un problema di sicurezza.

La funzione **GetObject** viene utilizzata per l'associazione agli oggetti servizio directory in linguaggi che supportano l'automazione, ad esempio Visual Basic. La funzione **GetObject** richiede una stringa del moniker. In ADSI la stringa di associazione è la stringa del moniker.

In linguaggi che non supportano direttamente l'automazione, ad esempio C o C++, ADSI fornisce la funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per l'associazione agli oggetti del servizio directory. In alternativa, è possibile usare le funzioni [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) e [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per ottenere lo stesso risultato di **GetObject**.

Per un servizio in esecuzione con l'account LocalSystem, il contesto di sicurezza utilizzato da **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) dipende dal computer in cui è in esecuzione il servizio. Se il servizio è in esecuzione come LocalSystem in un controller di dominio, il servizio dispone di accesso completo a livello di sistema per Active Directory. Se il servizio non è in esecuzione in un controller di dominio, il servizio dispone dei diritti di accesso e dei privilegi concessi all'account computer per il computer in cui è in esecuzione il servizio. Questo è significativamente meno potente dell'accesso a livello di sistema.

## <a name="examples"></a>Esempio

Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare la funzione **GetObject** per eseguire l'associazione a un oggetto.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per eseguire l'associazione a un oggetto.


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



 

 