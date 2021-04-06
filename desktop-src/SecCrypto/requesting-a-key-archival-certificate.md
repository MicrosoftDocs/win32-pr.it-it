---
description: Viene illustrato come richiedere un certificato di archiviazione delle chiavi.
ms.assetid: a09f55c1-fb27-41e7-9a2f-617d2360c02f
title: Richiesta di un certificato di archiviazione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da1f69338ed4a41986700853ef5d46ee08612e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883294"
---
# <a name="requesting-a-key-archival-certificate"></a><span data-ttu-id="fb395-103">Richiesta di un certificato di archiviazione delle chiavi</span><span class="sxs-lookup"><span data-stu-id="fb395-103">Requesting a Key Archival Certificate</span></span>

<span data-ttu-id="fb395-104">Nell'esempio seguente viene illustrata la creazione e l'invio di una [*richiesta di certificato*](../secgloss/c-gly.md) e la ricezione del certificato di archiviazione della chiave risultante.</span><span class="sxs-lookup"><span data-stu-id="fb395-104">The following example shows creating and submitting a [*certificate request*](../secgloss/c-gly.md) and receiving the resulting key archival certificate.</span></span> <span data-ttu-id="fb395-105">Affinché questo esempio abbia esito positivo, l' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) che riceve la richiesta di certificato deve essere configurata per l'archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="fb395-105">For this example to succeed, the [*certification authority*](../secgloss/c-gly.md) (CA) that receives the certificate request must be configured for key archival.</span></span>

<span data-ttu-id="fb395-106">Nei passaggi seguenti viene descritto come creare e inviare una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="fb395-106">The following steps describe how to create and submit a certificate request.</span></span>

<span data-ttu-id="fb395-107">**Per creare e inviare una richiesta di certificato**</span><span class="sxs-lookup"><span data-stu-id="fb395-107">**To create and submit a certificate request**</span></span>

1.  <span data-ttu-id="fb395-108">Recuperare il certificato di Exchange della CA usando il metodo [**ICertRequest2:: GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) .</span><span class="sxs-lookup"><span data-stu-id="fb395-108">Retrieve the CA's exchange certificate using the [**ICertRequest2::GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) method.</span></span>
2.  <span data-ttu-id="fb395-109">Specificare che il certificato di scambio CA recuperato è il certificato di archiviazione delle chiavi utilizzando la proprietà [**ICEnroll4::P rivatekeyarchivecertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) .</span><span class="sxs-lookup"><span data-stu-id="fb395-109">Specify that the retrieved CA exchange certificate is the key archive certificate using the [**ICEnroll4::PrivateKeyArchiveCertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) property.</span></span>
3.  <span data-ttu-id="fb395-110">Creare una richiesta di certificato CMC usando il metodo [**ICEnroll4:: CreateRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) .</span><span class="sxs-lookup"><span data-stu-id="fb395-110">Create a CMC certificate request using the [**ICEnroll4::createRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) method.</span></span>
4.  <span data-ttu-id="fb395-111">Inviare la richiesta di certificato a una CA usando il metodo [**ICertRequest2:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) .</span><span class="sxs-lookup"><span data-stu-id="fb395-111">Submit the certificate request to a CA using the [**ICertRequest2::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) method.</span></span> <span data-ttu-id="fb395-112">La CA deve essere configurata in modo da supportare l'archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="fb395-112">The CA must be configured to support key archival.</span></span>

<span data-ttu-id="fb395-113">Nei passaggi seguenti viene descritto come recuperare il certificato emesso per scopi di archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="fb395-113">The following steps describe how to retrieve the issued certificate for key archival purposes.</span></span>

<span data-ttu-id="fb395-114">**Per recuperare il certificato emesso per scopi di archiviazione chiavi**</span><span class="sxs-lookup"><span data-stu-id="fb395-114">**To retrieve the issued certificate for key archival purposes**</span></span>

1.  <span data-ttu-id="fb395-115">Recuperare la risposta completa, incluso il certificato emesso, usando il metodo [**ICertRequest2:: GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) .</span><span class="sxs-lookup"><span data-stu-id="fb395-115">Retrieve the full response, including the issued certificate, using the [**ICertRequest2::GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) method.</span></span>
2.  <span data-ttu-id="fb395-116">Installare il certificato emesso usando il metodo [**ICEnroll4:: acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) .</span><span class="sxs-lookup"><span data-stu-id="fb395-116">Install the issued certificate using the [**ICEnroll4::acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) method.</span></span>

<span data-ttu-id="fb395-117">Nell'esempio seguente viene illustrata la creazione e l'invio di una richiesta di certificato e la ricezione del certificato di archiviazione della chiave risultante.</span><span class="sxs-lookup"><span data-stu-id="fb395-117">The following example shows creating and submitting a certificate request and receiving the resulting key archival certificate.</span></span>


