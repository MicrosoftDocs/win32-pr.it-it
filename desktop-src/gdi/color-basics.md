---
description: Le funzionalità relative ai colori dei dispositivi, ad esempio le visualizzazioni e le stampanti, possono variare da monocromatico a migliaia di colori.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Nozioni di base sui colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226705"
---
# <a name="color-basics"></a><span data-ttu-id="d329b-103">Nozioni di base sui colori</span><span class="sxs-lookup"><span data-stu-id="d329b-103">Color Basics</span></span>

<span data-ttu-id="d329b-104">Le funzionalità relative ai colori dei dispositivi, ad esempio le visualizzazioni e le stampanti, possono variare da monocromatico a migliaia di colori.</span><span class="sxs-lookup"><span data-stu-id="d329b-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="d329b-105">Poiché un'applicazione potrebbe avere la necessità di generare l'output per i dispositivi in tutto questo intervallo, è consigliabile prepararsi a gestire le diverse funzionalità di colore.</span><span class="sxs-lookup"><span data-stu-id="d329b-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="d329b-106">Un'applicazione può individuare il numero di colori disponibili per un determinato dispositivo usando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare il valore NUMCOLORS.</span><span class="sxs-lookup"><span data-stu-id="d329b-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="d329b-107">Questo valore specifica il numero di colori disponibili per l'utilizzo da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d329b-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="d329b-108">In genere, questo conteggio corrisponde a una proprietà fisica del dispositivo di output, ad esempio il numero di inchiostri nella stampante o il numero di segnali di colore distinti che l'adattatore di visualizzazione può trasmettere al monitor.</span><span class="sxs-lookup"><span data-stu-id="d329b-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="d329b-109">Sebbene il valore NUMCOLORS specifichi il numero di colori, non identifica i colori disponibili.</span><span class="sxs-lookup"><span data-stu-id="d329b-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="d329b-110">Un'applicazione è in grado di individuare i colori disponibili enumerando tutte le penne con il \_ tipo a tinta unita PS.</span><span class="sxs-lookup"><span data-stu-id="d329b-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="d329b-111">Poiché il driver di dispositivo che supporta un determinato dispositivo ha in genere una gamma completa di penne solide e perché il sistema richiede che le penne solide abbiano solo colori che possono essere generati dal dispositivo, l'enumerazione di tali penne è spesso equivalente all'enumerazione dei colori.</span><span class="sxs-lookup"><span data-stu-id="d329b-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="d329b-112">Un'applicazione può enumerare le penne usando la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .</span><span class="sxs-lookup"><span data-stu-id="d329b-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="d329b-113">Per un esempio di codice, vedere [enumerazione dei colori](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="d329b-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="d329b-114">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="d329b-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d329b-115">Valori dei colori</span><span class="sxs-lookup"><span data-stu-id="d329b-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="d329b-116">Approssimazioni di colori e dithering</span><span class="sxs-lookup"><span data-stu-id="d329b-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="d329b-117">Colore nelle bitmap</span><span class="sxs-lookup"><span data-stu-id="d329b-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="d329b-118">Combinazione di colori</span><span class="sxs-lookup"><span data-stu-id="d329b-118">Color Mixing</span></span>](color-mixing.md)

 

 



