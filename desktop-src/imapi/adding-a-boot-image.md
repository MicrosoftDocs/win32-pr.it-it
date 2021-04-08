---
title: Aggiunta di un'immagine di avvio
description: Questo esempio si basa sull'esempio di masterizzazione di un'immagine del disco aggiungendo codice per includere un'immagine di avvio nella sezione di avvio del disco.
ms.assetid: b23cdbb9-ae0d-4261-965b-56abe865f323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce48537f32f1dc574eef174b26daaa5e2ebe255
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045341"
---
# <a name="adding-a-boot-image"></a><span data-ttu-id="458df-103">Aggiunta di un'immagine di avvio</span><span class="sxs-lookup"><span data-stu-id="458df-103">Adding a Boot Image</span></span>

<span data-ttu-id="458df-104">Questo esempio si basa sull'esempio di [masterizzazione di un'immagine del disco](burning-a-disc.md) aggiungendo codice per includere un'immagine di avvio nella sezione di avvio del disco. L'immagine di avvio si connette all'oggetto file system scritto su disco. Una volta collegato, il resto del processo di masterizzazione è identico a quello della procedura di masterizzazione di base.</span><span class="sxs-lookup"><span data-stu-id="458df-104">This example builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc. The bootable image connects to the file system object that is written to disc. Once attached, the rest of the burning process is identical to the basic burning procedure.</span></span> <span data-ttu-id="458df-105">L'immagine di avvio fornisce l'avvio del sistema tramite l'unità disco CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="458df-105">The boot image provides system startup using the CD or DVD disc drive.</span></span>

<span data-ttu-id="458df-106">L'esempio consente di impostare come hardcoded il percorso dell'immagine di avvio.</span><span class="sxs-lookup"><span data-stu-id="458df-106">The example hardcodes the path to the bootable image.</span></span> <span data-ttu-id="458df-107">Assicurarsi di modificare il percorso insieme ad altri valori hardcoded nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="458df-107">Be sure to change the path along with other hardcoded values as appropriate.</span></span>


```VB
' This script burns a boot image and data files to disc in a 
' single session  using files from a single directory tree. 

'Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF  = 4

WScript.Quit(Main)

Function Main
    Dim index                ' Index to recording drive.
    Dim recorder             ' Recorder object
    Dim path                 ' Directory of files to burn
    Dim stream               ' Data stream for burning device
    Dim bootFile             ' Path and filename of boot image
    
    index = 1                ' Second drive on the system
    path = "g:\BurnDir"      
    bootFile = "g:\BootImg\etfsboot.com"

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' -------- Adding Boot Image Code -----
    Dim bootOptions    
    WScript.Echo "Creating BootOptions"
    SET bootOptions = WScript.CreateObject("IMAPI2FS.BootOptions")
    bootOptions.Manufacturer = "Microsoft"
    bootOptions.PlatformId   = 0       ' x86 processor
    bootOptions.Emulation    = 0       ' EmulationType.EmulationNone
    
    ' Need a stream for the boot image file 
    Const adFileTypeBinary = 1
    DIM bootStream
    Set bootStream = CreateObject("ADODB.Stream")
    WScript.Echo "Creating IStream for file " + bootFile
    bootStream.Open
    bootStream.Type = adFileTypeBinary
    bootStream.LoadFromFile bootFile
    bootOptions.AssignBootImage(bootStream)
    
    ' Create disc file system image (ISO9660 in this example)
    Dim FSI
    SET FSI = WScript.CreateObject("IMAPI2FS.MsftFileSystemImage")
    FSI.ChooseImageDefaults(Recorder)
   
    ' Add the boot directory and its contents to the file system 
    FSI.BootImageOptions = bootOptions

    ' Add the content directory and files to the file system 
    FSI.root.AddTree path, FALSE

    Dim result
    Set result = FSI.CreateResultImage()
    stream = result.ImageStream

    ' Create and write stream to disc using the specified recorder.
    Dim dataWriter
    Set dataWriter = CreateObject("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    dataWriter.write(stream)
    WScript.Echo "----- Finished writing content -----"

    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="458df-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="458df-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="458df-109">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="458df-109">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="458df-110">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="458df-110">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="458df-111">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="458df-111">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="458df-112">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="458df-112">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 




