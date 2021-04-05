---
title: Strumento per la creazione di pacchetti di app (MakeAppx.exe)
description: App Packager (MakeAppx.exe) crea un pacchetto dell'app da file su disco o estrae i file da un pacchetto dell'app su disco.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117578"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="f818d-103">Strumento per la creazione di pacchetti di app (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="f818d-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="f818d-104">Per indicazioni su UWP sull'uso di questo strumento, vedere [creare un pacchetto dell'app con lo strumento MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="f818d-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="f818d-105">App Packager (MakeAppx.exe) crea un pacchetto dell'app da file su disco o estrae i file da un pacchetto dell'app su disco.</span><span class="sxs-lookup"><span data-stu-id="f818d-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="f818d-106">A partire da Windows 8.1, app Packager crea anche un bundle del pacchetto dell'app dai pacchetti dell'app su disco o estrae i pacchetti dell'app da un bundle del pacchetto dell'app su disco.</span><span class="sxs-lookup"><span data-stu-id="f818d-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="f818d-107">È incluso in Microsoft Visual Studio e Windows Software Development Kit (SDK) per Windows 8 o Windows Software Development Kit (SDK) per Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="f818d-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="f818d-108">Visitare [i download per gli sviluppatori]( https://msdn.microsoft.com/windows/apps/br229516.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f818d-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="f818d-109">Lo strumento MakeAppx.exe si trova in genere in questi percorsi:</span><span class="sxs-lookup"><span data-stu-id="f818d-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="f818d-110">In x86: C: \\ Program Files (x86) \\ windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ program files (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="f818d-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="f818d-111">In x64 in due posizioni:</span><span class="sxs-lookup"><span data-stu-id="f818d-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="f818d-112">C: \\ programmi (x86) \\ windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe o c: \\ program files (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="f818d-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="f818d-113">C: \\ programmi (x86) \\ windows Kit \\ 8,0 \\ bin \\ x64 \\makeappx.exe o c: \\ programmi (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="f818d-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="f818d-114">Non è disponibile alcuna versione ARM dello strumento.</span><span class="sxs-lookup"><span data-stu-id="f818d-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="f818d-115">Per creare un pacchetto utilizzando una struttura di directory</span><span class="sxs-lookup"><span data-stu-id="f818d-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="f818d-116">Per creare un pacchetto usando un file di mapping</span><span class="sxs-lookup"><span data-stu-id="f818d-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="f818d-117">Per firmare il pacchetto con SignTool</span><span class="sxs-lookup"><span data-stu-id="f818d-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="f818d-118">Per estrarre i file da un pacchetto</span><span class="sxs-lookup"><span data-stu-id="f818d-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="f818d-119">Per creare un bundle di pacchetti usando una struttura di directory</span><span class="sxs-lookup"><span data-stu-id="f818d-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="f818d-120">Per creare un bundle di pacchetti usando un file di mapping</span><span class="sxs-lookup"><span data-stu-id="f818d-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="f818d-121">Per estrarre i pacchetti da un bundle</span><span class="sxs-lookup"><span data-stu-id="f818d-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="f818d-122">Per crittografare un pacchetto con un file di chiave</span><span class="sxs-lookup"><span data-stu-id="f818d-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="f818d-123">Per crittografare un pacchetto con una chiave di test globale</span><span class="sxs-lookup"><span data-stu-id="f818d-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="f818d-124">Per decrittografare un pacchetto con un file di chiave</span><span class="sxs-lookup"><span data-stu-id="f818d-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="f818d-125">Per decrittografare un pacchetto con una chiave di test globale</span><span class="sxs-lookup"><span data-stu-id="f818d-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="f818d-126">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f818d-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="f818d-127">Uso del pacchetto di app</span><span class="sxs-lookup"><span data-stu-id="f818d-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="f818d-128">I percorsi relativi sono supportati in tutto lo strumento.</span><span class="sxs-lookup"><span data-stu-id="f818d-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="f818d-129">Per creare un pacchetto utilizzando una struttura di directory</span><span class="sxs-lookup"><span data-stu-id="f818d-129">To create a package using a directory structure</span></span>

<span data-ttu-id="f818d-130">Inserire il AppxManifest.xml nella radice di una directory contenente tutti i file di payload per l'app.</span><span class="sxs-lookup"><span data-stu-id="f818d-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="f818d-131">Viene creata una struttura di directory identica per il pacchetto dell'app e sarà disponibile quando il pacchetto viene estratto in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f818d-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="f818d-132">Inserire tutti i file in un'unica struttura di directory, creando sottodirectory come desiderato.</span><span class="sxs-lookup"><span data-stu-id="f818d-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="f818d-133">Creare un manifesto del pacchetto valido, AppxManifest.xml e inserirlo nella directory radice.</span><span class="sxs-lookup"><span data-stu-id="f818d-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="f818d-134">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-134">Run this command:</span></span>

    <span data-ttu-id="f818d-135">**MakeAppx Pack/d** *input \_ DirectoryPath* **/p** _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="f818d-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="f818d-136">Per creare un pacchetto usando un file di mapping</span><span class="sxs-lookup"><span data-stu-id="f818d-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="f818d-137">Creare un manifesto del pacchetto valido, AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="f818d-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="f818d-138">Creare un file di mapping.</span><span class="sxs-lookup"><span data-stu-id="f818d-138">Create a mapping file.</span></span> <span data-ttu-id="f818d-139">La prima riga contiene i **\[ file \]** di stringa e le righe che seguono specificano i percorsi di origine (disco) e di destinazione (pacchetto) nelle stringhe tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="f818d-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="f818d-140">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-140">Run this command:</span></span>

    <span data-ttu-id="f818d-141">**MakeAppx Pack/f** *mapping \_ filePath* **/p** _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="f818d-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="f818d-142">Per firmare il pacchetto con SignTool</span><span class="sxs-lookup"><span data-stu-id="f818d-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="f818d-143">Creare il certificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-143">Create the certificate.</span></span> <span data-ttu-id="f818d-144">Il server di pubblicazione elencato nel manifesto deve corrispondere alle informazioni sul soggetto dell'editore del certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="f818d-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="f818d-145">Per altre informazioni sulla creazione di un certificato di firma, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="f818d-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="f818d-146">Eseguire SignTool.exe per firmare il pacchetto:</span><span class="sxs-lookup"><span data-stu-id="f818d-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="f818d-147">**Segno di SignTool/a/v/FD** *HashAlgorithm* **/f** *certFileName* _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="f818d-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="f818d-148">*HashAlgorithm* deve corrispondere all'algoritmo hash usato per creare il BlockMap quando l'app è stata assemblata.</span><span class="sxs-lookup"><span data-stu-id="f818d-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="f818d-149">Con l'utilità di creazione pacchetti MakeAppx, l'algoritmo hash predefinito appx BlockMap è **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="f818d-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="f818d-150">Eseguire SignTool.exe specificando **SHA256** come algoritmo/FD (file digest):</span><span class="sxs-lookup"><span data-stu-id="f818d-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="f818d-151">**Signtool sign/a/v/FD SHA256/F** *certFileName* _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="f818d-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="f818d-152">Per altre informazioni su come firmare i pacchetti, vedere [come firmare un pacchetto dell'app con SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="f818d-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="f818d-153">Per estrarre i file da un pacchetto</span><span class="sxs-lookup"><span data-stu-id="f818d-153">To extract files from a package</span></span>

1.  <span data-ttu-id="f818d-154">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-154">Run this command:</span></span>

    <span data-ttu-id="f818d-155">**MakeAppx decomprimere/p** _file_**. appx/d** *\_ directory di output*</span><span class="sxs-lookup"><span data-stu-id="f818d-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="f818d-156">Il pacchetto decompresso ha la stessa struttura del pacchetto installato.</span><span class="sxs-lookup"><span data-stu-id="f818d-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="f818d-157">Per creare un bundle di pacchetti usando una struttura di directory</span><span class="sxs-lookup"><span data-stu-id="f818d-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="f818d-158">Viene usato il comando **bundle** per creare un bundle dell'app in</span><span class="sxs-lookup"><span data-stu-id="f818d-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="f818d-159">aggiungendo tutti i pacchetti da <content directory> (incluse le sottocartelle).</span><span class="sxs-lookup"><span data-stu-id="f818d-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="f818d-160">Se <content directory> contiene un manifesto del bundle, AppxBundleManifest.xml, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f818d-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="f818d-161">Inserire tutti i pacchetti in un'unica struttura di directory, creando sottodirectory nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="f818d-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="f818d-162">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-162">Run this command:</span></span>

    <span data-ttu-id="f818d-163">**MakeAppx bundle/d** *input \_ DirectoryPath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="f818d-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="f818d-164">Per creare un bundle di pacchetti usando un file di mapping</span><span class="sxs-lookup"><span data-stu-id="f818d-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="f818d-165">Viene usato il comando **bundle** per creare un bundle dell'app in</span><span class="sxs-lookup"><span data-stu-id="f818d-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="f818d-166">aggiungendo tutti i pacchetti da un elenco di pacchetti in <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="f818d-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="f818d-167">Se <mapping file> contiene un manifesto del bundle, AppxBundleManifest.xml, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f818d-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="f818d-168">Creare un oggetto <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="f818d-168">Create a <mapping file>.</span></span> <span data-ttu-id="f818d-169">La prima riga contiene i **\[ file \]** di stringa e le righe che seguono specificano i pacchetti da aggiungere al bundle.</span><span class="sxs-lookup"><span data-stu-id="f818d-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="f818d-170">Ogni pacchetto è descritto da una coppia di percorsi tra virgolette, separate da spazi o tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="f818d-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="f818d-171">La coppia di percorsi rappresenta l'origine (su disco) e la destinazione (in bundle) del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="f818d-172">Tutti i nomi dei pacchetti di destinazione devono avere l'estensione appx.</span><span class="sxs-lookup"><span data-stu-id="f818d-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="f818d-173">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-173">Run this command:</span></span>

    <span data-ttu-id="f818d-174">**MakeAppx bundle/f** *mapping \_ filePath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="f818d-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="f818d-175">Per estrarre i pacchetti da un bundle</span><span class="sxs-lookup"><span data-stu-id="f818d-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="f818d-176">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-176">Run this command:</span></span>

    <span data-ttu-id="f818d-177">**MakeAppx Unbundle/p** _\_ nome bundle_**. appxbundle/d** *\_ directory di output*</span><span class="sxs-lookup"><span data-stu-id="f818d-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="f818d-178">Il bundle decompresso ha la stessa struttura del bundle del pacchetto installato.</span><span class="sxs-lookup"><span data-stu-id="f818d-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="f818d-179">Per crittografare un pacchetto con un file di chiave</span><span class="sxs-lookup"><span data-stu-id="f818d-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="f818d-180">Creazione di un file di chiave.</span><span class="sxs-lookup"><span data-stu-id="f818d-180">Create a key file.</span></span> <span data-ttu-id="f818d-181">I file di chiave devono iniziare con una riga contenente la stringa " \[ Keys \] " seguita da righe che descrivono le chiavi per la crittografia del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="f818d-182">Ogni chiave viene descritta da una coppia di stringhe racchiuse tra virgolette, separate da spazi o tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="f818d-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="f818d-183">La prima stringa rappresenta l'ID chiave e la seconda stringa rappresenta la chiave di crittografia in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="f818d-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="f818d-184">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-184">Run this command:</span></span>

    <span data-ttu-id="f818d-185">**MakeAppx.exe crittografare/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto crittografato_**. eappx/KF** _\_ nome file_**. txt**</span><span class="sxs-lookup"><span data-stu-id="f818d-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="f818d-186">Il pacchetto di input verrà crittografato nel pacchetto crittografato specificato utilizzando il file di chiave fornito.</span><span class="sxs-lookup"><span data-stu-id="f818d-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="f818d-187">Per crittografare un pacchetto con una chiave di test globale</span><span class="sxs-lookup"><span data-stu-id="f818d-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="f818d-188">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-188">Run this command:</span></span>

    <span data-ttu-id="f818d-189">**MakeAppx.exe crittografare/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto crittografato_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="f818d-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="f818d-190">Il pacchetto di input verrà crittografato nel pacchetto crittografato specificato usando la chiave di test globale.</span><span class="sxs-lookup"><span data-stu-id="f818d-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="f818d-191">Per decrittografare un pacchetto con un file di chiave</span><span class="sxs-lookup"><span data-stu-id="f818d-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="f818d-192">Creazione di un file di chiave.</span><span class="sxs-lookup"><span data-stu-id="f818d-192">Create a key file.</span></span> <span data-ttu-id="f818d-193">I file di chiave devono iniziare con una riga contenente la stringa " \[ Keys \] " seguita da righe che descrivono le chiavi per la crittografia del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="f818d-194">Ogni chiave viene descritta da una coppia di stringhe racchiuse tra virgolette, separate da spazi o tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="f818d-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="f818d-195">La prima stringa rappresenta l'ID chiave a 32 byte con codifica Base64 e la seconda stringa rappresenta la chiave di crittografia 32 byte con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="f818d-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="f818d-196">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-196">Run this command:</span></span>

    <span data-ttu-id="f818d-197">**MakeAppx.exe Decrypt/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto non crittografato_**. eappx/KF** _\_ nome file_**. txt**</span><span class="sxs-lookup"><span data-stu-id="f818d-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="f818d-198">Il pacchetto di input verrà decrittografato nel pacchetto non crittografato specificato utilizzando il file di chiave fornito.</span><span class="sxs-lookup"><span data-stu-id="f818d-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="f818d-199">Per decrittografare un pacchetto con una chiave di test globale</span><span class="sxs-lookup"><span data-stu-id="f818d-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="f818d-200">Eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-200">Run this command:</span></span>

    <span data-ttu-id="f818d-201">**MakeAppx.exe Decrypt/p** _\_ nome pacchetto_**. appx/EP** _\_ \_ nome pacchetto non crittografato_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="f818d-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="f818d-202">Il pacchetto di input verrà decrittografato nel pacchetto non crittografato specificato utilizzando la chiave di test globale.</span><span class="sxs-lookup"><span data-stu-id="f818d-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="f818d-203">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f818d-203">Usage</span></span>

<span data-ttu-id="f818d-204">L'argomento della riga di comando **/p** è sempre obbligatorio, con **/d**, **/f** o **/EP**.</span><span class="sxs-lookup"><span data-stu-id="f818d-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="f818d-205">Si noti che **/d**, **/f** e **/EP** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f818d-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="f818d-206">**\[ Opzioni \] MakeAppx Pack** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="f818d-207">**\[ Opzioni \] MakeAppx Pack** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="f818d-208">**MakeAppx Decomprimi \[ Opzioni \]** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="f818d-209">**\[ Opzioni \] bundle MakeAppx** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="f818d-210">**\[ Opzioni \] bundle MakeAppx** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="f818d-211">**MakeAppx Unbundle \[ Options \]** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="f818d-212">**\[ Opzioni \] di crittografia MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="f818d-213">**\[ Opzioni \] di decrittografia MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="f818d-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="f818d-214">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="f818d-214">Command-line Syntax</span></span>

<span data-ttu-id="f818d-215">Di seguito è illustrata la sintassi di utilizzo comune da riga di comando per MakeAppx.</span><span class="sxs-lookup"><span data-stu-id="f818d-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="f818d-216">**MakeAppx \[ pack \| unpack \| bundle \| Unbundle \| Encrypt \| Decrypt \]** \[ **/h** **/KF** **/KT** **/l** **/o** **/No** **/NV** **/v** **/PFN** **/?**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="f818d-217">**MakeAppx** comprime o decomprime i file in un pacchetto, aggrega o decomprime i pacchetti in un bundle oppure crittografa o decrittografa il pacchetto o il bundle dell'applicazione nella directory di input o nel file di mapping specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="f818d-218">Di seguito è riportato l'elenco dei parametri che si applicano a **MakeAppx Pack**, **MakeAppx decomprimete**, **MakeAppx bundle**, **MakeAppx Unbundle**, **MakeAppx Encrypt** o **MakeAppx Decrypt**.</span><span class="sxs-lookup"><span data-stu-id="f818d-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="f818d-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-220">Questa opzione viene utilizzata per i pacchetti localizzati.</span><span class="sxs-lookup"><span data-stu-id="f818d-220">This option is used for localized packages.</span></span> <span data-ttu-id="f818d-221">La convalida predefinita può comportare problemi se applicata ai pacchetti localizzati.</span><span class="sxs-lookup"><span data-stu-id="f818d-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="f818d-222">Questa opzione disattiva solo la convalida specifica, senza che sia necessario disabilitare la convalida.</span><span class="sxs-lookup"><span data-stu-id="f818d-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="f818d-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-224">Sovrascrivere il file di output se esistente.</span><span class="sxs-lookup"><span data-stu-id="f818d-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="f818d-225">Se non si specifica questa opzione o l'opzione **/No** , all'utente viene chiesto se desidera sovrascrivere il file.</span><span class="sxs-lookup"><span data-stu-id="f818d-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="f818d-226">Non è possibile usare questa opzione con **/No**.</span><span class="sxs-lookup"><span data-stu-id="f818d-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-227"><span id="_no"></span><span id="_NO"></span>**/No**</span><span class="sxs-lookup"><span data-stu-id="f818d-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-228">Impedisce la sovrascrittura del file di output, se presente.</span><span class="sxs-lookup"><span data-stu-id="f818d-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="f818d-229">Se non si specifica questa opzione o l'opzione **/o** , viene chiesto all'utente se desidera sovrascrivere il file.</span><span class="sxs-lookup"><span data-stu-id="f818d-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="f818d-230">Non è possibile usare questa opzione con **/o**.</span><span class="sxs-lookup"><span data-stu-id="f818d-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="f818d-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-232">Ignorare la convalida semantica.</span><span class="sxs-lookup"><span data-stu-id="f818d-232">Skip semantic validation.</span></span> <span data-ttu-id="f818d-233">Se non specifichi questa opzione, lo strumento esegue una convalida completa del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="f818d-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-235">Abilitare l'output di registrazione dettagliata alla console.</span><span class="sxs-lookup"><span data-stu-id="f818d-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="f818d-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-237">Visualizzare il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="f818d-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="f818d-238">**MakeAppx Pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx Unbundle**, **MakeAppx Encrypt** e **MakeAppx Decrypt** sono comandi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f818d-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="f818d-239">Ecco i parametri della riga di comando che si applicano in modo specifico a ogni comando:</span><span class="sxs-lookup"><span data-stu-id="f818d-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="f818d-240">**MakeAppx Pack** \[ **h**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="f818d-241">Crea un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** ( *algoritmo* )</span><span class="sxs-lookup"><span data-stu-id="f818d-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="f818d-243">Specifica l'algoritmo hash da usare per la creazione della mappa dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="f818d-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="f818d-244">Di seguito sono riportati i valori validi per *Algorithm*:</span><span class="sxs-lookup"><span data-stu-id="f818d-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="f818d-245">SHA256 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f818d-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="f818d-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="f818d-246">SHA384</span></span></dd> <dd><span data-ttu-id="f818d-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="f818d-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="f818d-248">Non è possibile usare questa opzione con il comando **unpack** .</span><span class="sxs-lookup"><span data-stu-id="f818d-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="f818d-249">**Decompressione MakeAppx** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="f818d-250">Estrae tutti i file dal pacchetto specificato nella directory di output indicata.</span><span class="sxs-lookup"><span data-stu-id="f818d-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="f818d-251">L'output ha la stessa struttura di directory del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="f818d-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-253">Specifica una directory denominata con il nome completo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="f818d-254">Questa directory viene creata nel percorso di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="f818d-255">Non è possibile usare questa opzione con il comando **Pack** .</span><span class="sxs-lookup"><span data-stu-id="f818d-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="f818d-256">**MakeAppx Unbundle** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="f818d-257">Decomprime tutti i pacchetti in una sottodirectory nel percorso di output specificato, con il nome completo del bundle.</span><span class="sxs-lookup"><span data-stu-id="f818d-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="f818d-258">L'output ha la stessa struttura di directory del bundle di pacchetti installato.</span><span class="sxs-lookup"><span data-stu-id="f818d-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="f818d-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-260">Specifica una directory denominata con il nome completo del bundle del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f818d-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="f818d-261">Questa directory viene creata nel percorso di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="f818d-262">Non è possibile usare questa opzione con il comando **bundle** .</span><span class="sxs-lookup"><span data-stu-id="f818d-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="f818d-263">**Crittografia MakeAppx** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="f818d-264">Crea un pacchetto dell'app crittografato dal pacchetto dell'app di input specificato nel pacchetto di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="f818d-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="f818d-266">Esegue la crittografia del pacchetto o del bundle usando la chiave dal file di chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="f818d-267">Non è possibile usare questa opzione con **KT**.</span><span class="sxs-lookup"><span data-stu-id="f818d-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="f818d-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-269">Crittografa il pacchetto o il bundle usando la chiave di test globale.</span><span class="sxs-lookup"><span data-stu-id="f818d-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="f818d-270">Non è possibile usare questa opzione con **KF**.</span><span class="sxs-lookup"><span data-stu-id="f818d-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="f818d-271">**Decrittografia MakeAppx** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="f818d-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="f818d-272">Crea un pacchetto dell'app non crittografato dal pacchetto dell'app di input specificato nel pacchetto di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="f818d-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="f818d-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="f818d-274">Decrittografa il pacchetto o il bundle usando la chiave dal file di chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="f818d-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="f818d-275">Non è possibile usare questa opzione con **KT**.</span><span class="sxs-lookup"><span data-stu-id="f818d-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="f818d-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="f818d-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="f818d-277">Decrittografa il pacchetto o il bundle usando la chiave di test globale.</span><span class="sxs-lookup"><span data-stu-id="f818d-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="f818d-278">Non è possibile usare questa opzione con **KF**.</span><span class="sxs-lookup"><span data-stu-id="f818d-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="f818d-279">Convalida semantica eseguita da MakeAppx</span><span class="sxs-lookup"><span data-stu-id="f818d-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="f818d-280">MakeAppx esegue una convalida semantica limitata progettata per intercettare gli errori di distribuzione più comuni e garantire la validità del pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="f818d-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="f818d-281">La convalida assicura che:</span><span class="sxs-lookup"><span data-stu-id="f818d-281">This validation ensures that:</span></span>

-   <span data-ttu-id="f818d-282">Tutti i file a cui si fa riferimento nel manifesto del pacchetto siano inclusi nel pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="f818d-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="f818d-283">Un'applicazione non abbia due chiavi identiche.</span><span class="sxs-lookup"><span data-stu-id="f818d-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="f818d-284">Un'applicazione non esegue la registrazione per un protocollo non consentito da questo elenco: SMB, FILE, MS-WWA-WEB, MS-WWA.</span><span class="sxs-lookup"><span data-stu-id="f818d-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="f818d-285">Questa convalida semantica non è completa e non è garantito che i pacchetti compilati da MakeAppx siano installabili.</span><span class="sxs-lookup"><span data-stu-id="f818d-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 