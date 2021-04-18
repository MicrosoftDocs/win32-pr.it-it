---
description: Elenchi di revoche dei certificati
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Elenchi di revoche dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303938"
---
# <a name="certificate-revocation-lists"></a>Elenchi di revoche dei certificati

In questo argomento viene descritto come esaminare l'elenco di revoche di certificati (CRL) per i driver revocati quando si utilizza Certified Output Protocol (COPP).

Il CRL contiene i digest dei certificati revocati e può essere fornito e firmato da Microsoft. Il CRL viene distribuito tramite le licenze Digital Rights Management (DRM). Il CRL può revocare qualsiasi certificato nella catena di certificati del driver. Se viene revocato un certificato nella catena, viene revocato anche il certificato e tutti i certificati sottostanti nella catena.

Per ottenere il CRL, l'applicazione deve utilizzare Windows Media Format SDK, versione 9 o successiva, e seguire questa procedura:

1.  Chiamare **WMCreateReader** per creare l'oggetto Reader di Windows Media Format SDK.
2.  Eseguire una query sull'oggetto Reader per l'interfaccia **IWMDRMReader** .
3.  Chiamare **IWMDRMReader:: GetDRMProperty** con il valore g \_ wszWMDRMNet \_ revoca per ottenere l'elenco CRL. È necessario chiamare questo metodo due volte: una volta per ottenere la dimensione del buffer da allocare e una volta per riempire il buffer. La seconda chiamata restituisce una stringa che contiene l'elenco CRL. L'intera stringa è codificata in base 64.
4.  Decodificare la stringa con codifica base 64. Per eseguire questa operazione, è possibile usare la funzione **CryptStringToBinary** . Questa funzione fa parte di CryptoAPI.

> [!Note]  
> Per usare l'interfaccia **IWMDRMReader** , è necessario ottenere una libreria DRM statica da Microsoft e collegare l'applicazione a questo file di libreria. Per ulteriori informazioni, vedere l'argomento "ottenere la libreria DRM necessaria" nella documentazione relativa a Windows Media Format SDK.

 

Se il CRL non è presente nel computer dell'utente, il metodo **GetDRMProperty** restituisce la proprietà non supportata da NS \_ E \_ DRM \_ \_ . Attualmente, l'unico modo per ottenere l'elenco CRL consiste nell'acquisire una licenza DRM.

Nel codice seguente viene illustrata una funzione che restituisce il CRL:


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



Successivamente, l'applicazione deve verificare che il CRL sia valido. A tale scopo, verificare che il certificato CRL, che fa parte del CRL, sia firmato direttamente dal certificato radice Microsoft e che il valore dell'elemento SignCRL sia impostato su 1. Verificare inoltre la firma del CRL.

Una volta verificata l'elenco CRL, l'applicazione può archiviarla. Il numero di versione CRL deve anche essere verificato prima dell'archiviazione in modo che l'applicazione archivi sempre la versione più recente.

Il CRL ha il formato seguente.



| Sezione            | Contenuto                                                             |
|--------------------|----------------------------------------------------------------------|
| Intestazione             | numero di voci version32 CRL a 32 bit                           |
| Voci di revoca | Più voci di revoca a 160 bit                                  |
| Certificato        | certificato di lunghezza lengthVariable certificato a 32 bit                 |
| Firma          | firma a 8 bit type16-bit firma lengthVariable-lunghezza |



 

> [!Note]  
> Tutti i valori interi sono senza segno e sono rappresentati nella notazione Big endian (ordine dei byte di rete).

 

Descrizioni delle sezioni CRL

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione
</dt> <dd>

L'intestazione contiene il numero di versione del CRL e il numero di voci di revoca nel CRL. Un CRL può contenere zero o più voci.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Voci di revoca
</dt> <dd>

Ogni voce di revoca è il digest a 160 bit di un certificato revocato. Confrontare questo digest con l'elemento DigestValue all'interno del certificato.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificato
</dt> <dd>

La sezione certificate contiene un valore a 32 bit che indica la lunghezza (in byte) del certificato XML e la relativa catena di certificati, insieme a una matrice di byte che contiene sia il certificato XML dell'autorità di certificazione (CA) che la catena di certificati con Microsoft come radice. Il certificato deve essere firmato da un'autorità di certificazione che dispone dell'autorità per emettere CRL.

> [!Note]  
> Il certificato non deve essere con terminazione null.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma
</dt> <dd>

La sezione Signature contiene il tipo e la lunghezza della firma e la firma digitale. Il tipo a 8 bit è impostato su 2 per indicare che usa SHA-1 con la crittografia RSA a 1024 bit. La lunghezza è un valore a 16 bit contenente la lunghezza della firma digitale in byte. La firma digitale viene calcolata su tutte le sezioni precedenti del CRL.

La firma viene calcolata usando lo schema di firma digitale RSASSA-PSS definito in PKCS \# 1 (versione 2,1). La funzione hash è SHA-1, definita in Federal Information Processing Standard (FIPS) 180-2 e la funzione di generazione della maschera è maschera MGF1, definita nella sezione B. 2.1 in PKCS \# 1 (versione 2,1). Le operazioni RSASP1 e RSAVP1 usano RSA con un modulo a 1024 bit con un esponente di verifica 65537.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



