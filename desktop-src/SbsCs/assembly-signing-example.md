---
description: Nell'esempio seguente viene illustrato come generare un assembly affiancato firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Esempio di firma degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322040"
---
# <a name="assembly-signing-example"></a><span data-ttu-id="90390-103">Esempio di firma degli assembly</span><span class="sxs-lookup"><span data-stu-id="90390-103">Assembly Signing Example</span></span>

<span data-ttu-id="90390-104">Nell'esempio seguente viene illustrato come generare un assembly affiancato firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly.</span><span class="sxs-lookup"><span data-stu-id="90390-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="90390-105">Gli assembly side-by-side condivisi devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="90390-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="90390-106">Il sistema operativo verifica la firma dell'assembly prima di installare un assembly condiviso nell'archivio side-by-side globale (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="90390-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="90390-107">In questo modo è difficile eseguire lo spoofing dell'editore dell'assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="90390-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="90390-108">Si noti che la modifica dei file di assembly o del contenuto del manifesto dopo la generazione del catalogo degli assembly invalida il catalogo e l'assembly.</span><span class="sxs-lookup"><span data-stu-id="90390-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="90390-109">Se è necessario aggiornare i file di assembly o il manifesto dopo la creazione e la firma del catalogo, è necessario firmare di nuovo l'assembly e generare un nuovo catalogo.</span><span class="sxs-lookup"><span data-stu-id="90390-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="90390-110">Iniziare con i file di assembly, il manifesto dell'assembly e il file del certificato che si userà per firmare l'assembly.</span><span class="sxs-lookup"><span data-stu-id="90390-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="90390-111">Il file del certificato deve avere una lunghezza di 2048 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="90390-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="90390-112">Non è necessario usare un certificato attendibile.</span><span class="sxs-lookup"><span data-stu-id="90390-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="90390-113">Il certificato viene usato solo per verificare che l'assembly non sia stato danneggiato.</span><span class="sxs-lookup"><span data-stu-id="90390-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="90390-114">Eseguire l'utilità di [Pktextract.exe](pktextract-exe.md) fornita nel Software Development Kit (SDK) di Microsoft Windows per estrarre il token di chiave pubblica dal file del certificato.</span><span class="sxs-lookup"><span data-stu-id="90390-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="90390-115">Per il corretto funzionamento di Pktextract, il file del certificato deve essere presente nella stessa directory dell'utilità.</span><span class="sxs-lookup"><span data-stu-id="90390-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="90390-116">Usare il valore del token di chiave pubblica Estratto per aggiornare l'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="90390-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="90390-117">Di seguito è riportato un esempio di un file manifesto denominato MySampleAssembly. manifest.</span><span class="sxs-lookup"><span data-stu-id="90390-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="90390-118">L'assembly MySampleAssembly contiene un solo file, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="90390-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="90390-119">Si noti che il valore dell'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** è stato aggiornato con il valore del token di chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="90390-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

<span data-ttu-id="90390-120">Eseguire quindi l'utilità [Mt.exe](mt-exe.md) fornita nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="90390-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="90390-121">I file di assembly devono trovarsi nella stessa directory del manifesto.</span><span class="sxs-lookup"><span data-stu-id="90390-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="90390-122">In questo esempio si tratta della directory MySampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="90390-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="90390-123">Chiamare Mt.exe per l'esempio come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="90390-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="90390-124">**c: \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="90390-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="90390-125">Ecco come appare il manifesto di esempio dopo l'esecuzione Mt.exe.</span><span class="sxs-lookup"><span data-stu-id="90390-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="90390-126">Si noti che l'esecuzione di Mt.exe con l'opzione hashupdate aggiunge l'hash SHA-1 del file.</span><span class="sxs-lookup"><span data-stu-id="90390-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="90390-127">Non modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="90390-127">Do not change this value.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

<span data-ttu-id="90390-128">L'esecuzione di Mt.exe con l'opzione-makecdfs genera un file denominato MySampleAssembly. manifest. CDF che descrive il contenuto del catalogo di sicurezza che verrà usato per convalidare il manifesto.</span><span class="sxs-lookup"><span data-stu-id="90390-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="90390-129">Il passaggio successivo consiste nell'eseguire Makecat.exe su questo. CDF per creare il catalogo di sicurezza per l'assembly.</span><span class="sxs-lookup"><span data-stu-id="90390-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="90390-130">La chiamata a Makecat.exe per questo esempio apparirà come segue:</span><span class="sxs-lookup"><span data-stu-id="90390-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="90390-131">**c: \\ MySampleAssembly>MakeCat MySampleAssembly. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="90390-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="90390-132">Il passaggio finale consiste nell'eseguire SignTool.exe per firmare il file di catalogo con il certificato.</span><span class="sxs-lookup"><span data-stu-id="90390-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="90390-133">Deve corrispondere allo stesso certificato usato in precedenza per generare il token di chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="90390-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="90390-134">Per ulteriori informazioni su SignTool.exe vedere l'argomento [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="90390-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="90390-135">La chiamata a **SignTool** per l'esempio apparirà come segue:</span><span class="sxs-lookup"><span data-stu-id="90390-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="90390-136">**c: \\ MySampleAssembly>signtool sign/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="90390-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="90390-137">Se si dispone di un certificato digitale autenticato e l'autorità di certificazione usa il formato di file PVK per archiviare la chiave privata, è possibile usare l'utilità di importazione dei file di certificato digitale PVK (pvkimprt.exe) per importare la chiave nel provider del servizio di crittografia (CSP).</span><span class="sxs-lookup"><span data-stu-id="90390-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="90390-138">Questa utilità consente di esportare nel formato standard del settore PFX/P12.</span><span class="sxs-lookup"><span data-stu-id="90390-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="90390-139">Per ulteriori informazioni sull'utilità di importazione dei file di certificato digitale PVK, vedere la sezione relativa alle risorse di distribuzione in MSDN Library o contattare l'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="90390-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="90390-140">Potrebbe essere possibile ottenere pvkimprt.exe da https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="90390-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="90390-141">Vedere anche [creazione di file e cataloghi firmati](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="90390-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
