---
title: Come creare un certificato di firma per pacchetti app
description: Informazioni su come usare MakeCert.exe e Pvk2Pfx.exe per creare un certificato di firma del codice di test, in modo che sia possibile firmare i pacchetti dell'app Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046568"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="845cb-103">Come creare un certificato di firma per pacchetti app</span><span class="sxs-lookup"><span data-stu-id="845cb-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="845cb-104">MakeCert.exe è deprecato.</span><span class="sxs-lookup"><span data-stu-id="845cb-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="845cb-105">Per informazioni aggiornate sulla creazione di un certificato, vedere [creare un certificato per la firma del pacchetto](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="845cb-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="845cb-106">Informazioni su come usare [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) per creare un certificato di firma del codice di test, in modo che sia possibile firmare i pacchetti dell'app Windows.</span><span class="sxs-lookup"><span data-stu-id="845cb-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="845cb-107">È necessario firmare digitalmente le app di Windows in pacchetto prima di distribuirle.</span><span class="sxs-lookup"><span data-stu-id="845cb-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="845cb-108">Se non si usa Microsoft Visual Studio 2012 per creare e firmare i pacchetti dell'app, è necessario creare e gestire i propri certificati di firma del codice.</span><span class="sxs-lookup"><span data-stu-id="845cb-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="845cb-109">È possibile creare certificati usando [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) da Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="845cb-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="845cb-110">È quindi possibile usare i certificati per firmare i pacchetti dell'app, in modo che possano essere distribuiti localmente per il test.</span><span class="sxs-lookup"><span data-stu-id="845cb-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="845cb-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="845cb-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="845cb-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="845cb-112">Technologies</span></span>

