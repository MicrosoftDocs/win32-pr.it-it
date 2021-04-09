---
description: Tipi di codifica ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipi di codifica ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128007"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="c032a-103">Tipi di codifica ASF</span><span class="sxs-lookup"><span data-stu-id="c032a-103">ASF Encoding Types</span></span>

<span data-ttu-id="c032a-104">I metodi di codifica si concentrano tutti sul buffer utilizzato dal codificatore per gestire i dati di input non compressi.</span><span class="sxs-lookup"><span data-stu-id="c032a-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="c032a-105">Questo buffer è definito dalla velocità in bit del flusso, in bit al secondo e dalla finestra del buffer, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="c032a-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="c032a-106">Quando si esegue la codifica nei file ASF, i codificatori Windows Media rispettano i vincoli del buffer.</span><span class="sxs-lookup"><span data-stu-id="c032a-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="c032a-107">Per ulteriori informazioni sulla finestra buffer, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="c032a-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="c032a-108">Sapere come e quando usare ogni metodo può essere utile per creare contenuti compressi di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="c032a-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="c032a-109">La tabella seguente contiene collegamenti ad argomenti su ognuno dei metodi di codifica disponibili che un'applicazione può usare per codificare i dati multimediali in ASF.</span><span class="sxs-lookup"><span data-stu-id="c032a-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="c032a-110">Metodo di codifica</span><span class="sxs-lookup"><span data-stu-id="c032a-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="c032a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c032a-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c032a-112">Codifica della velocità in bit costante</span><span class="sxs-lookup"><span data-stu-id="c032a-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="c032a-113">Il codificatore comprime i dati a una velocità in bit specificata.</span><span class="sxs-lookup"><span data-stu-id="c032a-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="c032a-114">Codifica della velocità in bit della variabile basata sulla qualità</span><span class="sxs-lookup"><span data-stu-id="c032a-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="c032a-115">Il codificatore comprime i dati in un particolare valore di qualità, in modo che la qualità del supporto codificato sia coerente per tutta la sua durata, indipendentemente dai requisiti del buffer del flusso risultante.</span><span class="sxs-lookup"><span data-stu-id="c032a-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="c032a-116">Codifica della velocità in bit variabile non vincolata</span><span class="sxs-lookup"><span data-stu-id="c032a-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="c032a-117">Il codificatore comprime i dati alla massima qualità possibile mantenendo una velocità in bit specificata.</span><span class="sxs-lookup"><span data-stu-id="c032a-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="c032a-118">Questa modalità è detta anche codifica con velocità in bit variabile (VBR) a 2 passaggi.</span><span class="sxs-lookup"><span data-stu-id="c032a-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="c032a-119">Codifica della velocità in bit a variabili con vincoli di picco</span><span class="sxs-lookup"><span data-stu-id="c032a-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="c032a-120">Il codificatore comprime i dati in base a una velocità in bit specificata mantenendo i valori del buffer nella finestra del buffer massima specificata e nella velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="c032a-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="c032a-121">Questa modalità viene chiamata anche 2-pass di picco VBR.</span><span class="sxs-lookup"><span data-stu-id="c032a-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="c032a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c032a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c032a-123">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c032a-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c032a-124">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="c032a-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



