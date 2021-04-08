---
title: Nozioni di base compressore e decompressore
description: Nozioni di base compressore e decompressore
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Gestione compressione video (VCM), apertura di compressatori
- VCM (Gestione compressione video), apertura di comprimeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856053"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="f15b2-105">Nozioni di base compressore e decompressore</span><span class="sxs-lookup"><span data-stu-id="f15b2-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="f15b2-106">Per aprire e individuare un compressore, è possibile usare le funzioni [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) .</span><span class="sxs-lookup"><span data-stu-id="f15b2-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="f15b2-107">È possibile usare **ICLocate** per trovare un compressore di un tipo specifico e per ottenerne un handle da usare in altre funzioni di VCM.</span><span class="sxs-lookup"><span data-stu-id="f15b2-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="f15b2-108">Per aprire un compressore, è possibile usare **ICOpen**.</span><span class="sxs-lookup"><span data-stu-id="f15b2-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="f15b2-109">L'applicazione usa l'handle restituito da questa funzione per identificare il compressore aperto quando usa altre funzioni VCM.</span><span class="sxs-lookup"><span data-stu-id="f15b2-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="f15b2-110">Per aprire e individuare un decompressore, le applicazioni possono usare le macro [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) .</span><span class="sxs-lookup"><span data-stu-id="f15b2-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="f15b2-111">Queste macro usano **ICLocate** per Operation.</span><span class="sxs-lookup"><span data-stu-id="f15b2-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="f15b2-112">Quando l'applicazione ha terminato di usare un comprimetore o un decompressore, è necessario chiuderlo per liberare le risorse usate per la compressione o la decompressione.</span><span class="sxs-lookup"><span data-stu-id="f15b2-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="f15b2-113">L'applicazione può usare la funzione [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) per chiudere il compressore o il decompressore.</span><span class="sxs-lookup"><span data-stu-id="f15b2-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="f15b2-114">Inoltre, l'applicazione può enumerare i compressori o i decompressori in un sistema tramite la funzione [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="f15b2-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="f15b2-115">L'intestazione del flusso in un file AVI contiene informazioni sul tipo di flusso e sul gestore specifico per tale flusso.</span><span class="sxs-lookup"><span data-stu-id="f15b2-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="f15b2-116">All'interno dell'intestazione del flusso, i membri **fccType** e **fccHandler** identificano il tipo di flusso e il gestore di flusso specificato per il flusso.</span><span class="sxs-lookup"><span data-stu-id="f15b2-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




