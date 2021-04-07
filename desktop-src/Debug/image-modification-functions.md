---
description: Le funzioni di modifica delle immagini consentono di modificare l'immagine eseguibile.
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Funzioni di modifica delle immagini ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747895"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="8f1ee-103">Funzioni di modifica delle immagini ImageHlp</span><span class="sxs-lookup"><span data-stu-id="8f1ee-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="8f1ee-104">Le funzioni di modifica delle immagini consentono di modificare l'immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="8f1ee-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="8f1ee-105">Sono usati principalmente dagli strumenti di sviluppo e dall'installazione di programmi.</span><span class="sxs-lookup"><span data-stu-id="8f1ee-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="8f1ee-106">Possono essere usati per associare un'immagine, per calcolare il checksum (importante per garantire l'integrità delle immagini), per modificare l'indirizzo di caricamento e per produrre i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="8f1ee-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="8f1ee-107">Di seguito sono riportate le funzioni di modifica delle immagini.</span><span class="sxs-lookup"><span data-stu-id="8f1ee-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="8f1ee-108">**Azione BindImage sul**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="8f1ee-109">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="8f1ee-110">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="8f1ee-111">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="8f1ee-112">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="8f1ee-113">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="8f1ee-114">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="8f1ee-115">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="8f1ee-116">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="8f1ee-117">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="8f1ee-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 



