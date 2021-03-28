---
description: Il sistema gestisce i colori nelle bitmap in modo diverso rispetto ai colori in penne, pennelli e testo.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Colore nelle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130818"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="6f42d-103">Colore nelle bitmap</span><span class="sxs-lookup"><span data-stu-id="6f42d-103">Color in Bitmaps</span></span>

<span data-ttu-id="6f42d-104">Il sistema gestisce i colori nelle bitmap in modo diverso rispetto ai colori in penne, pennelli e testo.</span><span class="sxs-lookup"><span data-stu-id="6f42d-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="6f42d-105">Le bitmap compatibili, create tramite la funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , sono specifiche del dispositivo e mantengono le informazioni sui colori in un formato dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f42d-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="6f42d-106">Non viene usato alcun valore di colore e i colori non sono soggetti ad approssimazioni e dithering.</span><span class="sxs-lookup"><span data-stu-id="6f42d-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="6f42d-107">Le bitmap indipendenti dal dispositivo conservano le informazioni sui colori come valori dei colori o indici della tavolozza dei colori.</span><span class="sxs-lookup"><span data-stu-id="6f42d-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="6f42d-108">Se vengono utilizzati i valori dei colori, i colori sono soggetti a approssimazione, ma non a rethering.</span><span class="sxs-lookup"><span data-stu-id="6f42d-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="6f42d-109">Gli indici della tavolozza dei colori possono essere usati solo con i dispositivi che supportano le tavolozze dei colori.</span><span class="sxs-lookup"><span data-stu-id="6f42d-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="6f42d-110">Anche se il sistema non approssimativo o i colori di dithering identificati da indici, il colore risultante può essere diverso da quello previsto, perché gli indici restituiscono risultati validi solo nel contesto della tavolozza dei colori che era corrente al momento della creazione della bitmap.</span><span class="sxs-lookup"><span data-stu-id="6f42d-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="6f42d-111">Se la tavolozza viene modificata, eseguire i colori nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="6f42d-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="6f42d-112">Per ulteriori informazioni sugli indici della tavolozza, vedere [default palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span><span class="sxs-lookup"><span data-stu-id="6f42d-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="6f42d-113">Oltre a fare riferimento alla tavolozza logica, un'applicazione può anche fare riferimento a un valore in una tabella dei colori DIB.</span><span class="sxs-lookup"><span data-stu-id="6f42d-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="6f42d-114">Per selezionare un colore in una tabella di colori DIB, chiamare [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="6f42d-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="6f42d-115">Si noti che questo è possibile solo per un contesto di dispositivo in cui è stata selezionata una DIB.</span><span class="sxs-lookup"><span data-stu-id="6f42d-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



