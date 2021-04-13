---
title: Temporizzazione (Windows Multimedia)
description: Intervallo
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, temporizzazione
- DrawDibTime (funzione)
- DrawDib, debug
- debug di DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474861"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="57355-107">Temporizzazione (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="57355-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="57355-108">Come parte del debug di un'applicazione, è possibile ottenere informazioni sul tempo necessario per completare le operazioni DrawDib ripetitive.</span><span class="sxs-lookup"><span data-stu-id="57355-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="57355-109">La funzione [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) restituisce informazioni sulla temporizzazione per le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57355-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="57355-110">Disegno di una bitmap</span><span class="sxs-lookup"><span data-stu-id="57355-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="57355-111">Decompressione di una bitmap</span><span class="sxs-lookup"><span data-stu-id="57355-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="57355-112">Retinatura di una bitmap</span><span class="sxs-lookup"><span data-stu-id="57355-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="57355-113">Estensione di una bitmap</span><span class="sxs-lookup"><span data-stu-id="57355-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="57355-114">Trasferimento di una bitmap tramite la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)</span><span class="sxs-lookup"><span data-stu-id="57355-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="57355-115">Trasferimento di una bitmap tramite la funzione [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)</span><span class="sxs-lookup"><span data-stu-id="57355-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="57355-116">Dopo il recupero di un set di valori, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) Reimposta il conteggio e il valore per ogni operazione.</span><span class="sxs-lookup"><span data-stu-id="57355-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="57355-117">La funzione [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) è disponibile solo nella versione di debug delle funzioni DrawDib.</span><span class="sxs-lookup"><span data-stu-id="57355-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57355-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57355-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57355-119">Rendering di immagini</span><span class="sxs-lookup"><span data-stu-id="57355-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
