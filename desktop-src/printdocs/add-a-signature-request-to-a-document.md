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
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="1f6a4-103">Aggiungere una richiesta di firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="1f6a4-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="1f6a4-104">In questo argomento viene descritto come aggiungere una richiesta di firma a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="1f6a4-105">Una richiesta di firma richiede a un utente di firmare un documento se accetta l'intento della firma.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="1f6a4-106">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1f6a4-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="1f6a4-107">Per aggiungere una richiesta di firma a un documento XPS:</span><span class="sxs-lookup"><span data-stu-id="1f6a4-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="1f6a4-108">Caricare il documento XPS in un gestore delle firme, come descritto in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="1f6a4-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="1f6a4-109">Aggiungere un blocco di firma al gestore delle firme.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="1f6a4-110">Creare una richiesta di firma nel nuovo blocco di firma.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="1f6a4-111">Impostare le proprietà della richiesta di firma:</span><span class="sxs-lookup"><span data-stu-id="1f6a4-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="1f6a4-112">Impostare lo scopo della firma.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="1f6a4-113">Impostare il nome della persona la cui firma è richiesta (il firmatario richiesto).</span><span class="sxs-lookup"><span data-stu-id="1f6a4-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="1f6a4-114">Impostare la data di richiesta della firma.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="1f6a4-115">Impostare altre proprietà della firma come richiesto.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-115">Set other signature properties as required.</span></span>

<span data-ttu-id="1f6a4-116">Nell'esempio di codice seguente viene illustrato come aggiungere una richiesta di firma a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1f6a4-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f6a4-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1f6a4-118">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="1f6a4-119">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="1f6a4-120">**IXpsSignatureBlock:: CreateRequest**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="1f6a4-121">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="1f6a4-122">**IXpsSignatureManager::AddSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="1f6a4-123">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="1f6a4-124">**IXpsSignatureRequest:: setent**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="1f6a4-125">**IXpsSignatureRequest::SetRequestedSigner**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="1f6a4-126">**IXpsSignatureRequest::SetRequestSignByDate**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="1f6a4-127">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="1f6a4-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="1f6a4-128">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="1f6a4-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="1f6a4-129">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="1f6a4-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="1f6a4-130">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="1f6a4-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



