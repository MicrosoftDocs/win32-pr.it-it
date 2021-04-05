---
description: Attributi del descrittore di flusso
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Attributi del descrittore di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753842"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="ecf45-103">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="ecf45-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="ecf45-104">Attributi del descrittore di flusso comuni</span><span class="sxs-lookup"><span data-stu-id="ecf45-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="ecf45-105">Gli attributi seguenti si applicano ai descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="ecf45-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="ecf45-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="ecf45-106">Attribute</span></span>                                                   | <span data-ttu-id="ecf45-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf45-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf45-108">**\_lingua MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="ecf45-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="ecf45-109">Specifica la lingua per un flusso.</span><span class="sxs-lookup"><span data-stu-id="ecf45-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="ecf45-110">MF \_ SD si \_ escludono a vicenda \_</span><span class="sxs-lookup"><span data-stu-id="ecf45-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="ecf45-111">Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="ecf45-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="ecf45-112">**MF \_ SD \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="ecf45-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="ecf45-113">Specifica se un flusso contiene contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="ecf45-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="ecf45-114">\_ \_ Nome flusso MF \_ SD</span><span class="sxs-lookup"><span data-stu-id="ecf45-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="ecf45-115">Contiene il nome di un flusso.</span><span class="sxs-lookup"><span data-stu-id="ecf45-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="ecf45-116">Attributi del descrittore di flusso ASF-Specific</span><span class="sxs-lookup"><span data-stu-id="ecf45-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="ecf45-117">Gli attributi seguenti si applicano ai descrittori di flusso per i file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="ecf45-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="ecf45-118">Attributo</span><span class="sxs-lookup"><span data-stu-id="ecf45-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="ecf45-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf45-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf45-120">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Avg \_ bufferSize**</span><span class="sxs-lookup"><span data-stu-id="ecf45-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="ecf45-121">Specifica la dimensione media del buffer necessaria per un flusso in un file ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="ecf45-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="ecf45-122">**\_velocità in \_ \_ \_ \_ bit dei dati media \_ di MF SD ASF EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="ecf45-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="ecf45-123">Specifica la velocità media dei bit di dati di un flusso in un file ASF, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ecf45-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="ecf45-124">**\_ \_ \_ \_ \_ indice ID lingua \_ MF SD ASF EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="ecf45-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="ecf45-125">Specifica la lingua utilizzata da un flusso in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="ecf45-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="ecf45-126">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ bufferSize**</span><span class="sxs-lookup"><span data-stu-id="ecf45-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="ecf45-127">Specifica la dimensione massima del buffer necessaria per un flusso in un file ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="ecf45-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="ecf45-128">**\_velocità in \_ \_ \_ \_ bit massima dei dati di EXTSTRMPROP \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="ecf45-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="ecf45-129">Specifica la velocità in bit massima dei dati di un flusso in un file ASF, in bit al secondo</span><span class="sxs-lookup"><span data-stu-id="ecf45-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="ecf45-130">**\_modello di \_ \_ conformità del \_ dispositivo di metadati \_ \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="ecf45-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="ecf45-131">Specifica il modello di conformità del dispositivo per un flusso in un file ASF, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ecf45-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="ecf45-132">**\_velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_**</span><span class="sxs-lookup"><span data-stu-id="ecf45-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="ecf45-133">Specifica la velocità in bit media di un flusso in un file ASF, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ecf45-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="ecf45-134">Attributi del descrittore del flusso di origine dei supporti SAMI</span><span class="sxs-lookup"><span data-stu-id="ecf45-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="ecf45-135">Il seguente attributo si applica al descrittore di flusso per l'origine dei supporti SAMI.</span><span class="sxs-lookup"><span data-stu-id="ecf45-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="ecf45-136">Attributo</span><span class="sxs-lookup"><span data-stu-id="ecf45-136">Attribute</span></span>                                                       | <span data-ttu-id="ecf45-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf45-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf45-138">**\_lingua MF SD \_ Sami \_**</span><span class="sxs-lookup"><span data-stu-id="ecf45-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="ecf45-139">Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso.</span><span class="sxs-lookup"><span data-stu-id="ecf45-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ecf45-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecf45-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecf45-141">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ecf45-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="ecf45-142">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecf45-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



