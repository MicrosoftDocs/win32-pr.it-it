---
description: La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori dell'immagine esistente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinazione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130814"
---
# <a name="color-mixing"></a><span data-ttu-id="3073b-103">Combinazione di colori</span><span class="sxs-lookup"><span data-stu-id="3073b-103">Color Mixing</span></span>

<span data-ttu-id="3073b-104">La combinazione di colori consente a un'applicazione di creare nuovi colori combinando il colore della penna o del pennello con i colori dell'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="3073b-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="3073b-105">L'applicazione può scegliere di disegnare la penna o il colore del pennello così come è (disegno efficace di qualsiasi immagine esistente) o di combinare il colore con i colori già presenti.</span><span class="sxs-lookup"><span data-stu-id="3073b-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="3073b-106">La modalità di combinazione di primo piano, talvolta chiamata operazione raster binaria, determina il modo in cui questi colori vengono combinati.</span><span class="sxs-lookup"><span data-stu-id="3073b-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="3073b-107">Un'applicazione può unire i colori, mantenendo tutti i componenti di entrambi i colori; mascherare i colori, rimuovere o moderare i componenti che non sono comuni; o mascherano esclusivamente i colori, rimuovendo o moderando i componenti comuni.</span><span class="sxs-lookup"><span data-stu-id="3073b-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="3073b-108">Questa operazione di combinazione di base prevede diverse varianti.</span><span class="sxs-lookup"><span data-stu-id="3073b-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="3073b-109">La combinazione di colori è soggetta all'approssimazione del colore.</span><span class="sxs-lookup"><span data-stu-id="3073b-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="3073b-110">Se il risultato della combinazione di colori è un colore che il dispositivo non è in grado di generare, il sistema approssima il risultato, usando un colore che può generare.</span><span class="sxs-lookup"><span data-stu-id="3073b-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="3073b-111">Se un'applicazione combina colori diversi, i singoli colori utilizzati per creare il colore con rethereing vengono combinati e i risultati sono soggetti a approssimazione dei colori.</span><span class="sxs-lookup"><span data-stu-id="3073b-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="3073b-112">Un'applicazione imposta la modalità di combinazione di primo piano usando la funzione [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera la modalità corrente usando la funzione [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .</span><span class="sxs-lookup"><span data-stu-id="3073b-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="3073b-113">Sebbene sia disponibile una modalità di combinazione in background, questa modalità non controlla la combinazione di colori.</span><span class="sxs-lookup"><span data-stu-id="3073b-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="3073b-114">Specifica invece se usare un colore di sfondo quando si disegnano linee con stile, pennelli tratteggiati e testo.</span><span class="sxs-lookup"><span data-stu-id="3073b-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



