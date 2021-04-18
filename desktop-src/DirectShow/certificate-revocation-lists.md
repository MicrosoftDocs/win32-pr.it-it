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
# <a name="certificate-revocation-lists"></a><span data-ttu-id="a132f-103">Elenchi di revoche dei certificati</span><span class="sxs-lookup"><span data-stu-id="a132f-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="a132f-104">In questo argomento viene descritto come esaminare l'elenco di revoche di certificati (CRL) per i driver revocati quando si utilizza Certified Output Protocol (COPP).</span><span class="sxs-lookup"><span data-stu-id="a132f-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="a132f-105">Il CRL contiene i digest dei certificati revocati e può essere fornito e firmato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a132f-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="a132f-106">Il CRL viene distribuito tramite le licenze Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="a132f-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="a132f-107">Il CRL può revocare qualsiasi certificato nella catena di certificati del driver.</span><span class="sxs-lookup"><span data-stu-id="a132f-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="a132f-108">Se viene revocato un certificato nella catena, viene revocato anche il certificato e tutti i certificati sottostanti nella catena.</span><span class="sxs-lookup"><span data-stu-id="a132f-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="a132f-109">Per ottenere il CRL, l'applicazione deve utilizzare Windows Media Format SDK, versione 9 o successiva, e seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="a132f-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="a132f-110">Chiamare **WMCreateReader** per creare l'oggetto Reader di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a132f-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="a132f-111">Eseguire una query sull'oggetto Reader per l'interfaccia **IWMDRMReader** .</span><span class="sxs-lookup"><span data-stu-id="a132f-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="a132f-112">Chiamare **IWMDRMReader:: GetDRMProperty** con il valore g \_ wszWMDRMNet \_ revoca per ottenere l'elenco CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="a132f-113">È necessario chiamare questo metodo due volte: una volta per ottenere la dimensione del buffer da allocare e una volta per riempire il buffer.</span><span class="sxs-lookup"><span data-stu-id="a132f-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="a132f-114">La seconda chiamata restituisce una stringa che contiene l'elenco CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="a132f-115">L'intera stringa è codificata in base 64.</span><span class="sxs-lookup"><span data-stu-id="a132f-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="a132f-116">Decodificare la stringa con codifica base 64.</span><span class="sxs-lookup"><span data-stu-id="a132f-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="a132f-117">Per eseguire questa operazione, è possibile usare la funzione **CryptStringToBinary** .</span><span class="sxs-lookup"><span data-stu-id="a132f-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="a132f-118">Questa funzione fa parte di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a132f-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="a132f-119">Per usare l'interfaccia **IWMDRMReader** , è necessario ottenere una libreria DRM statica da Microsoft e collegare l'applicazione a questo file di libreria.</span><span class="sxs-lookup"><span data-stu-id="a132f-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="a132f-120">Per ulteriori informazioni, vedere l'argomento "ottenere la libreria DRM necessaria" nella documentazione relativa a Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a132f-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="a132f-121">Se il CRL non è presente nel computer dell'utente, il metodo **GetDRMProperty** restituisce la proprietà non supportata da NS \_ E \_ DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a132f-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="a132f-122">Attualmente, l'unico modo per ottenere l'elenco CRL consiste nell'acquisire una licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="a132f-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="a132f-123">Nel codice seguente viene illustrata una funzione che restituisce il CRL:</span><span class="sxs-lookup"><span data-stu-id="a132f-123">The following code shows a function that returns the CRL:</span></span>


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



<span data-ttu-id="a132f-124">Successivamente, l'applicazione deve verificare che il CRL sia valido.</span><span class="sxs-lookup"><span data-stu-id="a132f-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="a132f-125">A tale scopo, verificare che il certificato CRL, che fa parte del CRL, sia firmato direttamente dal certificato radice Microsoft e che il valore dell'elemento SignCRL sia impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="a132f-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="a132f-126">Verificare inoltre la firma del CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="a132f-127">Una volta verificata l'elenco CRL, l'applicazione può archiviarla.</span><span class="sxs-lookup"><span data-stu-id="a132f-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="a132f-128">Il numero di versione CRL deve anche essere verificato prima dell'archiviazione in modo che l'applicazione archivi sempre la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="a132f-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="a132f-129">Il CRL ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="a132f-129">The CRL has the following format.</span></span>



