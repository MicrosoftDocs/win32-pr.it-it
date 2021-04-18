---
description: In questo argomento viene descritto come aggiungere una richiesta di firma a un documento XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Aggiungere una richiesta di firma a un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316427"
---
# <a name="add-a-signature-request-to-an-xps-document"></a>Aggiungere una richiesta di firma a un documento XPS

In questo argomento viene descritto come aggiungere una richiesta di firma a un documento XPS. Una richiesta di firma richiede a un utente di firmare un documento se accetta l'intento della firma.

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).

Per aggiungere una richiesta di firma a un documento XPS:

1.  Caricare il documento XPS in un gestore delle firme, come descritto in [Initialize the Signature Manager](initialize-the-signature-manager.md).
2.  Aggiungere un blocco di firma al gestore delle firme.
3.  Creare una richiesta di firma nel nuovo blocco di firma.
4.  Impostare le proprietà della richiesta di firma:
    1.  Impostare lo scopo della firma.
    2.  Impostare il nome della persona la cui firma è richiesta (il firmatario richiesto).
    3.  Impostare la data di richiesta della firma.
    4.  Impostare altre proprietà della firma come richiesto.

Nell'esempio di codice seguente viene illustrato come aggiungere una richiesta di firma a un documento XPS.


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[**IXpsSignatureBlock:: CreateRequest**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::AddSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[**IXpsSignatureRequest:: setent**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestedSigner**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestSignByDate**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Errori dell'API firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori del documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



