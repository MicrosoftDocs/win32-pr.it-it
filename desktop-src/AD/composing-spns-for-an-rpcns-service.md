---
title: Composizione di nomi SPN per un servizio RpcNs
description: L'esempio di codice seguente compone i nomi dell'entità servizio (SPN) per un servizio RPC con una voce nel contenitore RpcServices nella directory. Un servizio RPC usa la funzione RpcNsBindingExport per creare la relativa voce RpcServices.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Composizione di nomi SPN per un'inserzione del servizio RpcNs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472651"
---
# <a name="composing-spns-for-an-rpcns-service"></a>Composizione di nomi SPN per un servizio RpcNs

L'esempio di codice seguente compone i nomi dell'entità servizio (SPN) per un servizio RPC con una voce nel contenitore RpcServices nella directory. Un servizio RPC usa la funzione [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) per creare la relativa voce RpcServices.

Un servizio RPC utilizza questo esempio di codice per compilare il nome SPN o i nomi SPN che identificano un'istanza del servizio. Il servizio usa questa routine per eseguire le attività seguenti:

-   Per registrare o annullare la registrazione degli SPN nella directory, quando il servizio viene installato o rimosso. Per ulteriori informazioni e un esempio di codice, vedere la pagina relativa [alla registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md).
-   Registrarsi con il servizio di autenticazione RPC all'avvio del servizio. Per ulteriori informazioni, vedere [l'autenticazione reciproca nelle applicazioni RPC](mutual-authentication-in-rpc-applications.md).

Questo esempio di codice usa il nome distinto della voce RpcServices del servizio per comporre il nome SPN. Prima di chiamare questo codice, chiamare la funzione [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) per creare la voce RpcServices del servizio.

Questo esempio di codice chiama la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per compilare un nome SPN. Il nome SPN è composto dal nome della classe del servizio e dal nome distinto della voce RpcServices del servizio.


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 