| <span data-ttu-id="a132f-130">Sezione</span><span class="sxs-lookup"><span data-stu-id="a132f-130">Section</span></span>            | <span data-ttu-id="a132f-131">Contenuto</span><span class="sxs-lookup"><span data-stu-id="a132f-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="a132f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a132f-132">Header</span></span>             | <span data-ttu-id="a132f-133">numero di voci version32 CRL a 32 bit</span><span class="sxs-lookup"><span data-stu-id="a132f-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="a132f-134">Voci di revoca</span><span class="sxs-lookup"><span data-stu-id="a132f-134">Revocation Entries</span></span> | <span data-ttu-id="a132f-135">Più voci di revoca a 160 bit</span><span class="sxs-lookup"><span data-stu-id="a132f-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="a132f-136">Certificato</span><span class="sxs-lookup"><span data-stu-id="a132f-136">Certificate</span></span>        | <span data-ttu-id="a132f-137">certificato di lunghezza lengthVariable certificato a 32 bit</span><span class="sxs-lookup"><span data-stu-id="a132f-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="a132f-138">Firma</span><span class="sxs-lookup"><span data-stu-id="a132f-138">Signature</span></span>          | <span data-ttu-id="a132f-139">firma a 8 bit type16-bit firma lengthVariable-lunghezza</span><span class="sxs-lookup"><span data-stu-id="a132f-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="a132f-140">Tutti i valori interi sono senza segno e sono rappresentati nella notazione Big endian (ordine dei byte di rete).</span><span class="sxs-lookup"><span data-stu-id="a132f-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="a132f-141">Descrizioni delle sezioni CRL</span><span class="sxs-lookup"><span data-stu-id="a132f-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="a132f-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione</span><span class="sxs-lookup"><span data-stu-id="a132f-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="a132f-143">L'intestazione contiene il numero di versione del CRL e il numero di voci di revoca nel CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="a132f-144">Un CRL può contenere zero o più voci.</span><span class="sxs-lookup"><span data-stu-id="a132f-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="a132f-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Voci di revoca</span><span class="sxs-lookup"><span data-stu-id="a132f-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="a132f-146">Ogni voce di revoca è il digest a 160 bit di un certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="a132f-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="a132f-147">Confrontare questo digest con l'elemento DigestValue all'interno del certificato.</span><span class="sxs-lookup"><span data-stu-id="a132f-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="a132f-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificato</span><span class="sxs-lookup"><span data-stu-id="a132f-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="a132f-149">La sezione certificate contiene un valore a 32 bit che indica la lunghezza (in byte) del certificato XML e la relativa catena di certificati, insieme a una matrice di byte che contiene sia il certificato XML dell'autorità di certificazione (CA) che la catena di certificati con Microsoft come radice.</span><span class="sxs-lookup"><span data-stu-id="a132f-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="a132f-150">Il certificato deve essere firmato da un'autorità di certificazione che dispone dell'autorità per emettere CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="a132f-151">Il certificato non deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a132f-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="a132f-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma</span><span class="sxs-lookup"><span data-stu-id="a132f-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="a132f-153">La sezione Signature contiene il tipo e la lunghezza della firma e la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="a132f-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="a132f-154">Il tipo a 8 bit è impostato su 2 per indicare che usa SHA-1 con la crittografia RSA a 1024 bit.</span><span class="sxs-lookup"><span data-stu-id="a132f-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="a132f-155">La lunghezza è un valore a 16 bit contenente la lunghezza della firma digitale in byte.</span><span class="sxs-lookup"><span data-stu-id="a132f-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="a132f-156">La firma digitale viene calcolata su tutte le sezioni precedenti del CRL.</span><span class="sxs-lookup"><span data-stu-id="a132f-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="a132f-157">La firma viene calcolata usando lo schema di firma digitale RSASSA-PSS definito in PKCS \# 1 (versione 2,1).</span><span class="sxs-lookup"><span data-stu-id="a132f-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="a132f-158">La funzione hash è SHA-1, definita in Federal Information Processing Standard (FIPS) 180-2 e la funzione di generazione della maschera è maschera MGF1, definita nella sezione B. 2.1 in PKCS \# 1 (versione 2,1).</span><span class="sxs-lookup"><span data-stu-id="a132f-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="a132f-159">Le operazioni RSASP1 e RSAVP1 usano RSA con un modulo a 1024 bit con un esponente di verifica 65537.</span><span class="sxs-lookup"><span data-stu-id="a132f-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a132f-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a132f-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a132f-161">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="a132f-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



