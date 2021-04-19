---
title: Come firmare il pacchetto di un'app tramite SignTool
description: Informazioni su come usare SignTool per firmare i pacchetti dell'app Windows in modo che possano essere distribuiti.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300602"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="a78d9-103">Come firmare il pacchetto di un'app tramite SignTool</span><span class="sxs-lookup"><span data-stu-id="a78d9-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="a78d9-104">Per la firma di un pacchetto dell'app Windows, vedere [firmare un pacchetto dell'app con SignTool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="a78d9-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="a78d9-105">Informazioni su come usare [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'app Windows in modo che possano essere distribuiti.</span><span class="sxs-lookup"><span data-stu-id="a78d9-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="a78d9-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) fa parte del Software Development Kit (SDK) di Windows.</span><span class="sxs-lookup"><span data-stu-id="a78d9-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="a78d9-107">Per poter distribuire tutti i pacchetti dell'app Windows, è necessario firmarli digitalmente.</span><span class="sxs-lookup"><span data-stu-id="a78d9-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="a78d9-108">Mentre Microsoft Visual Studio 2012 e versioni successive possono firmare un pacchetto dell'app durante la sua creazione, i pacchetti creati con lo strumento [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) del Windows SDK non sono firmati.</span><span class="sxs-lookup"><span data-stu-id="a78d9-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="a78d9-109">È possibile utilizzare [**SignTool**](/windows-hardware/drivers/devtest/signtool) solo per firmare i pacchetti dell'app Windows in Windows 8 e versioni successive o windows Server 2012 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a78d9-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="a78d9-110">Non è possibile usare **SignTool** per firmare i pacchetti dell'app nei sistemi operativi di livello inferiore, ad esempio Windows 7 o windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a78d9-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="a78d9-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="a78d9-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a78d9-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="a78d9-112">Technologies</span></span>

-   <span data-ttu-id="a78d9-113">[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a78d9-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="a78d9-114">[Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="a78d9-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="a78d9-115">Strumenti per firmare i file e controllare le firme</span><span class="sxs-lookup"><span data-stu-id="a78d9-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="a78d9-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a78d9-116">Prerequisites</span></span>

-   <span data-ttu-id="a78d9-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), che fa parte dell'Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a78d9-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="a78d9-118">Un certificato di firma codice valido, ad esempio, un file di scambio di informazioni personali (con estensione pfx) creato con gli strumenti [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)</span><span class="sxs-lookup"><span data-stu-id="a78d9-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="a78d9-119">Per informazioni sulla creazione di un certificato di firma codice valido, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="a78d9-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="a78d9-120">App di Windows in pacchetto, ad esempio un file con estensione appx creato con lo strumento [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)</span><span class="sxs-lookup"><span data-stu-id="a78d9-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="a78d9-121">**Altre considerazioni**</span><span class="sxs-lookup"><span data-stu-id="a78d9-121">**Additional considerations**</span></span>

<span data-ttu-id="a78d9-122">Il certificato usato per firmare il pacchetto dell'app deve soddisfare i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a78d9-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="a78d9-123">Il nome del soggetto del certificato deve corrispondere all'attributo del **server di pubblicazione** contenuto nell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del file AppxManifest.xml archiviato nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a78d9-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="a78d9-124">Il nome del server di pubblicazione fa parte dell'identità di un'app di Windows in pacchetto, quindi è necessario fare in modo che il nome del soggetto del certificato corrisponda al nome dell'editore dell'app.</span><span class="sxs-lookup"><span data-stu-id="a78d9-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="a78d9-125">Ciò consente di verificare l'identità dei pacchetti firmati rispetto alla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="a78d9-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="a78d9-126">Per informazioni sugli errori di firma che possono derivare dalla firma di un pacchetto dell'app con [**SignTool**](/windows-hardware/drivers/devtest/signtool), vedere la sezione Osservazioni di [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="a78d9-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="a78d9-127">Il certificato deve essere valido per la firma del codice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="a78d9-128">Ciò significa che entrambi gli elementi devono essere true:</span><span class="sxs-lookup"><span data-stu-id="a78d9-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="a78d9-129">Il campo utilizzo chiavi avanzato (EKU) del certificato deve essere annullato o contenere il valore EKU per la firma del codice (1.3.6.1.5.5.7.3.3).</span><span class="sxs-lookup"><span data-stu-id="a78d9-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="a78d9-130">Il campo utilizzo chiavi (KU) del certificato deve essere annullato o contenere il bit Usage per la firma digitale (0x80).</span><span class="sxs-lookup"><span data-stu-id="a78d9-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="a78d9-131">Il certificato contiene una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="a78d9-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="a78d9-132">Il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="a78d9-132">The certificate is valid.</span></span> <span data-ttu-id="a78d9-133">È attivo, non è scaduto e non è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="a78d9-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="a78d9-134">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a78d9-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="a78d9-135">Passaggio 1: determinare l'algoritmo hash da usare</span><span class="sxs-lookup"><span data-stu-id="a78d9-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="a78d9-136">Quando si firma il pacchetto dell'app, è necessario usare lo stesso algoritmo hash usato al momento della creazione del pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="a78d9-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="a78d9-137">Se sono state usate le impostazioni predefinite per creare il pacchetto dell'app, l'algoritmo hash usato è SHA256.</span><span class="sxs-lookup"><span data-stu-id="a78d9-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="a78d9-138">Se è stato usato il pacchetto di app con un algoritmo hash specifico per creare il pacchetto dell'app, usare lo stesso algoritmo per la firma del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a78d9-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="a78d9-139">Per determinare l'algoritmo hash da utilizzare per la firma di un pacchetto, è possibile estrarre il contenuto del pacchetto ed esaminare il file di AppxBlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="a78d9-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="a78d9-140">L'attributo **HashMethod** dell'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica l'algoritmo hash usato durante la creazione del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78d9-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="a78d9-141">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a78d9-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="a78d9-142">L'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) precedente indica che è stato usato l'algoritmo SHA256.</span><span class="sxs-lookup"><span data-stu-id="a78d9-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="a78d9-143">Questa tabella elenca il mapping degli algoritmi attualmente disponibili:</span><span class="sxs-lookup"><span data-stu-id="a78d9-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="a78d9-144">Valore **HashMethod**</span><span class="sxs-lookup"><span data-stu-id="a78d9-144">**HashMethod** value</span></span>                            | <span data-ttu-id="a78d9-145">*HashAlgorithm* da usare</span><span class="sxs-lookup"><span data-stu-id="a78d9-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="a78d9-146">SHA256 (appx predefinito)</span><span class="sxs-lookup"><span data-stu-id="a78d9-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="a78d9-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="a78d9-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="a78d9-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="a78d9-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="a78d9-149">Passaggio 2: eseguire SignTool.exe per firmare il pacchetto</span><span class="sxs-lookup"><span data-stu-id="a78d9-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="a78d9-150">**Per firmare il pacchetto con un certificato di firma da un file con estensione pfx**</span><span class="sxs-lookup"><span data-stu-id="a78d9-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="a78d9-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) imposta come valore predefinito il parametro/FD *HashAlgorithm* su SHA1 se non è specificato e SHA1 non è valido per la firma dei pacchetti dell'app.</span><span class="sxs-lookup"><span data-stu-id="a78d9-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="a78d9-152">Quindi, è necessario specificare questo parametro quando si firma un pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="a78d9-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="a78d9-153">Per firmare un pacchetto dell'app creato con l'hash SHA256 predefinito, è necessario specificare il parametro *HashAlgorithm* di/FD come SHA256:</span><span class="sxs-lookup"><span data-stu-id="a78d9-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="a78d9-154">È possibile omettere il parametro/p *password* se si usa un file con estensione pfx che non è protetto da password.</span><span class="sxs-lookup"><span data-stu-id="a78d9-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="a78d9-155">È anche possibile usare altre opzioni di selezione dei certificati supportate da [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78d9-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="a78d9-156">Per altre informazioni su queste opzioni, vedere [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="a78d9-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="a78d9-157">Non è possibile usare l'operazione timestamp di [**SignTool**](/windows-hardware/drivers/devtest/signtool) in un pacchetto dell'app firmato; l'operazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a78d9-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="a78d9-158">Se si vuole indicare il timestamp del pacchetto dell'app, è necessario eseguire questa operazione durante l'operazione di firma.</span><span class="sxs-lookup"><span data-stu-id="a78d9-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="a78d9-159">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a78d9-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="a78d9-160">Rendere il parametro/TR *timestampServerUrl* uguale all'URL per un server di timestamp RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="a78d9-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="a78d9-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="a78d9-161">Remarks</span></span>

<span data-ttu-id="a78d9-162">Questa sezione illustra la risoluzione dei problemi relativi agli errori di firma per i pacchetti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78d9-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="a78d9-163">Risoluzione degli errori di firma del pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="a78d9-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="a78d9-164">Oltre agli errori di firma che [**SignTool**](/windows-hardware/drivers/devtest/signtool) può restituire, **SignTool** può restituire anche errori specifici per la firma dei pacchetti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78d9-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="a78d9-165">Questi errori vengono in genere visualizzati come errori interni:</span><span class="sxs-lookup"><span data-stu-id="a78d9-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="a78d9-166">Se il codice di errore inizia con 0x8008, ad esempio 0x80080206 \_ appx \_ E \_ contenuto danneggiato, significa che il pacchetto firmato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a78d9-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="a78d9-167">In questo caso, prima di poter firmare il pacchetto, è necessario ricompilare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a78d9-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="a78d9-168">Per l'elenco completo degli \* errori 0x8008, vedere [**codici di errore com (sicurezza e configurazione)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="a78d9-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="a78d9-169">Più comunemente, l'errore è 0x8007000B (errore \_ nel \_ formato errato).</span><span class="sxs-lookup"><span data-stu-id="a78d9-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="a78d9-170">In questo caso, è possibile trovare informazioni più specifiche sull'errore nel registro eventi:</span><span class="sxs-lookup"><span data-stu-id="a78d9-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="a78d9-171">**Per eseguire una ricerca nel registro eventi**</span><span class="sxs-lookup"><span data-stu-id="a78d9-171">**To search the event log**</span></span>

1.  <span data-ttu-id="a78d9-172">Eseguire eventvwr. msc.</span><span class="sxs-lookup"><span data-stu-id="a78d9-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="a78d9-173">Aprire il registro eventi: Visualizzatore eventi (locale) > registri applicazioni e servizi > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="a78d9-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="a78d9-174">Cercare l'evento di errore più recente.</span><span class="sxs-lookup"><span data-stu-id="a78d9-174">Look for the most recent error event.</span></span>

<span data-ttu-id="a78d9-175">L'errore interno generalmente corrisponde a uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a78d9-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a78d9-176">ID evento</span><span class="sxs-lookup"><span data-stu-id="a78d9-176">Event ID</span></span></th>
<th><span data-ttu-id="a78d9-177">Esempio di stringa di evento</span><span class="sxs-lookup"><span data-stu-id="a78d9-177">Example event string</span></span></th>
<th><span data-ttu-id="a78d9-178">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="a78d9-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a78d9-179">150</span><span class="sxs-lookup"><span data-stu-id="a78d9-179">150</span></span></td>
<td><span data-ttu-id="a78d9-180">errore 0x8007000B: il nome del server di pubblicazione del manifesto dell'applicazione (CN = Contoso) deve corrispondere al nome del soggetto del certificato di firma (CN = Contoso, C = US).</span><span class="sxs-lookup"><span data-stu-id="a78d9-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="a78d9-181">Il nome del server di pubblicazione del manifesto dell'applicazione deve corrispondere esattamente al nome del soggetto della firma.</span><span class="sxs-lookup"><span data-stu-id="a78d9-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a78d9-182">Questi nomi sono specificati tra virgolette e sono sensibili a maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a78d9-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="a78d9-183">È possibile aggiornare la stringa dell'attributo del <strong>server di pubblicazione</strong> definita per l'elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> nel file di AppxManifest.xml in modo che corrisponda al nome del soggetto del certificato di firma designato.</span><span class="sxs-lookup"><span data-stu-id="a78d9-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="a78d9-184">In alternativa, selezionare un certificato di firma diverso con un nome soggetto corrispondente al nome del server di pubblicazione del manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78d9-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="a78d9-185">Il nome del server di pubblicazione del manifesto e il nome del soggetto del certificato sono entrambi elencati nel messaggio di evento.</span><span class="sxs-lookup"><span data-stu-id="a78d9-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a78d9-186">151</span><span class="sxs-lookup"><span data-stu-id="a78d9-186">151</span></span></td>
<td><span data-ttu-id="a78d9-187">errore 0x8007000B: il metodo hash della firma specificato (SHA512) deve corrispondere al metodo hash usato nella mappa del blocco del pacchetto dell'app (SHA256).</span><span class="sxs-lookup"><span data-stu-id="a78d9-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="a78d9-188">L'oggetto hashAlgorithm specificato nel parametro/FD non è corretto (vedere passaggio 1: determinare l'algoritmo hash da usare).</span><span class="sxs-lookup"><span data-stu-id="a78d9-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="a78d9-189">Eseguire di nuovo <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> con l'oggetto HashAlgorithm che corrisponde alla mappa del blocco del pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="a78d9-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a78d9-190">152</span><span class="sxs-lookup"><span data-stu-id="a78d9-190">152</span></span></td>
<td><span data-ttu-id="a78d9-191">errore 0x8007000B: il contenuto del pacchetto dell'app deve essere convalidato rispetto alla mappa dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="a78d9-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="a78d9-192">Il pacchetto dell'app è danneggiato e deve essere ricompilato per generare una nuova mappa a blocchi.</span><span class="sxs-lookup"><span data-stu-id="a78d9-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="a78d9-193">Per altre informazioni sulla creazione di un pacchetto dell'app, vedere Creazione di un pacchetto dell'app con <a href="make-appx-package--makeappx-exe-.md">app Packager</a> o <a href="/previous-versions/hh975357(v=vs.110)">creazione di un pacchetto dell'app con Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="a78d9-194">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="a78d9-194">Security Considerations</span></span>

<span data-ttu-id="a78d9-195">Dopo la firma del pacchetto, il certificato utilizzato per firmare il pacchetto deve essere ancora considerato attendibile dal computer in cui deve essere distribuito il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a78d9-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="a78d9-196">Aggiungendo un certificato agli [archivi certificati del computer locale](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), si influisce sull'attendibilità del certificato di tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a78d9-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="a78d9-197">Si consiglia di installare i certificati di firma del codice desiderati per testare i pacchetti dell'applicazione nell'archivio certificati persone attendibili e rimuovere tempestivamente tali certificati quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="a78d9-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="a78d9-198">Se si creano certificati di test personalizzati per la firma dei pacchetti dell'app, è anche consigliabile limitare i privilegi associati al certificato di test.</span><span class="sxs-lookup"><span data-stu-id="a78d9-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="a78d9-199">Per altre informazioni sulla creazione di certificati di test per la firma dei pacchetti dell'app, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="a78d9-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a78d9-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a78d9-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a78d9-201">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="a78d9-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="a78d9-202">Esempio di creare un pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="a78d9-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="a78d9-203">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="a78d9-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="a78d9-204">[Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a78d9-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a78d9-205">[Firma di un pacchetto in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="a78d9-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="a78d9-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="a78d9-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="a78d9-207">App Packager (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="a78d9-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="a78d9-208">Come creare un certificato di firma del pacchetto di un'app</span><span class="sxs-lookup"><span data-stu-id="a78d9-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

