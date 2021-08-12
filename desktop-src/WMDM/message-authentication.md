---
title: Autenticazione dei messaggi
description: Autenticazione dei messaggi
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Gestione dispositivi multimediali, autenticazione dei messaggi
- Gestione dispositivi, autenticazione dei messaggi
- applicazioni desktop, autenticazione dei messaggi
- provider di servizi, autenticazione dei messaggi
- guida alla programmazione, autenticazione dei messaggi
- autenticazione dei messaggi
- codice di autenticazione del messaggio (MAC)
- MAC (codice di autenticazione del messaggio)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2921b80d42207bab608c6a8260e6756d3e9f323eab70742acc787ff731ad4b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584485"
---
# <a name="message-authentication"></a>Autenticazione dei messaggi

L'autenticazione dei messaggi è un processo che consente alle applicazioni e ai provider di servizi di verificare che i dati passati tra di essi non siano stati manomissionati. Windows Gestione dispositivi multimediali consente alle applicazioni e ai provider di servizi di eseguire l'autenticazione dei messaggi usando codici di autenticazione dei messaggi (MAC). Ecco come funziona l'autenticazione MAC:

Il mittente dei dati, in genere il provider di servizi, passa uno o più dati tramite una funzione crittografica unidiretiva che produce una singola firma, il MAC, per tutti i dati. Il mittente invia quindi tutti i dati firmati insieme al MAC al ricevitore (in genere l'applicazione). Il ricevitore passa i dati tramite la stessa funzione di crittografia per generare un MAC e li confronta con il MAC inviato. Se il MAC corrisponde, i dati non sono stati modificati.

Per eseguire l'autenticazione MAC, l'applicazione o il provider di servizi richiede una chiave di crittografia e un certificato corrispondente. Per informazioni su dove ottenere questi elementi, vedere [Strumenti per lo sviluppo.](tools-for-development.md)

I passaggi seguenti descrivono come i dati vengono firmati dal mittente e successivamente controllati dal ricevitore. In Windows Gestione dispositivi multimediali, il provider di servizi usa la classe [CSecureChannelServer](csecurechannelserver-class.md) per generare macs e l'applicazione usa la [classe CSecureChannelClient.](csecurechannelclient-class.md) Entrambe le classi forniscono funzioni identiche con parametri identici, quindi i passaggi seguenti si applicano a entrambe le classi.

Mittente (in genere il provider di servizi):

1.  Ottenere i dati da firmare.
2.  Creare un nuovo handle MAC chiamando **MACInit.**
3.  Aggiungere una parte di dati da firmare all'handle chiamando **MACUpdate.** Questa funzione accetta l'handle creato in precedenza e una parte di dati che devono essere firmati.
4.  Ripetere il passaggio 3 con ogni dato aggiuntivo che deve essere firmato. Non è importante l'ordine in cui i dati vengono aggiunti al MAC.
5.  Copiare il mac dall'handle in un nuovo buffer di byte chiamando **MACFinal.** Questa funzione accetta l'handle MAC e un buffer allocato e copia il mac dall'handle nel buffer specificato.

Quando si esegue l'autenticazione MAC, è importante che sia il mittente che il destinatario inserino gli stessi dati nel MAC. Per i metodi dell'applicazione che forniscono un MAC, in genere tutti i parametri sono inclusi nel valore MAC (ad eccezione del MAC stesso, naturalmente). Si consideri ad esempio **il metodo IWMDMOperation::TransferObjectData:**

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

In questo metodo il mac *includerà pData* e *pdwSize.* Se non si includono entrambi i parametri, il codice MAC creato non corrisponderà al MAC passato *ad abMac*. Un provider di servizi deve assicurarsi di inserire tutti i parametri obbligatori nel metodo dell'applicazione nel valore MAC.

Il codice C++ seguente illustra la creazione di un MAC nell'implementazione di [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)di un provider di servizi.


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



Destinatario (in genere l'applicazione):

Se il ricevitore non ha implementato [**l'interfaccia IWMDMOperation3,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) deve eseguire gli stessi passaggi del mittente e quindi confrontare i due valori MAC. L'esempio di codice C++ seguente mostra come un'applicazione controlla il mac ricevuto in una chiamata a [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) per assicurarsi che il numero di serie non sia stato manomesso in transito.


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di canali autenticati sicuri**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




