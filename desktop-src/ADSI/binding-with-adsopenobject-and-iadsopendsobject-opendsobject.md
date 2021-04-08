---
title: Binding con ADsOpenObject e IADsOpenDSObject OpenDSObject
description: La funzione ADsOpenObject e il metodo IADsOpenDSObject OpenDSObject vengono usati per l'associazione agli oggetti servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Binding con ADsOpenObject e IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, uso, associazione con ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047354"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Binding con ADsOpenObject e IADsOpenDSObject:: OpenDSObject

La funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) vengono usati per l'associazione agli oggetti servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.

Quando possibile, è necessario utilizzare le credenziali del thread chiamante. Tuttavia, se è necessario utilizzare le credenziali alternative, è necessario utilizzare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Se vengono usate credenziali alternative, è importante non memorizzare la password nella cache. È possibile eseguire più operazioni di binding specificando il nome utente e la password per la prima operazione di binding e quindi specificando solo il nome utente nelle associazioni successive. Il sistema configura una sessione alla prima chiamata e utilizza la stessa sessione per le successive chiamate di binding, purché vengano soddisfatte le condizioni seguenti:

-   Lo stesso nome utente in ogni operazione di associazione.
-   Implementare un'associazione senza server o eseguire l'associazione allo stesso server in ogni operazione di binding.
-   Mantenere una sessione aperta mantenendo un riferimento a un oggetto da una delle operazioni di associazione. La sessione viene chiusa quando viene rilasciato l'ultimo riferimento all'oggetto.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) utilizzano le [interfacce SSPI (Security Support Provider Interface)](/windows/desktop/SecAuthN/sspi) di Windows NT per garantire la flessibilità nelle opzioni di autenticazione. Il vantaggio principale dell'utilizzo di queste interfacce consiste nel fornire tipi diversi di autenticazione ai client Active Directory e crittografare la sessione. Attualmente, ADSI non consente il passaggio di certificati. Pertanto, è possibile utilizzare SSL per la crittografia e quindi Kerberos, NTLM o autenticazione semplice, a seconda della modalità di impostazione dei flag sul parametro *dwReserved* .

Non è possibile richiedere un provider SSPI specifico in ADSI, sebbene si ottenga sempre il protocollo preferenziale più alto. Nel caso di un'associazione client Windows a un computer che esegue Windows, il protocollo è Kerberos. Non consentire un certificato per l'autenticazione è accettabile nel caso di una pagina Web, in quanto l'autenticazione viene eseguita prima di eseguire la pagina Web.

Sebbene le operazioni aperte consentano di specificare un utente e una password, non è consigliabile farlo. Al contrario, non specificare alcuna credenziale e utilizzare in modo implicito le credenziali del contesto di sicurezza del chiamante. Per eseguire il binding a un oggetto directory usando le credenziali del chiamante con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specificare **null** per nome utente e password.

Infine, per eseguire il binding senza autenticazione, usare il flag **Ads \_ No \_ Authentication** . Nessuna autenticazione indica che ADSI tenta di eseguire l'associazione come utente anonimo all'oggetto di destinazione e non esegue alcuna autenticazione. Questa operazione equivale a richiedere l'associazione anonima in LDAP e indica che tutti gli utenti sono inclusi nel contesto di sicurezza.

Se i flag di autenticazione sono impostati su zero, ADSI esegue un binding semplice, inviato come testo non crittografato.

> [!Caution]  
> Se vengono specificati un nome utente e una password senza specificare i flag di autenticazione, il nome utente e la password vengono trasmessi in rete in testo non crittografato, il che rappresenta un rischio per la sicurezza. Non specificare un nome utente e una password senza specificare i flag di autenticazione.

 

## <a name="examples"></a>Esempio

Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


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



L'interfaccia [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) può essere usata anche in C++, ma Duplica la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare l'interfaccia [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) per eseguire la stessa operazione di associazione come nell'esempio di codice precedente.


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



 

 