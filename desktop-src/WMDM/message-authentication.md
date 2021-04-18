---
title: Autenticazione del messaggio
description: Autenticazione del messaggio
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media Gestione dispositivi, autenticazione del messaggio
- Gestione dispositivi, autenticazione del messaggio
- applicazioni desktop, autenticazione del messaggio
- provider di servizi, autenticazione del messaggio
- Guida per programmatori, autenticazione del messaggio
- autenticazione del messaggio
- codice di autenticazione messaggi (MAC)
- MAC (codice di autenticazione messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297839"
---
# <a name="message-authentication"></a>Autenticazione del messaggio

L'autenticazione del messaggio è un processo che consente alle applicazioni e ai provider di servizi di verificare che i dati passati tra di essi non siano stati manomessi. Windows Media Gestione dispositivi consente alle applicazioni e ai provider di servizi di eseguire l'autenticazione dei messaggi usando i codici Mac (Message Authentication Code). Ecco come funziona l'autenticazione MAC:

Il mittente dei dati, in genere il provider di servizi, passa una o più parti di dati tramite una funzione di crittografia unidirezionale che produce una singola firma, il MAC, per tutti i dati. Il mittente invia quindi tutte le parti di dati firmate insieme al MAC al ricevitore, in genere l'applicazione. Il ricevitore passa i dati attraverso la stessa funzione di crittografia per generare un MAC e lo confronta con il MAC che è stato inviato. Se il MAC corrisponde, i dati non sono stati modificati.

Per eseguire l'autenticazione MAC, l'applicazione o il provider di servizi richiede una chiave di crittografia e un certificato corrispondente. Per informazioni su dove ottenere questi dati, vedere [strumenti per lo sviluppo](tools-for-development.md).

Nei passaggi seguenti viene descritto il modo in cui i dati vengono firmati dal mittente e successivamente controllati dal ricevitore. In Windows Media Gestione dispositivi, il provider di servizi usa la classe [CSecureChannelServer](csecurechannelserver-class.md) per generare i computer Mac e l'applicazione usa la classe [CSecureChannelClient](csecurechannelclient-class.md) . Entrambe le classi forniscono funzioni identiche con parametri identici, quindi i passaggi seguenti si applicano a entrambe le classi.

Mittente, in genere il provider di servizi:

1.  Ottiene i dati da firmare.
2.  Creare un nuovo handle MAC chiamando **MACInit**.
3.  Aggiungere una porzione di dati da firmare all'handle chiamando **MACUpdate**. Questa funzione accetta l'handle creato in precedenza, oltre a una parte di dati che devono essere firmati.
4.  Ripetere il passaggio 3 con tutti i dati aggiuntivi che devono essere firmati. Non sono importanti i dati degli ordini aggiunti al MAC.
5.  Copiare il MAC dall'handle in un nuovo buffer di byte chiamando **MACFinal**. Questa funzione accetta l'handle MAC e un buffer allocato e copia il MAC dall'handle nel buffer fornito.

Quando si esegue l'autenticazione MAC, è importante che sia il mittente che il ricevitore stiano inserendo gli stessi dati nel MAC. Per i metodi dell'applicazione che forniscono un MAC, in genere tutti i parametri sono inclusi nel valore MAC (ad eccezione del MAC stesso, ovviamente). Si consideri, ad esempio, il metodo **IWMDMOperation:: TransferObjectData** :

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

In questo metodo, il MAC include *pData* e *pdwSize*. Se non vengono inclusi entrambi i parametri, il MAC creato non corrisponderà al MAC passato a *abMac*. Un provider di servizi deve assicurarsi di inserire tutti i parametri richiesti nel metodo dell'applicazione nel valore MAC.

Nel codice C++ riportato di seguito viene illustrata la creazione di un MAC nell'implementazione di un provider di servizi di [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).


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



Il ricevitore (in genere l'applicazione):

Se il ricevitore non ha implementato l'interfaccia [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , deve eseguire gli stessi passaggi del mittente, quindi confrontare i due valori Mac. Nell'esempio di codice C++ riportato di seguito viene illustrato il modo in cui un'applicazione controlla il MAC ricevuto in una chiamata a [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) per assicurarsi che il numero di serie non sia stato alterato in transito.


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

[**Uso di canali con autenticazione sicura**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




