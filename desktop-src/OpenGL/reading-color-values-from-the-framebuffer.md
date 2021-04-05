---
title: Lettura dei valori di colore dal framebuffer
description: Quando si usano le funzioni che leggono i valori di colore dal framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori di indice colore nei dispositivi con colori reali e nei dispositivi basati su tavolozza.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL per Windows, lettura dei valori dei colori da framebuffer
- lettura dei valori di colore da framebuffer OpenGL
- framebuffer, lettura dei valori di colore OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709358"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="0f4c4-106">Lettura dei valori di colore dal framebuffer</span><span class="sxs-lookup"><span data-stu-id="0f4c4-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="0f4c4-107">Quando si usano le funzioni che leggono i valori di colore dal framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori di indice colore nei dispositivi con colori reali e nei dispositivi basati su tavolozza.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="0f4c4-108">Su un dispositivo a colori true:</span><span class="sxs-lookup"><span data-stu-id="0f4c4-108">On a true-color device:</span></span>

-   <span data-ttu-id="0f4c4-109">I valori RGBA sono limitati al canale nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="0f4c4-110">I valori di indice dei colori vengono archiviati come valori RGBA nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="0f4c4-111">Quando si usano questi valori, è necessario eseguire una conversione inversa da RGBA all'indice della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="0f4c4-112">Se due indici logici hanno gli stessi valori RGBA, può essere restituito l'indice errato.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="0f4c4-113">In un dispositivo basato su tavolozza:</span><span class="sxs-lookup"><span data-stu-id="0f4c4-113">On a palette-based device:</span></span>

-   <span data-ttu-id="0f4c4-114">I valori RGBA vengono letti da un indice nella tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="0f4c4-115">L'indice logico viene ottenuto da una tabella inversa e vengono estratti i componenti RGBA.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="0f4c4-116">I valori di indice colore vengono letti da un indice nella tavolozza di sistema e viene utilizzata una tabella inversa per ottenere l'indice della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="0f4c4-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




