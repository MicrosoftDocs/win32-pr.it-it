---
title: Configurazione di flussi di testo
description: Configurazione di flussi di testo
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flussi, configurazione di flussi di testo
- codec, configurazione di flussi di testo
- flussi di testo, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471302"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="ea800-106">Configurazione di flussi di testo</span><span class="sxs-lookup"><span data-stu-id="ea800-106">Configuring Text Streams</span></span>

<span data-ttu-id="ea800-107">I flussi di testo sono essenzialmente uguali ai flussi arbitrari personalizzati.</span><span class="sxs-lookup"><span data-stu-id="ea800-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="ea800-108">Non sono presenti informazioni di configurazione associate a un flusso di testo per identificare il tipo di codifica del testo, pertanto l'oggetto writer non è in grado di verificare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="ea800-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="ea800-109">Per configurare un flusso di testo, è necessario assicurarsi che la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contenga un tipo di supporto principale del \_ testo WMMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="ea800-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="ea800-110">È inoltre necessario impostare una velocità in bit e una finestra del buffer per il flusso.</span><span class="sxs-lookup"><span data-stu-id="ea800-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea800-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea800-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea800-112">**Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="ea800-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="ea800-113">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="ea800-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="ea800-114">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="ea800-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="ea800-115">**Flussi di testo**</span><span class="sxs-lookup"><span data-stu-id="ea800-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




