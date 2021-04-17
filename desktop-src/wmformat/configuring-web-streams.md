---
title: Configurazione di flussi Web
description: Configurazione di flussi Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flussi, configurazione di flussi Web
- codec, configurazione di flussi Web
- Flussi Web, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331943"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="8d290-106">Configurazione di flussi Web</span><span class="sxs-lookup"><span data-stu-id="8d290-106">Configuring Web Streams</span></span>

<span data-ttu-id="8d290-107">I flussi Web sono un tipo specializzato di flusso di trasferimento di file usato per recapitare i file associati a un sito Web in un singolo flusso.</span><span class="sxs-lookup"><span data-stu-id="8d290-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="8d290-108">La configurazione del flusso Web è riepilogata nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d290-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="8d290-109">Impostazione</span><span class="sxs-lookup"><span data-stu-id="8d290-109">Setting</span></span>                                            | <span data-ttu-id="8d290-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d290-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8d290-111">**\_Tipo di supporto WM \_ . majortype**</span><span class="sxs-lookup"><span data-stu-id="8d290-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="8d290-112">Impostare su WMMEDIATYPE \_ filetransfer.</span><span class="sxs-lookup"><span data-stu-id="8d290-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="8d290-113">**\_Tipo di supporto WM \_ . sottotipo**</span><span class="sxs-lookup"><span data-stu-id="8d290-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="8d290-114">Impostare su WMMEDIASUBTYPE \_ webstream.</span><span class="sxs-lookup"><span data-stu-id="8d290-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="8d290-115">**\_Tipo di supporto WM \_ . bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="8d290-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="8d290-116">Impostare su false.</span><span class="sxs-lookup"><span data-stu-id="8d290-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="8d290-117">**\_Tipo di supporto WM \_ . bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="8d290-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="8d290-118">Impostare su true.</span><span class="sxs-lookup"><span data-stu-id="8d290-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="8d290-119">**\_Tipo di supporto WM \_ . lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="8d290-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="8d290-120">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="8d290-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="8d290-121">**\_Tipo di supporto WM \_ . formatType**</span><span class="sxs-lookup"><span data-stu-id="8d290-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="8d290-122">Impostare su WMFORMAT \_ webstream.</span><span class="sxs-lookup"><span data-stu-id="8d290-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="8d290-123">**\_Tipo di supporto WM \_ . punk**</span><span class="sxs-lookup"><span data-stu-id="8d290-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="8d290-124">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="8d290-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="8d290-125">**\_Tipo di supporto WM \_ . cbFormat**</span><span class="sxs-lookup"><span data-stu-id="8d290-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="8d290-126">Impostare su `sizeof(WMT_WEBSTREAM_FORMAT)`.</span><span class="sxs-lookup"><span data-stu-id="8d290-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="8d290-127">**\_Tipo di supporto WM \_ . pbFormat**</span><span class="sxs-lookup"><span data-stu-id="8d290-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="8d290-128">Impostare sull'indirizzo di una struttura del **\_ \_ formato webstream WMT** correttamente configurata.</span><span class="sxs-lookup"><span data-stu-id="8d290-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="8d290-129">**\_Formato WEBSTREAM WMT \_ . cbSampleHeaderFixedData**</span><span class="sxs-lookup"><span data-stu-id="8d290-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="8d290-130">Impostare su `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span><span class="sxs-lookup"><span data-stu-id="8d290-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="8d290-131">**\_Formato WEBSTREAM WMT \_ . wVersion**</span><span class="sxs-lookup"><span data-stu-id="8d290-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="8d290-132">impostare su 1.</span><span class="sxs-lookup"><span data-stu-id="8d290-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="8d290-133">**\_Formato WEBSTREAM WMT \_ . wReserved**</span><span class="sxs-lookup"><span data-stu-id="8d290-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="8d290-134">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="8d290-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="8d290-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d290-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d290-136">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="8d290-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="8d290-137">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="8d290-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="8d290-138">**Flussi Web**</span><span class="sxs-lookup"><span data-stu-id="8d290-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




