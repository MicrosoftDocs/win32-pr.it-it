---
title: Funzionalità di codec
description: Funzionalità di codec
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Media Format SDK, funzionalità codec
- Windows Media Format SDK, funzionalità
- codec, funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221422"
---
# <a name="codec-features"></a><span data-ttu-id="27ea9-106">Funzionalità di codec</span><span class="sxs-lookup"><span data-stu-id="27ea9-106">Codec Features</span></span>

<span data-ttu-id="27ea9-107">Windows Media Format SDK viene fornito con diversi codec audio e video.</span><span class="sxs-lookup"><span data-stu-id="27ea9-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="27ea9-108">È possibile usare i codec forniti per comprimere e decomprimere il contenuto in base a una varietà di esigenze.</span><span class="sxs-lookup"><span data-stu-id="27ea9-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="27ea9-109">Il codec utilizzato dal writer per comprimere i dati viene specificato dalle informazioni di configurazione del flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="27ea9-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="27ea9-110">Le informazioni del profilo vengono quindi archiviate nell'intestazione del file creato dal writer.</span><span class="sxs-lookup"><span data-stu-id="27ea9-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="27ea9-111">Quindi, quando il file viene aperto dal lettore o dal lettore sincrono, le informazioni sul profilo nell'intestazione identificano il codec necessario per decomprimere i dati.</span><span class="sxs-lookup"><span data-stu-id="27ea9-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="27ea9-112">In questa sezione vengono descritte le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="27ea9-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="27ea9-113">Codec supportati</span><span class="sxs-lookup"><span data-stu-id="27ea9-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="27ea9-114">Codifica della velocità in bit costante (CBR)</span><span class="sxs-lookup"><span data-stu-id="27ea9-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="27ea9-115">Codifica della velocità in bit variabile (VBR)</span><span class="sxs-lookup"><span data-stu-id="27ea9-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="27ea9-116">Codifica a due passaggi</span><span class="sxs-lookup"><span data-stu-id="27ea9-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="27ea9-117">Supporto audio ad alta risoluzione</span><span class="sxs-lookup"><span data-stu-id="27ea9-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="27ea9-118">Audio a ritardo ridotto</span><span class="sxs-lookup"><span data-stu-id="27ea9-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="27ea9-119">Output audio S/PDIF</span><span class="sxs-lookup"><span data-stu-id="27ea9-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="27ea9-120">Immagine video</span><span class="sxs-lookup"><span data-stu-id="27ea9-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="27ea9-121">Modelli di conformità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="27ea9-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="27ea9-122">Impostazioni di complessità video</span><span class="sxs-lookup"><span data-stu-id="27ea9-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="27ea9-123">Interpolazione frame</span><span class="sxs-lookup"><span data-stu-id="27ea9-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="27ea9-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27ea9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ea9-125">**Funzionalità**</span><span class="sxs-lookup"><span data-stu-id="27ea9-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




