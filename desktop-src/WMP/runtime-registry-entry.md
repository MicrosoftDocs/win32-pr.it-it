---
title: Voce del registro di sistema runtime
description: Voce del registro di sistema runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, voci del registro di sistema di runtime
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci di runtime
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- voci del registro di sistema di runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044959"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="430b0-111">Voce del registro di sistema runtime</span><span class="sxs-lookup"><span data-stu-id="430b0-111">Runtime Registry Entry</span></span>

<span data-ttu-id="430b0-112">Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="430b0-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="430b0-113">La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="430b0-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="430b0-114">Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce di **Runtime** .</span><span class="sxs-lookup"><span data-stu-id="430b0-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="430b0-115">La voce **Runtime** specifica la tecnologia sottostante che Windows Media Player può utilizzare per riprodurre o convertire file multimediali digitali con estensione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="430b0-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="430b0-116">La voce **Runtime** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="430b0-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="430b0-117">**Nome**</span><span class="sxs-lookup"><span data-stu-id="430b0-117">**Name**</span></span> | <span data-ttu-id="430b0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="430b0-118">**Type**</span></span>       | <span data-ttu-id="430b0-119">**Valore**</span><span class="sxs-lookup"><span data-stu-id="430b0-119">**Value**</span></span>                                                     |
| <span data-ttu-id="430b0-120">Runtime</span><span class="sxs-lookup"><span data-stu-id="430b0-120">Runtime</span></span>  | <span data-ttu-id="430b0-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="430b0-121">**REG\_DWORD**</span></span> | <span data-ttu-id="430b0-122">Numero intero positivo che identifica la tecnologia sottostante.</span><span class="sxs-lookup"><span data-stu-id="430b0-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="430b0-123">Il valore della voce di **Runtime** deve essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="430b0-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="430b0-124">**Valore (decimale)**</span><span class="sxs-lookup"><span data-stu-id="430b0-124">**Value (decimal)**</span></span> | <span data-ttu-id="430b0-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="430b0-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="430b0-126">6</span><span class="sxs-lookup"><span data-stu-id="430b0-126">6</span></span>                   | <span data-ttu-id="430b0-127">Eseguire il rendering usando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="430b0-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="430b0-128">7</span><span class="sxs-lookup"><span data-stu-id="430b0-128">7</span></span>                   | <span data-ttu-id="430b0-129">Eseguire il rendering con Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="430b0-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="430b0-130">13</span><span class="sxs-lookup"><span data-stu-id="430b0-130">13</span></span>                  | <span data-ttu-id="430b0-131">Converte il file utilizzando il plug-in di conversione specificato.</span><span class="sxs-lookup"><span data-stu-id="430b0-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="430b0-132">Richiede Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="430b0-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="430b0-133">I valori 6 e 7 della voce del registro di sistema di **Runtime** sono supportati dalla serie Windows Media Player 9 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="430b0-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="430b0-134">Il valore 13 è supportato da Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="430b0-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="430b0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="430b0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="430b0-136">**Sottochiave ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="430b0-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="430b0-137">**Impostazioni del registro di sistema estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="430b0-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