```C++
// Pointer to interface objects.
ICEnroll4 * pEnroll = NULL;
ICertRequest2 * pRequest = NULL;

// BSTR variables.
BSTR    bstrCACert = NULL;
BSTR    bstrDN = NULL;
BSTR    bstrCertAuth = NULL;
BSTR    bstrReq = NULL;
BSTR    bstrDispMsg = NULL;
BSTR    bstrErrorMsg = NULL;

VARIANT varFullResp;

LONG    lDisp =0;
LONG    lRequestID = 0;
LONG    lStatus = 0;

HRESULT    hr;

// Initialize COM.
hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
if ( FAILED( hr ) )
{
    printf("Failed CoInitializeEx - [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Enrollment object.
hr = CoCreateInstance( CLSID_CEnroll,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICEnroll4,
                       (void **)&pEnroll);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Request object.
hr = CoCreateInstance( CLSID_CCertRequest,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICertRequest2,
                       (void **)&pRequest);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
    goto error;
}

// Allocate the BSTR that represents the certification authority.
// Note the use of '\\' to produce a single '\' in C++.
bstrCertAuth = SysAllocString(L"Server\\CertAuth");
if (NULL == bstrCertAuth)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Retrieve the CA's exchange certificate.
hr = pRequest->GetCACertificate(TRUE,
                                bstrCertAuth,
                                CR_OUT_BASE64HEADER,
                                &bstrCACert);
if (FAILED(hr))
{
    printf("Failed GetCACertificate [%x]\n", hr);
    goto error;
}

// Specify the retrieved certificate 
// as the key archive certificate.
hr = pEnroll->put_PrivateKeyArchiveCertificate(bstrCACert);
if (FAILED(hr))
{
    printf("put_PrivateKeyArchiveCertificate [%x]\n", hr);
    goto error;
}

// Create the data for the request.
// A user interface or database retrieval could
// be used instead of this example's hard-coded text.
bstrDN = SysAllocString(L"CN=UserName"    // common name
                        L",OU=UserUnit"   // org unit
                        L",O=UserOrg"     // org
                        L",L=UserCity"    // locality
                        L",S=WA"          // state
                        L",C=US");        // country/region
if (NULL == bstrDN)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Create the certificate request.
hr = pEnroll->createRequest( XECR_CMC,
                             bstrDN, 
                             NULL,
                             &bstrReq );
if ( FAILED( hr ) )
{
    printf("Failed createRequest - [%x]\n", hr);
    goto error;
}

// Submit the certificate request.
hr = pRequest->Submit( CR_IN_CMC,
                       bstrReq,
                       NULL,
                       bstrCertAuth,
                       &lDisp );
if ( FAILED( hr ) )
{
    
    printf("Failed Submit - [%x]\n", hr);  
    goto error;
}

// Evaluate the disposition of the submitted request.
switch (lDisp)
{
    case CR_DISP_ISSUED:
           printf("Certificate was issued.\n");
           break;

    case CR_DISP_ISSUED_OUT_OF_BAND:
    case CR_DISP_INCOMPLETE:
    case CR_DISP_ERROR:
    case CR_DISP_DENIED:
    case CR_DISP_UNDER_SUBMISSION:
    case CR_DISP_REVOKED:
            printf("Certificate was not issued: %d\n", lDisp);
            break;

    default:
            printf("Unexpected disposition: %d\n", lDisp);
            goto error;
}

// Retrieve the request ID.
hr = pRequest->GetRequestId(&lRequestID);
if ( FAILED(hr) )
{
    printf("Failed GetRequestId - [%x]\n", hr);  
    goto error;
}
printf("The request ID is %d\n", lRequestID);

if (CR_DISP_ISSUED != lDisp)
{
    // Provide information about why a certificate 
    // was not issued.
    
    // Retrieve the last status.
    hr = pRequest->GetLastStatus(&lStatus);
    if ( FAILED(hr) )
    {
        printf("Failed GetLastStatus - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the disposition message.
    hr = pRequest->GetDispositionMessage(&bstrDispMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetDispositionMessage - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the error message.
    hr = pRequest->GetErrorMessageText(lStatus,
                                       CR_GEMT_HRESULT_STRING,
                                       &bstrErrorMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetErrorMessageText - [%x]\n", hr);  
        goto error;
    }
    
    // Display the information and exit.
    printf("Request ID: %d\nDisposition: %S\nError: %S\n",
           lRequestID,
           bstrDispMsg,
           bstrErrorMsg);
    goto error;
}

// Retrieve the full response.
VariantInit(&varFullResp);
hr = pRequest->GetFullResponseProperty( FR_PROP_FULLRESPONSE,
                                        0,
                                        PROPTYPE_BINARY,
                                        CR_OUT_BASE64,
                                        &varFullResp );
if ( FAILED( hr ) )
{
    printf("Failed GetFullResponseProperty - [%x]\n", hr);
    goto error;
}

// Accept the response.
hr = pEnroll->acceptResponse(varFullResp.bstrVal);
if ( FAILED( hr ) )
{
    printf("Failed AcceptResponse - [%x]\n", hr);
    goto error;
}
else
{
    printf("Successfully completed processing\n");
}

error:

// Done processing.
// Clean up object resources.
if ( NULL != pEnroll )
    pEnroll->Release();
if ( NULL != pRequest )
    pRequest->Release();

// Free BSTR variables.
if ( NULL != bstrCACert )
    SysFreeString ( bstrCACert );
if ( NULL != bstrDN )
    SysFreeString ( bstrDN );
if ( NULL != bstrCertAuth )
    SysFreeString ( bstrCertAuth );
if ( NULL != bstrReq )
    SysFreeString ( bstrReq );
if ( NULL != bstrDispMsg )
    SysFreeString ( bstrDispMsg );
if ( NULL != bstrErrorMsg )
    SysFreeString ( bstrErrorMsg );

// Clear VARIANTS.
VariantClear(&varFullResp);

// Free COM resources.
CoUninitialize();

return hr;
```



 

 
