---
title: Configurazione di flussi arbitrari personalizzati
description: Configurazione di flussi arbitrari personalizzati
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flussi, configurazione di flussi arbitrari personalizzati
- codec, configurazione di flussi arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710162"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="8a3c2-105">Configurazione di flussi arbitrari personalizzati</span><span class="sxs-lookup"><span data-stu-id="8a3c2-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="8a3c2-106">Quando si usa un tipo di dati arbitrario personalizzato, è necessario creare un valore GUID che funga da identificatore principale del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="8a3c2-107">Quando il writer rileva un flusso in un profilo con un tipo principale non riconosce, presuppone che il flusso sia dati arbitrari personalizzati.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="8a3c2-108">Accetta gli esempi, li packetize e li combina con esempi dagli altri flussi del file senza verificare i dati in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="8a3c2-109">È anche possibile creare identificatori GUID di sottotipo personalizzati per definire sottocategorie dei dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="8a3c2-110">Il writer ignorerà completamente questi sottotipi, ma verrà mantenuto nella sezione di intestazione del file ASF, in modo che l'applicazione di lettura possa recuperarli e prendere decisioni in base a tali sottotipi.</span><span class="sxs-lookup"><span data-stu-id="8a3c2-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="8a3c2-111">Un flusso arbitrario richiede una velocità in bit e una finestra del buffer e deve avere una struttura di [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con i valori deselezionati, ad eccezione del tipo di supporto principale e del sottotipo (se ne viene usato uno).</span><span class="sxs-lookup"><span data-stu-id="8a3c2-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a3c2-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a3c2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a3c2-113">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="8a3c2-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="8a3c2-114">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="8a3c2-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="8a3c2-115">**Flussi di dati arbitrari personalizzati**</span><span class="sxs-lookup"><span data-stu-id="8a3c2-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