-   <span data-ttu-id="845cb-113">[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="845cb-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="845cb-114">[Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="845cb-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="845cb-115">Strumenti per la firma dei driver</span><span class="sxs-lookup"><span data-stu-id="845cb-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="845cb-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="845cb-116">Prerequisites</span></span>

-   <span data-ttu-id="845cb-117">Strumenti di [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) da WDK</span><span class="sxs-lookup"><span data-stu-id="845cb-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="845cb-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="845cb-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="845cb-119">Passaggio 1: determinare il nome del server di pubblicazione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="845cb-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="845cb-120">Per rendere il certificato di firma creato utilizzabile con il pacchetto dell'app che si vuole firmare, il nome del soggetto del certificato di firma deve corrispondere all'attributo **Publisher** dell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml per tale app.</span><span class="sxs-lookup"><span data-stu-id="845cb-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="845cb-121">Si supponga, ad esempio, che il AppxManifest.xml contenga:</span><span class="sxs-lookup"><span data-stu-id="845cb-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="845cb-122">Per il parametro *PublisherName* specificato con l'utilità [**Makecert**](/windows-hardware/drivers/devtest/makecert) nel passaggio successivo, usare "CN = Contoso software, O = Contoso Corporation, C = US".</span><span class="sxs-lookup"><span data-stu-id="845cb-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="845cb-123">Questa stringa di parametro è specificata tra virgolette e fa distinzione tra maiuscole e minuscole e spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="845cb-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="845cb-124">La stringa dell'attributo **Publisher** definita per l'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml deve essere identica alla stringa specificata con il parametro [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n per il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="845cb-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="845cb-125">Copiare e incollare la stringa dove possibile.</span><span class="sxs-lookup"><span data-stu-id="845cb-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="845cb-126">Passaggio 2: creare una chiave privata utilizzando MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="845cb-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="845cb-127">Usare l'utilità [**Makecert**](/windows-hardware/drivers/devtest/makecert) per creare un certificato di prova autofirmato e una chiave privata:</span><span class="sxs-lookup"><span data-stu-id="845cb-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="845cb-128">Questo comando richiede di specificare una password per il file con estensione PVK.</span><span class="sxs-lookup"><span data-stu-id="845cb-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="845cb-129">Si consiglia di scegliere una [password complessa](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) e di proteggere la chiave privata in un luogo sicuro.</span><span class="sxs-lookup"><span data-stu-id="845cb-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="845cb-130">Per questi motivi, è consigliabile usare i parametri suggeriti nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="845cb-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="845cb-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="845cb-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="845cb-132">Crea un certificato radice autofirmato.</span><span class="sxs-lookup"><span data-stu-id="845cb-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="845cb-133">Ciò semplifica la gestione del certificato di test.</span><span class="sxs-lookup"><span data-stu-id="845cb-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="845cb-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="845cb-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="845cb-135">Contrassegna il vincolo di base per il certificato come entità finale.</span><span class="sxs-lookup"><span data-stu-id="845cb-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="845cb-136">In questo modo si impedisce che il certificato venga usato come autorità di certificazione (CA) che può emettere altri certificati.</span><span class="sxs-lookup"><span data-stu-id="845cb-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="845cb-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="845cb-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="845cb-138">Imposta i valori di utilizzo chiavi avanzato (EKU) per il certificato.</span><span class="sxs-lookup"><span data-stu-id="845cb-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="845cb-139">Non inserire uno spazio tra i due valori delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="845cb-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="845cb-140">1.3.6.1.5.5.7.3.3 indica che il certificato è valido per la firma del codice.</span><span class="sxs-lookup"><span data-stu-id="845cb-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="845cb-141">Specificare sempre questo valore per limitare l'utilizzo previsto per il certificato.</span><span class="sxs-lookup"><span data-stu-id="845cb-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="845cb-142">1.3.6.1.4.1.311.10.3.13 indica che il certificato rispetta la firma del ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="845cb-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="845cb-143">In genere, se una firma viene contrassegnata con un timestamp, purché il certificato sia valido nel momento in cui è stato indicato il timestamp, la firma rimane valida anche se il certificato scade.</span><span class="sxs-lookup"><span data-stu-id="845cb-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="845cb-144">Questo EKU impone la scadenza della firma, indipendentemente dal fatto che la firma sia contrassegnata con il timestamp.</span><span class="sxs-lookup"><span data-stu-id="845cb-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="845cb-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="845cb-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="845cb-146">Imposta la data di scadenza del certificato.</span><span class="sxs-lookup"><span data-stu-id="845cb-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="845cb-147">Specificare un valore per il parametro *expirationDate* nel formato mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="845cb-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="845cb-148">Si consiglia di scegliere una data di scadenza solo se necessario a scopo di test, in genere inferiore a un anno.</span><span class="sxs-lookup"><span data-stu-id="845cb-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="845cb-149">Questa data di scadenza insieme all'EKU per la firma di durata può contribuire a limitare la finestra in cui il certificato può essere compromesso e usato in modo improprio.</span><span class="sxs-lookup"><span data-stu-id="845cb-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="845cb-150">Per altre informazioni sulle altre opzioni, vedere [**Makecert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="845cb-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="845cb-151">Passaggio 3: creare un file di scambio di informazioni personali (con estensione pfx) usando Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="845cb-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="845cb-152">Usare l'utilità [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) per convertire i file con estensione PVK e CER creati da [**Makecert**](/windows-hardware/drivers/devtest/makecert) in un file con estensione pfx che è possibile usare con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app:</span><span class="sxs-lookup"><span data-stu-id="845cb-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="845cb-153">I file *myKey. PVK* e *myKey. cer* sono gli stessi che [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) creati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="845cb-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="845cb-154">Utilizzando il parametro facoltativo/po, è possibile specificare una password diversa per il file con estensione pfx risultante; in caso contrario, il file con estensione pfx ha la stessa password di *myKey. PVK*.</span><span class="sxs-lookup"><span data-stu-id="845cb-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="845cb-155">Per ulteriori informazioni sulle altre opzioni, vedere [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="845cb-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="845cb-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="845cb-156">Remarks</span></span>

<span data-ttu-id="845cb-157">Dopo aver creato il file con estensione pfx, è possibile usare il file con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="845cb-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="845cb-158">Per altre informazioni, vedere [come firmare un pacchetto dell'app usando SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="845cb-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="845cb-159">Ma il certificato non è ancora considerato attendibile dal computer locale per la distribuzione dei pacchetti dell'app finché non viene installato nell'archivio certificati attendibili del computer locale.</span><span class="sxs-lookup"><span data-stu-id="845cb-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="845cb-160">È possibile utilizzare [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), disponibile in Windows.</span><span class="sxs-lookup"><span data-stu-id="845cb-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="845cb-161">**Per installare i certificati con WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="845cb-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="845cb-162">Eseguire **Cmd.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="845cb-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="845cb-163">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="845cb-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="845cb-164">Si consiglia di rimuovere i certificati se non sono più in uso.</span><span class="sxs-lookup"><span data-stu-id="845cb-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="845cb-165">Dallo stesso prompt dei comandi dell'amministratore eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="845cb-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="845cb-166">**CertID** è il numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="845cb-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="845cb-167">Eseguire questo comando per determinare il numero di serie del certificato:</span><span class="sxs-lookup"><span data-stu-id="845cb-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="845cb-168">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="845cb-168">Security Considerations</span></span>

<span data-ttu-id="845cb-169">Aggiungendo un certificato agli [archivi certificati del computer locale](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), si influisce sull'attendibilità del certificato di tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="845cb-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="845cb-170">Si consiglia di installare i certificati di firma del codice desiderati per testare i pacchetti dell'applicazione nell'archivio certificati persone attendibili.</span><span class="sxs-lookup"><span data-stu-id="845cb-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="845cb-171">Rimuovere tempestivamente questi certificati quando non sono più necessari, per impedire che vengano usati per compromettere l'attendibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="845cb-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="845cb-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="845cb-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="845cb-173">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="845cb-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="845cb-174">Esempio di creare un pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="845cb-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="845cb-175">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="845cb-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="845cb-176">[Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="845cb-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="845cb-177">Come firmare un pacchetto di app con SignTool</span><span class="sxs-lookup"><span data-stu-id="845cb-177">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

<span data-ttu-id="845cb-178">[Firma di un pacchetto di app](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="845cb-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 