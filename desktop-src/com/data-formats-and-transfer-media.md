---
title: Formati di dati e supporti di trasferimento
description: Formati di dati e supporti di trasferimento
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104047583"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="bd61b-103">Formati di dati e supporti di trasferimento</span><span class="sxs-lookup"><span data-stu-id="bd61b-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="bd61b-104">La maggior parte delle piattaforme, tra cui Windows, definisce un protocollo standard per il trasferimento dei dati tra le applicazioni, in base a un set di funzioni denominate Appunti.</span><span class="sxs-lookup"><span data-stu-id="bd61b-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="bd61b-105">Le applicazioni che usano queste funzioni possono condividere dati anche se i loro formati di dati nativi sono molto diversi.</span><span class="sxs-lookup"><span data-stu-id="bd61b-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="bd61b-106">In genere, questi appunti presentano due carenze significative che COM ha superato.</span><span class="sxs-lookup"><span data-stu-id="bd61b-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="bd61b-107">Per prima cosa, le descrizioni dei dati usano solo un identificatore di formato, ad esempio l'identificatore di formato degli Appunti a 16 bit per Windows, il che significa che gli Appunti possono descrivere solo la struttura dei propri dati, ovvero l'ordine dei bit.</span><span class="sxs-lookup"><span data-stu-id="bd61b-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="bd61b-108">Può segnalare, "Ho una bitmap" "o ho del testo", ma non è possibile specificare i dispositivi di destinazione per i quali i dati sono composti, le visualizzazioni o gli aspetti che possono fornire i dati o i supporti di archiviazione più adatti per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="bd61b-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="bd61b-109">Ad esempio, non può segnalare "Ho una stringa di testo archiviata nella memoria globale e formattata per la presentazione sullo schermo o su una stampante" oppure "Ho una bitmap di sketch di anteprima visualizzata per una stampante a matrice di punti dpi 100 e archiviata come file su disco".</span><span class="sxs-lookup"><span data-stu-id="bd61b-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="bd61b-110">In secondo luogo, tutti i trasferimenti di dati tramite gli appunti si verificano generalmente tramite la memoria globale.</span><span class="sxs-lookup"><span data-stu-id="bd61b-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="bd61b-111">L'uso della memoria globale è ragionevolmente efficiente per piccole quantità di dati, ma terribilmente inefficiente per grandi quantità, ad esempio un oggetto multimediale da 20 MB.</span><span class="sxs-lookup"><span data-stu-id="bd61b-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="bd61b-112">La memoria globale è lenta per un oggetto dati di grandi dimensioni, la cui dimensione richiede un notevole scambio nella memoria virtuale su disco.</span><span class="sxs-lookup"><span data-stu-id="bd61b-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="bd61b-113">Nei casi in cui i dati scambiati risiedono principalmente su disco, l'utilizzo forzato di questo collo di bottiglia della memoria virtuale è estremamente inefficiente.</span><span class="sxs-lookup"><span data-stu-id="bd61b-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="bd61b-114">Un modo migliore è ignorare completamente la memoria globale e trasferire semplicemente i dati direttamente sul disco.</span><span class="sxs-lookup"><span data-stu-id="bd61b-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="bd61b-115">Per risolvere questi problemi, COM fornisce due strutture di dati: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="bd61b-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="bd61b-116">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="bd61b-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="bd61b-117">Struttura FORMATETC</span><span class="sxs-lookup"><span data-stu-id="bd61b-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="bd61b-118">Struttura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="bd61b-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="bd61b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd61b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd61b-120">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="bd61b-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




