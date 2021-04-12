---
title: Voce del registro di sistema FormatCode
description: Voce del registro di sistema FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Media Player di Windows, voci del registro di sistema FormatCode
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci FormatCode
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- Voci del registro di sistema FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104223406"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="1dcd8-111">Voce del registro di sistema FormatCode</span><span class="sxs-lookup"><span data-stu-id="1dcd8-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="1dcd8-112">Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="1dcd8-113">La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="1dcd8-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="1dcd8-114">Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce **FormatCode** .</span><span class="sxs-lookup"><span data-stu-id="1dcd8-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="1dcd8-115">La voce del registro di sistema **FormatCode** specifica il codice di formato MTP (Media Transport Protocol) per i file con estensione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="1dcd8-116">La voce del registro di sistema **FormatCode** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="1dcd8-117">Nome</span><span class="sxs-lookup"><span data-stu-id="1dcd8-117">Name</span></span>       | <span data-ttu-id="1dcd8-118">Type</span><span class="sxs-lookup"><span data-stu-id="1dcd8-118">Type</span></span>           | <span data-ttu-id="1dcd8-119">valore</span><span class="sxs-lookup"><span data-stu-id="1dcd8-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="1dcd8-120">FormatCode</span><span class="sxs-lookup"><span data-stu-id="1dcd8-120">FormatCode</span></span> | <span data-ttu-id="1dcd8-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1dcd8-121">**REG\_DWORD**</span></span> | <span data-ttu-id="1dcd8-122">Intero positivo a 16 bit che identifica il formato del file.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="1dcd8-123">Quando l'utente tenta di copiare un file multimediale digitale con estensione di file personalizzata in un dispositivo portatile, Windows Media Player Cerca nel registro di sistema di trovare un codice di formato associato all'estensione del nome file personalizzata.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="1dcd8-124">Se Windows Media Player trova un codice di formato, USA MTP per determinare se il dispositivo supporta il formato di file personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="1dcd8-125">Se il dispositivo supporta il formato, il file multimediale viene copiato nel dispositivo senza essere transcodificato.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="1dcd8-126">Un dispositivo che supporta MTP può fornire Media Player Windows con un set di dati DeviceInfo, che contiene, tra le altre cose, un elenco di codici di formato supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="1dcd8-127">Se è in corso lo sviluppo di un formato di file personalizzato, è possibile richiedere un codice di formato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1dcd8-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="1dcd8-128">Per informazioni su come richiedere un codice di formato, vedere Microsoft Media Transport Protocol Porting Kit, disponibile nel [centro per sviluppatori Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="1dcd8-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dcd8-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dcd8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dcd8-130">**Impostazioni del registro di sistema estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="1dcd8-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




