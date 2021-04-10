---
title: Copia di dati da un file a un altro
description: Copia di dati da un file a un altro
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows Media Format SDK, copia di dati
- Formato di sistemi avanzati (ASF), copia di dati
- ASF (Advanced Systems Format), copia di dati
- flussi, copia di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955763"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="61925-107">Copia di dati da un file a un altro</span><span class="sxs-lookup"><span data-stu-id="61925-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="61925-108">Al livello più elementare, la copia di un flusso da un file ASF a un altro è piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="61925-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="61925-109">Tuttavia, esistono problemi da considerare quando si usano flussi da più file di input o quando si copiano i flussi che prima si decomprimeno e si ricodificano.</span><span class="sxs-lookup"><span data-stu-id="61925-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="61925-110">Le sezioni seguenti descrivono la copia di flussi.</span><span class="sxs-lookup"><span data-stu-id="61925-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="61925-111">Sezione</span><span class="sxs-lookup"><span data-stu-id="61925-111">Section</span></span>                                                                                              | <span data-ttu-id="61925-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="61925-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61925-113">Copia dei flussi senza decomprimere i dati</span><span class="sxs-lookup"><span data-stu-id="61925-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="61925-114">Viene descritto come copiare i flussi utilizzando esempi compressi per mantenere la qualità del contenuto.</span><span class="sxs-lookup"><span data-stu-id="61925-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="61925-115">Copia di flussi con esempi decompressi</span><span class="sxs-lookup"><span data-stu-id="61925-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="61925-116">Descrive le difficoltà di copia dei flussi utilizzando esempi decompressi.</span><span class="sxs-lookup"><span data-stu-id="61925-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="61925-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61925-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61925-118">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="61925-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="61925-119">**Oggetto configurazione del flusso**</span><span class="sxs-lookup"><span data-stu-id="61925-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="61925-120">**Oggetto lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="61925-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="61925-121">**Oggetto writer**</span><span class="sxs-lookup"><span data-stu-id="61925-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




