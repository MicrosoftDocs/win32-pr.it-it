---
title: Ottenere informazioni sui compressori e i decompressori
description: Ottenere informazioni sui compressori e i decompressori
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Gestione compressione video (VCM), recupero di informazioni sui commediatori
- VCM (Video Compression Manager), recupero di informazioni sui commediatori
- ICGetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955515"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="4b991-106">Ottenere informazioni sui compressori e i decompressori</span><span class="sxs-lookup"><span data-stu-id="4b991-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="4b991-107">Per ottenere informazioni generali su un compressore o un decompressore, l'applicazione può usare la funzione [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) .</span><span class="sxs-lookup"><span data-stu-id="4b991-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="4b991-108">Questa funzione riempie una struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con le informazioni sul compressore o il decompressore.</span><span class="sxs-lookup"><span data-stu-id="4b991-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="4b991-109">L'applicazione deve allocare la memoria per la struttura **ICINFO** e passarvi un puntatore in **ICGetInfo**.</span><span class="sxs-lookup"><span data-stu-id="4b991-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="4b991-110">A meno che l'applicazione non cerchi un compressore o un decompressore particolare, i flag nella struttura **ICINFO** forniscono le informazioni più utili sulle funzionalità di un compressore o di un decompressore.</span><span class="sxs-lookup"><span data-stu-id="4b991-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="4b991-111">Per ottenere la frequenza dei fotogrammi chiave predefinita e il valore di qualità predefinito di un compressore o di un decompressore, l'applicazione può inviare i messaggi [**MCI \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usare le macro [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).</span><span class="sxs-lookup"><span data-stu-id="4b991-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="4b991-112">Per determinare il formato di visualizzazione migliore di un compressore o di un decompressore, l'applicazione può usare la funzione [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .</span><span class="sxs-lookup"><span data-stu-id="4b991-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="4b991-113">Per determinare se un compressore o un decompressore può visualizzare una finestra di dialogo informazioni su, inviare il messaggio [**ICM \_ About**](icm-about.md) (usare la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ).</span><span class="sxs-lookup"><span data-stu-id="4b991-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="4b991-114">È anche possibile visualizzare la finestra di dialogo informazioni su di un commutatore o un decompressore inviando il \_ messaggio ICM about e modificando il valore del parametro *wParam* (o usando la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).</span><span class="sxs-lookup"><span data-stu-id="4b991-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




