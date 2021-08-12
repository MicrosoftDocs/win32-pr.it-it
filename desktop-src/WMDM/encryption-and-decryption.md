---
title: Crittografia e decrittografia
description: Crittografia e decrittografia
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Gestione dispositivi multimediali, crittografia
- Gestione dispositivi, crittografia
- applicazioni desktop, crittografia
- provider di servizi, crittografia
- guida per programmatori, crittografia
- Crittografia
- Windows Gestione dispositivi multimediali, decrittografia
- Gestione dispositivi, decrittografia
- applicazioni desktop, decrittografia
- provider di servizi, decrittografia
- guida per programmatori, decrittografia
- decrittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c154910709007e502c1505fc6fc3274665942c9eabe8e24de5b30fe932d813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584669"
---
# <a name="encryption-and-decryption"></a>Crittografia e decrittografia

Windows Gestione dispositivi multimediali richiede la crittografia dei file inviati tra il provider di servizi e l'applicazione. Questa operazione può essere eseguita in uno dei due modi seguenti:

-   Se il provider di servizi supporta solo [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) e [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), i dati devono essere crittografati e decrittografati dall'applicazione e dal provider di servizi usando rispettivamente i metodi [CSecureChannelClient](csecurechannelclient-class.md) e [CSecureChannelServer.](csecurechannelserver-class.md)
-   Se il provider di servizi supporta [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) e [**IMDSPObject2::WriteOnClearChannel,**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)l'applicazione può evitare costose autenticazioni dei messaggi del canale sicuro. Il canale protetto viene mantenuto in modo che i provider di servizi legacy che non implementano [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) possano continuare a funzionare.

Il requisito di crittografia impedisce alle applicazioni dannose di ottenere i dati passati tra i componenti software e protegge anche l'integrità dei dati inviati al dispositivo o dal dispositivo.

I tre metodi seguenti richiedono la crittografia o la decrittografia.



| Metodo                                                                          | Descrizione                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | (Applicazione) Crittografia o decrittografia, a seconda che l'applicazione invii o riceva dati. |
| [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (provider di servizi) Crittografia.                                                                             |
| [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Provider di servizi) Decrittografia.                                                                             |



 

La crittografia e la decrittografia vengono entrambe eseguite da singole chiamate al metodo. La crittografia viene eseguita [**da CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) per le applicazioni o [**da CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) per i provider di servizi. La decrittografia viene eseguita da [**CSecureChannelClient::D ecryptParam**](/previous-versions/bb231586(v=vs.85)) per le applicazioni o [**da CSecureChannelServer::D ecryptParam**](/previous-versions/bb231598(v=vs.85)) per i provider di servizi. I parametri sono identici tra i metodi client e server.

La procedura seguente illustra come crittografare e decrittografare i dati. Questi passaggi sono importanti solo se l'applicazione comunica con un provider di servizi legacy che non implementa [IWMDMOperation3::TransferObjectDataOnClearChannel.](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)

**Crittografia**

1.  Creare la chiave MAC per i dati crittografati, come descritto in [Autenticazione dei messaggi](message-authentication.md).
2.  Chiamare **EncryptParam** con i dati da crittografare per eseguire la crittografia sul posto.

Nell'esempio di codice seguente viene illustrata l'implementazione di [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)di un provider di servizi. Questo metodo crea la chiave MAC usando i dati per crittografare e le dimensioni dei dati e li invia entrambi all'applicazione.


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



**Decrittografia**

1.  Chiamare **DecryptParam** con i dati da crittografare per eseguire la decrittografia sul posto.
2.  Verificare la chiave MAC per i dati decrittografati, come descritto in [Autenticazione dei messaggi](message-authentication.md).

Nell'esempio di codice seguente viene illustrata l'implementazione di [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)di un provider di servizi. Questo metodo crea la chiave MAC usando i dati per crittografare e le dimensioni dei dati e li invia entrambi all'applicazione.


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di canali autenticati sicuri**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 