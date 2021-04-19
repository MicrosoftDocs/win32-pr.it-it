---
description: Viene illustrato come recuperare un elenco di revoche di certificati.
ms.assetid: b8fbffae-d968-453d-81f0-af9d60be5fa9
title: Recupero di un elenco di revoche di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9c7933ac5762c9367d7bdff150da011f789835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317697"
---
# <a name="retrieving-a-certificate-revocation-list"></a><span data-ttu-id="c5902-103">Recupero di un elenco di revoche di certificati</span><span class="sxs-lookup"><span data-stu-id="c5902-103">Retrieving a Certificate Revocation List</span></span>

<span data-ttu-id="c5902-104">Un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) è responsabile della pubblicazione dell' [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL).</span><span class="sxs-lookup"><span data-stu-id="c5902-104">A [*certification authority*](../secgloss/c-gly.md) (CA) is responsible for publishing its [*certificate revocation list*](../secgloss/c-gly.md) (CRL).</span></span> <span data-ttu-id="c5902-105">Il CRL corrente può essere recuperato tramite il metodo [**ICertAdmin2:: GetCRL**](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl) .</span><span class="sxs-lookup"><span data-stu-id="c5902-105">The current CRL can be retrieved by using the [**ICertAdmin2::GetCRL**](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl) method.</span></span> <span data-ttu-id="c5902-106">Nei casi in cui il certificato di una CA è stato rinnovato, potrebbe essere necessario recuperare i CRL per i certificati della CA precedenti.</span><span class="sxs-lookup"><span data-stu-id="c5902-106">In cases where a CA's certificate has been renewed, you might need to retrieve CRLs for the previous CA certificates.</span></span> <span data-ttu-id="c5902-107">Per informazioni sul rinnovo della CA, vedere [rinnovo dell'autorità di certificazione](certification-authority-renewal.md).</span><span class="sxs-lookup"><span data-stu-id="c5902-107">For information about CA renewal, see [Certification Authority Renewal](certification-authority-renewal.md).</span></span> <span data-ttu-id="c5902-108">Inoltre, è possibile che un'autorità di certificazione pubblichi Delta CRL.</span><span class="sxs-lookup"><span data-stu-id="c5902-108">Additionally, a CA might publish delta CRLs.</span></span> <span data-ttu-id="c5902-109">Per recuperare i CRL per i certificati CA rinnovati o Delta CRL, usare i metodi [**ICertAdmin2:: GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty) o [**ICertRequest2:: GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) .</span><span class="sxs-lookup"><span data-stu-id="c5902-109">To retrieve CRLs for renewed CA certificates or delta CRLs, use either the [**ICertAdmin2::GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty) or [**ICertRequest2::GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) methods.</span></span>

<span data-ttu-id="c5902-110">Nell'esempio seguente viene illustrato il recupero del CRL corrente.</span><span class="sxs-lookup"><span data-stu-id="c5902-110">The following example shows retrieving the current CRL.</span></span>


```C++
    ICertAdmin2 * pCertAdmin2 = NULL;  // pointer to interface object
    BSTR bstrCA = NULL;  // variable for computer\CAname
    BSTR bstrCRL = NULL;  // variable to contain the retrieved CRL
    HRESULT hr;

    // Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    // Create the CertAdmin object,
    // and get a pointer to its ICertAdmin interface.
    hr = CoCreateInstance( CLSID_CCertAdmin,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertAdmin2,
                           (void **)&pCertAdmin2;);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin2 [%x]\n", hr);
        goto error;
    }

    // Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (FAILED(hr))
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    // Retrieve the CRL.
    hr = pCertAdmin2->GetCRL( bstrCA, CR_OUT_BINARY, &bstrCRL );
    if (FAILED(hr))
    {
        printf("Failed GetCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("CRL retrieved successfully\n");
        // Use the CRL as needed...

    // Processing is finished.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCRL)
        SysFreeString(bstrCRL);

    // Clean up object resources.
    if (NULL != pCertAdmin2)
        pCertAdmin2->Release();

    // Free COM resources.
    CoUninitialize();
```



<span data-ttu-id="c5902-111">Nell'esempio seguente viene illustrato come recuperare i CRL di base e Delta, inclusi quelli per i certificati della CA rinnovati.</span><span class="sxs-lookup"><span data-stu-id="c5902-111">The following example shows retrieving base and delta CRLs, including those for CA certificates that have been renewed.</span></span> <span data-ttu-id="c5902-112">L'esempio usa [**ICertAdmin2:: GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty), anche se [**ICertRequest2:: GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="c5902-112">The example uses [**ICertAdmin2::GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty), although [**ICertRequest2::GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) provides similar functionality.</span></span>


```C++
    LONG nCACertCount, nIndex, nCRLState;
    VARIANT    variant;

    VariantInit(&variant);
    // Determine the number of CA certificates.
    hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                CR_PROP_CASIGCERTCOUNT,
                                0,
                                PROPTYPE_LONG, 
                                CR_OUT_BINARY, 
                                &variant);
    if (FAILED(hr))
    {
        printf("Failed call to GetCAProperty - "
            "CR_PROP_CASIGCERTCOUNT\n");
        goto error;
    }
    nCACertCount = variant.lVal;

    for (nIndex = 0; nIndex < nCACertCount; nIndex++)
    {
           // Determine the CRL state for each certificate index.
           pCertAdmin2->GetCAProperty(bstrCA, 
                               CR_PROP_CRLSTATE, 
                               nIndex, 
                               PROPTYPE_LONG, 
                               CR_OUT_BINARY, 
                               &variant);
        if (FAILED(hr))
        {
            printf("Failed call to GetCAProperty - "
                "CR_PROP_CRLSTATE\n");
            goto error;
        }
        nCRLState = variant.lVal;

        // Process certificate indices only when 
        // the CRL state is valid.
        if (CA_DISP_VALID == nCRLState)
        {
           // Retrieve the base CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA,
                                   CR_PROP_BASECRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY,
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_BASECRL\n");
               goto error;
           }

           // Use the base CRL as needed (not shown).
           // ...

           // Retrieve the delta CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                   CR_PROP_DELTACRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY, 
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_DELTACRL\n");
               goto error;
           }

           // Use the delta CRL as needed (not shown).
           // ...

       }        
    }
    
    // Processing is finished.

error:

    // Clean up object resources.
    if ( NULL != pCertAdmin2 )
        pCertAdmin2->Release();

    // Free BSTR variables.
    if ( NULL != bstrCA )
        SysFreeString ( bstrCA );

    // Clear the variant.
    VariantClear(&variant);
```



 

 
