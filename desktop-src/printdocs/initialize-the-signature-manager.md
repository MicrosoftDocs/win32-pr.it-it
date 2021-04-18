---
description: Questo argomento descrive come inizializzare Gestione firme per l'uso con un documento XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Inizializzazione di gestione firme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318374"
---
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="0afa6-103">Inizializzazione di gestione firme</span><span class="sxs-lookup"><span data-stu-id="0afa6-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="0afa6-104">Questo argomento descrive come inizializzare Gestione firme per l'uso con un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="0afa6-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="0afa6-105">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0afa6-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="0afa6-106">Per usare le funzionalità di Windows 7 dell'API Crypto, definire le **informazioni sull'OID di Crypt \_ \_ con i \_ \_ \_ campi aggiuntivi** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0afa6-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="0afa6-107">Successivamente, creare un'istanza di un'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="0afa6-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



<span data-ttu-id="0afa6-108">L'interfaccia di cui è stata creata un'istanza da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) può essere utilizzata da un solo documento XPS, che deve essere caricato chiamando [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) prima di chiamare qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="0afa6-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="0afa6-109">Dopo che è stata creata un'istanza dell'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) ed è stato caricato un documento XPS, il gestore delle firme è pronto per l'uso.</span><span class="sxs-lookup"><span data-stu-id="0afa6-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0afa6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0afa6-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0afa6-111">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="0afa6-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="0afa6-112">Firmare un documento</span><span class="sxs-lookup"><span data-stu-id="0afa6-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="0afa6-113">Aggiungere una richiesta di firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0afa6-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="0afa6-114">Verificare le firme del documento</span><span class="sxs-lookup"><span data-stu-id="0afa6-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="0afa6-115">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="0afa6-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="0afa6-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="0afa6-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="0afa6-117">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="0afa6-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="0afa6-118">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="0afa6-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="0afa6-119">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0afa6-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="0afa6-120">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="0afa6-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="0afa6-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="0afa6-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
