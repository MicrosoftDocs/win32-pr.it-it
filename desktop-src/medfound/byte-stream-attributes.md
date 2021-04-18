---
description: Attributi del flusso di byte
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Attributi del flusso di byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305511"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="ddc11-103">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="ddc11-103">Byte Stream Attributes</span></span>

<span data-ttu-id="ddc11-104">Gli attributi seguenti si applicano ad alcuni flussi di byte.</span><span class="sxs-lookup"><span data-stu-id="ddc11-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="ddc11-105">Per determinare se un flusso di byte supporta gli attributi, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ddc11-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="ddc11-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="ddc11-106">Attribute</span></span>                                                                                  | <span data-ttu-id="ddc11-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc11-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="ddc11-108">**\_tipo di \_ contenuto MF BYTESTREAM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc11-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="ddc11-109">Specifica il tipo MIME di un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ddc11-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="ddc11-110">**\_durata MF BYTESTREAM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc11-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="ddc11-111">Specifica la durata di un flusso di byte, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ddc11-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="ddc11-112">\_URI del file MF BYTESTREAM \_ IFO \_ \_</span><span class="sxs-lookup"><span data-stu-id="ddc11-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="ddc11-113">Specifica l'URL di un file IFO associato.</span><span class="sxs-lookup"><span data-stu-id="ddc11-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="ddc11-114">**\_ora dell' \_ Ultima \_ modifica MF BYTESTREAM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc11-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="ddc11-115">Specifica la data dell'Ultima modifica di un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ddc11-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="ddc11-116">**\_nome dell' \_ origine MF BYTESTREAM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc11-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="ddc11-117">Specifica l'URL originale per un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ddc11-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="ddc11-118">Gli attributi seguenti si applicano ai gestori del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ddc11-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="ddc11-119">Attributo</span><span class="sxs-lookup"><span data-stu-id="ddc11-119">Attribute</span></span>                                                                                    | <span data-ttu-id="ddc11-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc11-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddc11-121">MF \_ BYTESTREAMHANDLER \_ accetta \_ la \_ scrittura condivisa</span><span class="sxs-lookup"><span data-stu-id="ddc11-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="ddc11-122">Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread</span><span class="sxs-lookup"><span data-stu-id="ddc11-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ddc11-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddc11-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddc11-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="ddc11-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="ddc11-125">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ddc11-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



