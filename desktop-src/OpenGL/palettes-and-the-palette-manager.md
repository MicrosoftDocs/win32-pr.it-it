---
title: Tavolozze e gestione tavolozze
description: Gestione tavolozze di Windows, che fa parte di GDI, è destinato in modo specifico a schede di visualizzazione a 8 bit con una tavolozza hardware di 256 voci di colori.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL per Windows, gestione tavolozze
- OpenGL per Windows, tavolozze hardware
- gestione tavolozze OpenGL
- tavolozze hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298203"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="4b80d-107">Tavolozze e gestione tavolozze</span><span class="sxs-lookup"><span data-stu-id="4b80d-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="4b80d-108">Gestione tavolozze di Windows, che fa parte di GDI, è destinato in modo specifico a schede di visualizzazione a 8 bit con una *tavolozza hardware* di 256 voci di colori.</span><span class="sxs-lookup"><span data-stu-id="4b80d-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="4b80d-109">I pixel sullo schermo vengono archiviati come indice a 8 bit nella tavolozza hardware.</span><span class="sxs-lookup"><span data-stu-id="4b80d-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="4b80d-110">Ogni voce della tavolozza hardware in genere definisce un colore a 24 bit (8 ciascuno di rosso, verde e blu).</span><span class="sxs-lookup"><span data-stu-id="4b80d-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="4b80d-111">Gestione tavolozze gestisce una *tavolozza di sistema* che è una copia della tavolozza hardware.</span><span class="sxs-lookup"><span data-stu-id="4b80d-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="4b80d-112">La tavolozza di sistema è divisa in due sezioni: 20 colori riservati e i rimanenti colori 236, che è possibile impostare tramite Gestione tavolozze.</span><span class="sxs-lookup"><span data-stu-id="4b80d-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="4b80d-113">Una *tavolozza logica* di 20 colori predefinita viene selezionata e realizzata in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b80d-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="4b80d-114">È possibile creare e usare una nuova tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="4b80d-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="4b80d-115">Per modificare la tavolozza di sistema, selezionare e realizzare la tavolozza logica creata.</span><span class="sxs-lookup"><span data-stu-id="4b80d-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="4b80d-116">Probabilmente si creerà una tavolozza logica per specificare i colori che si desidera visualizzare nell'applicazione OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4b80d-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="4b80d-117">Utilizzando determinate chiamate GDI, è possibile sostituire temporaneamente la maggior parte della tavolozza di sistema con una tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="4b80d-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="4b80d-118">Utilizzando una tavolozza logica, è possibile definire i colori dei pixel per GDI utilizzando la modalità RGBA o l'indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="4b80d-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="4b80d-119">Le dimensioni massime di una tavolozza logica sono 256 colori per i dispositivi a 8 bit e 4.096 colori in un dispositivo a colori true (16, 24 e 32 bit).</span><span class="sxs-lookup"><span data-stu-id="4b80d-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="4b80d-120">Per ulteriori informazioni sulle modalità di RGBA e di indice dei colori, vedere modalità [RGBA e gestione tavolozza Windows](rgba-mode-and-windows-palette-management.md) e [modalità colori OpenGL e gestione tavolozza di Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="4b80d-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




