---
description: "Usare il metodo ICertServerPolicy:: SetCertificateProperty per impostare le proprietà dell'oggetto di un certificato."
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Impostazione delle proprietà del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305601"
---
# <a name="setting-certificate-properties"></a><span data-ttu-id="a34cf-103">Impostazione delle proprietà del certificato</span><span class="sxs-lookup"><span data-stu-id="a34cf-103">Setting Certificate Properties</span></span>

<span data-ttu-id="a34cf-104">Usare il metodo [**ICertServerPolicy:: SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) per impostare le proprietà dell'oggetto di un certificato.</span><span class="sxs-lookup"><span data-stu-id="a34cf-104">Use the [**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the subject properties of a certificate.</span></span> <span data-ttu-id="a34cf-105">Le proprietà dell'oggetto sono proprietà correlate al proprietario del certificato o alla persona che ha richiesto il certificato.</span><span class="sxs-lookup"><span data-stu-id="a34cf-105">Subject properties are properties related to the owner of the certificate or the individual who requested the certificate.</span></span> <span data-ttu-id="a34cf-106">Per un elenco delle proprietà dell'oggetto, vedere [proprietà del nome](name-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a34cf-106">For a list of subject properties, see [Name Properties](name-properties.md).</span></span>

<span data-ttu-id="a34cf-107">È anche possibile usare il metodo [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) per impostare le proprietà del certificato NotBefore e NotAfter.</span><span class="sxs-lookup"><span data-stu-id="a34cf-107">You can also use the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the NotBefore and NotAfter certificate properties.</span></span> <span data-ttu-id="a34cf-108">Per una descrizione delle proprietà del certificato NotBefore e NotAfter, vedere [Proprietà](certificate-properties.md)del certificato.</span><span class="sxs-lookup"><span data-stu-id="a34cf-108">For a description of the NotBefore and NotAfter certificate properties, see [Certificate Properties](certificate-properties.md).</span></span>

<span data-ttu-id="a34cf-109">Usare il metodo [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) per aggiungere un numero qualsiasi di estensioni al certificato.</span><span class="sxs-lookup"><span data-stu-id="a34cf-109">Use the [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) method to add any number of extensions to the certificate.</span></span> <span data-ttu-id="a34cf-110">È possibile utilizzare le estensioni per aggiungere al certificato informazioni aggiuntive sull'oggetto o sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a34cf-110">You can use extensions to add supplemental subject or usage information to the certificate.</span></span> <span data-ttu-id="a34cf-111">Per altre informazioni, vedere [gestori di estensioni](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a34cf-111">For more information, see [Extension Handlers](extension-handlers.md).</span></span>

<span data-ttu-id="a34cf-112">Nell'esempio seguente vengono impostate una proprietà e un'estensione del certificato in un certificato.</span><span class="sxs-lookup"><span data-stu-id="a34cf-112">The following example sets a certificate property and extension on a certificate.</span></span> <span data-ttu-id="a34cf-113">È possibile chiamare i metodi [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) e [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) nell'implementazione di [**ICertPolicy2:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) .</span><span class="sxs-lookup"><span data-stu-id="a34cf-113">You call the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) and [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) methods in your [**ICertPolicy2::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) implementation.</span></span> <span data-ttu-id="a34cf-114">L'esempio non è un'implementazione **VerifyRequest** completa; Nell'esempio non viene mostrata la logica di verifica.</span><span class="sxs-lookup"><span data-stu-id="a34cf-114">The example is not a complete **VerifyRequest** implementation; the example does not show verification logic.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



