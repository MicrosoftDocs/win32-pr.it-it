---
title: Voce del Registro di sistema di runtime
description: Voce del Registro di sistema di runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player,voci del Registro di sistema di runtime
- Windows Media Player,estensioni di file
- Windows Media Player,registro
- registro, estensioni di file
- registro, voci di runtime
- registro, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione di file
- voci del Registro di sistema di runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424110"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="f33cd-111">Voce del Registro di sistema di runtime</span><span class="sxs-lookup"><span data-stu-id="f33cd-111">Runtime Registry Entry</span></span>

<span data-ttu-id="f33cd-112">Quando Windows Media Player rileva un'estensione di file personalizzata, cerca una sottochiave del Registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="f33cd-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="f33cd-113">La sottochiave è descritta in Impostazioni del Registro di [sistema dell'estensione file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f33cd-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="f33cd-114">Una delle voci del Registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la **voce Runtime.**</span><span class="sxs-lookup"><span data-stu-id="f33cd-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="f33cd-115">La **voce Runtime** specifica la tecnologia sottostante che Windows Media Player possibile usare per riprodurre o convertire file multimediali digitali con estensione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f33cd-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="f33cd-116">La **voce Runtime** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="f33cd-116">The **Runtime** entry has the following form.</span></span>



|   <span data-ttu-id="f33cd-117">Nome</span><span class="sxs-lookup"><span data-stu-id="f33cd-117">Name</span></span>   |   <span data-ttu-id="f33cd-118">Type</span><span class="sxs-lookup"><span data-stu-id="f33cd-118">Type</span></span>         |   <span data-ttu-id="f33cd-119">valore</span><span class="sxs-lookup"><span data-stu-id="f33cd-119">Value</span></span>                                                       |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="f33cd-120">Runtime</span><span class="sxs-lookup"><span data-stu-id="f33cd-120">Runtime</span></span>  | <span data-ttu-id="f33cd-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f33cd-121">**REG\_DWORD**</span></span> | <span data-ttu-id="f33cd-122">Intero positivo che identifica la tecnologia sottostante.</span><span class="sxs-lookup"><span data-stu-id="f33cd-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="f33cd-123">Il valore della voce **Runtime** deve essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="f33cd-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="f33cd-124">**Valore (decimale)**</span><span class="sxs-lookup"><span data-stu-id="f33cd-124">**Value (decimal)**</span></span> | <span data-ttu-id="f33cd-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f33cd-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33cd-126">6</span><span class="sxs-lookup"><span data-stu-id="f33cd-126">6</span></span>                   | <span data-ttu-id="f33cd-127">Eseguire il rendering con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f33cd-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="f33cd-128">7</span><span class="sxs-lookup"><span data-stu-id="f33cd-128">7</span></span>                   | <span data-ttu-id="f33cd-129">Eseguire il rendering con Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f33cd-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="f33cd-130">13</span><span class="sxs-lookup"><span data-stu-id="f33cd-130">13</span></span>                  | <span data-ttu-id="f33cd-131">Convertire il file usando il plug-in di conversione specificato.</span><span class="sxs-lookup"><span data-stu-id="f33cd-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="f33cd-132">Richiede Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f33cd-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="f33cd-133">I **valori 6** e 7 della voce del Registro di sistema Runtime sono supportati Windows Media Player serie 9 e successive.</span><span class="sxs-lookup"><span data-stu-id="f33cd-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="f33cd-134">Il valore 13 è supportato da Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f33cd-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f33cd-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f33cd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f33cd-136">**Sottochiave ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="f33cd-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="f33cd-137">**Impostazioni del Registro di sistema dell'estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="f33cd-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




