---
description: In questo argomento vengono elencate alcune considerazioni relative all'utilizzo dell'API di firma digitale XPS per aggiungere firme digitali a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso dell'API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881598"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="0c0bb-103">Uso dell'API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="0c0bb-104">In questo argomento vengono elencate alcune considerazioni relative all'utilizzo dell'API di firma digitale XPS per aggiungere firme digitali a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="0c0bb-105">L'API di firma digitale XPS consente alle applicazioni di richiedere agli utenti di firmare i documenti XPS e di verificare le firme presenti nei documenti XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="0c0bb-106">L'API di firma digitale XPS può essere applicata a un documento XPS senza caricarla in un OM XPS e può essere usata nei flussi di documenti XPS serializzati da un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="0c0bb-107">La sezione [attività di programmazione API di firma digitale XPS](#xps-digital-signature-api-programming-tasks) contiene argomenti che descrivono come programmare con l'API di firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="0c0bb-108">Questo argomento elenca le considerazioni seguenti per l'uso dell'API di firma digitale XPS quando si aggiunge il supporto per la firma digitale a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="0c0bb-109">Attività di programmazione API per la firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="0c0bb-110">Note speciali sulla programmazione dell'API per la firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="0c0bb-111">Verifica delle firme digitali in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="0c0bb-112">Criteri firma digitale firma</span><span class="sxs-lookup"><span data-stu-id="0c0bb-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="0c0bb-113">Incorporamento di una catena di certificati</span><span class="sxs-lookup"><span data-stu-id="0c0bb-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="0c0bb-114">Uso della struttura del contesto del certificato \_</span><span class="sxs-lookup"><span data-stu-id="0c0bb-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="0c0bb-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c0bb-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="0c0bb-116">Attività di programmazione API per la firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="0c0bb-117">Questa sezione contiene argomenti che descrivono come eseguire attività di programmazione tramite l'API di firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="0c0bb-118">Attività comuni di programmazione della firma digitale</span><span class="sxs-lookup"><span data-stu-id="0c0bb-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="0c0bb-119">Inizializzazione di gestione firme</span><span class="sxs-lookup"><span data-stu-id="0c0bb-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="0c0bb-120">Firmare un documento</span><span class="sxs-lookup"><span data-stu-id="0c0bb-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="0c0bb-121">Aggiungere una richiesta di firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="0c0bb-122">Verificare le firme del documento</span><span class="sxs-lookup"><span data-stu-id="0c0bb-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="0c0bb-123">Attività aggiuntive di programmazione della firma digitale</span><span class="sxs-lookup"><span data-stu-id="0c0bb-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="0c0bb-124">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="0c0bb-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="0c0bb-125">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="0c0bb-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="0c0bb-126">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="0c0bb-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="0c0bb-127">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="0c0bb-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="0c0bb-128">Note speciali sulla programmazione dell'API per la firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="0c0bb-129">Gli argomenti seguenti richiedono una particolare attenzione quando si usa l'API di firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="0c0bb-130">Verifica delle firme digitali in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="0c0bb-131">Criteri firma digitale firma</span><span class="sxs-lookup"><span data-stu-id="0c0bb-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="0c0bb-132">Incorporamento di una catena di certificati</span><span class="sxs-lookup"><span data-stu-id="0c0bb-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="0c0bb-133">Uso della struttura del contesto del certificato \_</span><span class="sxs-lookup"><span data-stu-id="0c0bb-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="0c0bb-134">Verifica delle firme digitali in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="0c0bb-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="0c0bb-135">[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) controlla solo il contenuto firmato per determinare che non è stato modificato dopo che è stato firmato.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="0c0bb-136">**IXpsSignature:: Verify** non verifica alcun certificato usato per firmare il contenuto del documento.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="0c0bb-137">Per ulteriori informazioni sui certificati e sulla crittografia, vedere [informazioni sulla crittografia](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="0c0bb-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="0c0bb-138">Per un esempio di come verificare le firme dei documenti in un programma, vedere [verificare le firme e i certificati del documento](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="0c0bb-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="0c0bb-139">Criteri firma digitale firma</span><span class="sxs-lookup"><span data-stu-id="0c0bb-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="0c0bb-140">I criteri di firma della firma digitale determinano quali parti di un documento XPS sono firmate.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="0c0bb-141">Un'opzione per i criteri di firma consiste nel firmare le relazioni di firma che iniziano dalla parte dell'origine della firma.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="0c0bb-142">Poiché le relazioni di firma cambiano con ogni firma aggiunta, le firme eseguite in questo criterio si interrompono quando vengono aggiunte nuove firme.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="0c0bb-143">Assicurarsi di comprendere chiaramente le implicazioni e gli effetti dell'impostazione di questi criteri. in caso contrario, potrebbe verificarsi un comportamento imprevisto o indesiderato.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="0c0bb-144">Per ulteriori informazioni sui criteri di firma, [**vedere \_ \_ criteri**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)di firma XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="0c0bb-145">Incorporamento di una catena di certificati</span><span class="sxs-lookup"><span data-stu-id="0c0bb-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="0c0bb-146">I certificati che costituiscono la catena di attendibilità di un certificato specifico possono essere aggiunti a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="0c0bb-147">Incorporando questi certificati è possibile semplificare, in scenari non in linea, che un'applicazione verifichi i certificati utilizzati da una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="0c0bb-148">Per altre informazioni su come incorporare i certificati in un documento XPS, vedere [incorporare le catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="0c0bb-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="0c0bb-149">Uso della struttura del contesto del certificato \_</span><span class="sxs-lookup"><span data-stu-id="0c0bb-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="0c0bb-150">Il [**\_ contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato e le strutture di [**\_ informazioni**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) sui certificati sono le strutture di dati principali che contengono le informazioni sul certificato.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="0c0bb-151">Per altre informazioni sull'uso di queste strutture, vedere [uso di una \_ struttura di dati CERT info](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="0c0bb-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="0c0bb-152">[**Certificato \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Le strutture di contesto restituite dalle funzioni API di crittografia devono essere rilasciate quando non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="0c0bb-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="0c0bb-153">Per rilasciare una struttura del **\_ contesto del certificato** , chiamare la funzione [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="0c0bb-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c0bb-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c0bb-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c0bb-155">Attività comuni di programmazione della firma digitale</span><span class="sxs-lookup"><span data-stu-id="0c0bb-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="0c0bb-156">Attività aggiuntive di programmazione della firma digitale</span><span class="sxs-lookup"><span data-stu-id="0c0bb-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="0c0bb-157">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="0c0bb-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="0c0bb-158">**informazioni sul certificato \_**</span><span class="sxs-lookup"><span data-stu-id="0c0bb-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="0c0bb-159">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="0c0bb-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="0c0bb-160">**\_criteri di firma XPS \_**</span><span class="sxs-lookup"><span data-stu-id="0c0bb-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="0c0bb-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="0c0bb-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
