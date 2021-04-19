---
description: Voci generali del registro di sistema
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Voci generali del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314473"
---
# <a name="general-registry-entries"></a><span data-ttu-id="726dc-103">Voci generali del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="726dc-103">General Registry Entries</span></span>


<span data-ttu-id="726dc-104">Le seguenti voci del registro di sistema devono essere effettuate separatamente per il decodificatore e il codificatore:</span><span class="sxs-lookup"><span data-stu-id="726dc-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="726dc-105">Sono necessarie le voci FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions e formats.</span><span class="sxs-lookup"><span data-stu-id="726dc-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="726dc-106">Tutte le altre sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="726dc-106">All of the others are optional.</span></span>

<span data-ttu-id="726dc-107">Si noti che le voci DeviceManufacturer e DeviceModels sono specifiche dei codec non elaborati e fanno riferimento al produttore della fotocamera e ai modelli di fotocamera a cui è applicabile il codec.</span><span class="sxs-lookup"><span data-stu-id="726dc-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="726dc-108">La versione delle specifiche è la versione della specifica del formato di immagine con cui è conforme il codec.</span><span class="sxs-lookup"><span data-stu-id="726dc-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="726dc-109">La voce formats specifica i formati di pixel supportati dal codec.</span><span class="sxs-lookup"><span data-stu-id="726dc-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="726dc-110">Un codec può supportare più di un formato pixel.</span><span class="sxs-lookup"><span data-stu-id="726dc-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="726dc-111">In tal caso, immettere più chiavi in HKEY \_ classi \_ radice \\ CLSID \\ {codificatore/decodificatore CLSID} \\ formati.</span><span class="sxs-lookup"><span data-stu-id="726dc-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="726dc-112">ArbitrationPriority</span><span class="sxs-lookup"><span data-stu-id="726dc-112">ArbitrationPriority</span></span>

<span data-ttu-id="726dc-113">A partire da Windows 8, ArbitrationPriority è una nuova voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="726dc-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="726dc-114">I valori validi sono compresi tra 0 e 10.</span><span class="sxs-lookup"><span data-stu-id="726dc-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="726dc-115">Quando la chiave ArbitrationPriority è presente, il valore di questa chiave indicherà a WIC di classificare in ordine di priorità il codec associato dietro qualsiasi altro codec con un valore ArbitrationPriority più basso.</span><span class="sxs-lookup"><span data-stu-id="726dc-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="726dc-116">Questa valutazione si verifica prima che venga eseguito l'arbitraggio di codec WIC esistente e garantisce che il codec associato venga classificato in ordine di priorità sotto qualsiasi codec in competizione, anche se è più idoneo.</span><span class="sxs-lookup"><span data-stu-id="726dc-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="726dc-117">Qualsiasi codec che non dispone di un valore ArbitrationPriority esplicito definito nel registro di sistema avrà come valore predefinito la priorità 0.</span><span class="sxs-lookup"><span data-stu-id="726dc-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="726dc-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="726dc-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="726dc-119">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="726dc-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="726dc-120">Installazione e registrazione di CODEC</span><span class="sxs-lookup"><span data-stu-id="726dc-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="726dc-121">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="726dc-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="726dc-122">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="726dc-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="726dc-123">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="726dc-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="726dc-124">**Funzionamento del componente Windows Imaging: individuazione e arbitraggio dei codec**</span><span class="sxs-lookup"><span data-stu-id="726dc-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



