---
description: Bump mapping è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi degli oggetti tassellati senza richiedere conteggi di poligoni estremamente elevati.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127390"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="288b7-103">Bump mapping (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="288b7-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="288b7-104">Bump mapping è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi degli oggetti tassellati senza richiedere conteggi di poligoni estremamente elevati.</span><span class="sxs-lookup"><span data-stu-id="288b7-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="288b7-105">Il mapping di Bump implementato da Direct3D può essere descritto accuratamente come una coordinata di trama per ogni pixel di mappe dell'ambiente speculare o diffusa, perché vengono fornite informazioni sul contorno della mappa a urto in termini di valori Delta, che il sistema applica alle coordinate di trama utente e v di una mappa dell'ambiente nella successiva fase della trama.</span><span class="sxs-lookup"><span data-stu-id="288b7-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="288b7-106">I valori delta vengono codificati nel formato pixel della superficie della mappa di Bump (vedere la pagina relativa ai [formati dei pixel di bump map](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="288b7-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="288b7-107">Il mapping di Bump si basa sulla fusione di più trame.</span><span class="sxs-lookup"><span data-stu-id="288b7-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="288b7-108">Ciò significa che il dispositivo deve supportare almeno due fasi di fusione. uno per la mappa bump e l'altro per una mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="288b7-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="288b7-109">Per applicare una mappa di trama di base aggiuntiva, ovvero il caso più comune, sono necessarie almeno tre fasi di combinazione di trame.</span><span class="sxs-lookup"><span data-stu-id="288b7-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="288b7-110">Il diagramma seguente illustra le relazioni tra la trama di base, la mappa a urto e la mappa dell'ambiente nella trama a cascata.</span><span class="sxs-lookup"><span data-stu-id="288b7-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![diagramma della fusione di trama a cascata](images/bumpmap-tcascade.png)

<span data-ttu-id="288b7-112">È necessario preparare le fasi di trama in modo appropriato per abilitare il mapping di Bump.</span><span class="sxs-lookup"><span data-stu-id="288b7-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="288b7-113">Gli argomenti seguenti introducono il mapping di bump e forniscono informazioni dettagliate su come è possibile usarlo nelle applicazioni:</span><span class="sxs-lookup"><span data-stu-id="288b7-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="288b7-114">Formati pixel della mappa Bump</span><span class="sxs-lookup"><span data-stu-id="288b7-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="288b7-115">Formule di mapping Bump</span><span class="sxs-lookup"><span data-stu-id="288b7-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="288b7-116">Uso di bump mapping</span><span class="sxs-lookup"><span data-stu-id="288b7-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="288b7-117">Direct3D non supporta in modo nativo i mapping di altezza; sono semplicemente un formato semplice in cui archiviare e visualizzare i dati di contorno.</span><span class="sxs-lookup"><span data-stu-id="288b7-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="288b7-118">L'applicazione può archiviare le informazioni di contorno in qualsiasi formato o persino generare una mappa Bump procedurale.</span><span class="sxs-lookup"><span data-stu-id="288b7-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="288b7-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="288b7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="288b7-120">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="288b7-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



