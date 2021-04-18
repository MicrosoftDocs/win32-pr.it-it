---
description: Viene illustrato come utilizzare le interfacce VSS per creare un provider hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Strumento VssSampleProvider ed esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307140"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="32ca9-103">Strumento VssSampleProvider ed esempio</span><span class="sxs-lookup"><span data-stu-id="32ca9-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="32ca9-104">Viene illustrato come utilizzare le [interfacce](volume-shadow-copy-api-interfaces.md) VSS per creare un provider hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="32ca9-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="32ca9-105">Lo strumento e l'esempio VssSampleProvider sono inclusi nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="32ca9-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="32ca9-106">È possibile scaricare il Windows SDK da [Windows Software Development Kit (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span><span class="sxs-lookup"><span data-stu-id="32ca9-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="32ca9-107">Nell'installazione di Windows SDK lo strumento VssSampleProvider si trova in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="32ca9-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="32ca9-108">I provider hardware sono supportati solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="32ca9-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="32ca9-109">In un sistema operativo client Windows, è possibile compilare l'esempio VssSampleProvider, ma non è possibile registrarlo come provider hardware.</span><span class="sxs-lookup"><span data-stu-id="32ca9-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="32ca9-110">Lo strumento VssSampleProvider è costituito dai file seguenti:</span><span class="sxs-lookup"><span data-stu-id="32ca9-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="32ca9-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="32ca9-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="32ca9-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="32ca9-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="32ca9-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="32ca9-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="32ca9-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="32ca9-114">Vstorinterface.dll</span></span>

<span data-ttu-id="32ca9-115">L'esempio VssSampleProvider include gli script di installazione e disinstallazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="32ca9-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="32ca9-116">Install-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="32ca9-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="32ca9-117">Uninstall-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="32ca9-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="32ca9-118">Registra \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="32ca9-118">Register\_app.vbs</span></span>

<span data-ttu-id="32ca9-119">**Per installare e usare l'esempio VssSampleProvider**</span><span class="sxs-lookup"><span data-stu-id="32ca9-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="32ca9-120">Passare alla directory `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="32ca9-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="32ca9-121">Questa directory contiene virtualstoragevss.sys e vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="32ca9-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="32ca9-122">Aprire una finestra del prompt dei comandi nella directory specificata.</span><span class="sxs-lookup"><span data-stu-id="32ca9-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="32ca9-123">Per installare il driver di archiviazione virtuale, digitare il comando seguente nella finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="32ca9-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="32ca9-124">Per installare il provider di esempio VSS, nella finestra del prompt dei comandi digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="32ca9-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="32ca9-125">Per creare un LUN virtuale, eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="32ca9-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="32ca9-126">Nella finestra del prompt dei comandi digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="32ca9-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="32ca9-127">Questo comando crea un LUN virtuale il cui identificatore di archiviazione è il **provider HW di esempio VSS**.</span><span class="sxs-lookup"><span data-stu-id="32ca9-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="32ca9-128">Per creare LUN virtuali aggiuntivi, ripetere questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="32ca9-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="32ca9-129">Il provider di esempio VSS riconosce un LUN solo se il **provider HW di esempio VSS** fa parte dell'identificatore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32ca9-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="32ca9-130">Per ulteriori informazioni sull'identificatore di archiviazione, vedere il seguente post di Blog.</span><span class="sxs-lookup"><span data-stu-id="32ca9-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="32ca9-131">LUN-risincronizzazione con DiskShadow e archiviazione virtuale</span><span class="sxs-lookup"><span data-stu-id="32ca9-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="32ca9-132">Nella finestra del prompt dei comandi usare diskpart.exe per formattare il disco virtuale e assegnarvi una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="32ca9-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="32ca9-133">Ecco uno script di esempio da eseguire al prompt dei comandi Diskpart.</span><span class="sxs-lookup"><span data-stu-id="32ca9-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="32ca9-134">Per eseguire il provider di esempio, nella finestra del prompt dei comandi digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="32ca9-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="32ca9-135">*<drive>* rappresenta la lettera di unità del LUN virtuale.</span><span class="sxs-lookup"><span data-stu-id="32ca9-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="32ca9-136">Per disinstallare il provider di esempio VSS, nella finestra del prompt dei comandi digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="32ca9-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="32ca9-137">Per disinstallare il driver di archiviazione virtuale, digitare il comando seguente nella finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="32ca9-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



