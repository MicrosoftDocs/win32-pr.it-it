---
title: Binding con ADsOpenObject e IADsOpenDSObject OpenDSObject
description: La funzione ADsOpenObject e il metodo IADsOpenDSObject OpenDSObject vengono usati per l'associazione agli oggetti del servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Associazione con ADSI ADsOpenObject e IADsOpenDSObject OpenDSObject
- ADSI ADSI , tramite, associazione con ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41ffe1e9ad0b8a78d1a8c563de250851a894012938682c4cfd0d0fd713f99bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082775"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Binding con ADsOpenObject e IADsOpenDSObject::OpenDSObject

La [**funzione ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) vengono usati per l'associazione agli oggetti del servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.

Le credenziali del thread chiamante devono essere usate quando possibile. Tuttavia, se è necessario usare credenziali alternative, è necessario usare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) Se vengono usate credenziali alternative, è importante non memorizzare la password nella cache. È possibile eseguire più operazioni di associazione specificando il nome utente e la password per la prima operazione di associazione e quindi specificando solo il nome utente nelle associazioni successive. Il sistema configura una sessione alla prima chiamata e usa la stessa sessione nelle chiamate di associazione successive, purché siano soddisfatte le condizioni seguenti:

-   Lo stesso nome utente in ogni operazione di associazione.
-   Implementare l'associazione senza server o l'associazione allo stesso server in ogni operazione di associazione.
-   Mantenere una sessione aperta mantenendo un riferimento a un oggetto da una delle operazioni di associazione. La sessione viene chiusa quando viene rilasciato l'ultimo riferimento all'oggetto.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usano le interfacce [SSPI (Security Support Provider Interface)](/windows/desktop/SecAuthN/sspi) di Windows NT per consentire la flessibilità nelle opzioni di autenticazione. Il vantaggio principale dell'uso di queste interfacce è fornire diversi tipi di autenticazione ai client Active Directory e crittografare la sessione. Attualmente, ADSI non consente il pass-in dei certificati. Pertanto, è possibile usare SSL per la crittografia e quindi Kerberos, NTLM o l'autenticazione semplice, a seconda della modalità di impostazione dei flag nel *parametro dwReserved.*

Non è possibile richiedere un provider SSPI specifico in ADSI, anche se si ottiene sempre il protocollo di preferenza più elevato. Nel caso di un'Windows client a un computer che esegue Windows, il protocollo è Kerberos. Non consentire un certificato per l'autenticazione è accettabile nel caso di una pagina Web perché l'autenticazione viene eseguita prima dell'esecuzione della pagina Web.

Anche se le operazioni Open consentono di specificare un utente e una password, è consigliabile non farlo. Non specificare invece alcuna credenziale e usare in modo implicito le credenziali del contesto di sicurezza del chiamante. Per eseguire l'associazione a un oggetto directory usando le credenziali del chiamante con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject::OpenDSObject,**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)specificare **NULL** per nome utente e password.

Infine, per eseguire l'associazione senza autenticazione, usare il flag **ADS \_ NO \_ AUTHENTICATION.** Nessuna autenticazione indica che ADSI tenta di eseguire l'associazione come utente anonimo all'oggetto di destinazione e non esegue alcuna autenticazione. Equivale a richiedere l'associazione anonima in LDAP e indica che tutti gli utenti sono inclusi nel contesto di sicurezza.

Se i flag di autenticazione sono impostati su zero, ADSI esegue un'associazione semplice, inviata come testo non crittografato.

> [!Caution]  
> Se si specificano un nome utente e una password senza specificare i flag di autenticazione, il nome utente e la password vengono trasmessi in rete in testo non crittografato, il che rappresenta un rischio per la sicurezza. Non specificare un nome utente e una password senza specificare i flag di autenticazione.

 

## <a name="examples"></a>Esempio

L'Visual Basic di codice seguente illustra come usare il [**metodo IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



L'esempio di codice C++ seguente illustra come usare la [**funzione ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



[**L'interfaccia IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) può essere usata anche in C++, ma duplica la [**funzione ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

L'esempio di codice C++ seguente illustra come usare l'interfaccia [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) per eseguire la stessa operazione di associazione dell'esempio di codice precedente.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 