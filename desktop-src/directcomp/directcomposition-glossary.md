---
title: Glossario DirectComposition
description: Questo argomento definisce le condizioni di DirectComposition Microsoft.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338047"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="a5f9e-103">Glossario DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a5f9e-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="a5f9e-104">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="a5f9e-105">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="a5f9e-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="a5f9e-106">Questo argomento definisce le condizioni di DirectComposition Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="a5f9e-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animazione (funzione)**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-108">Costrutto che specifica la modalità di modifica del valore di una singola proprietà dell'oggetto in un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**oggetto Animation**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-110">Oggetto che rappresenta una funzione per l'animazione delle proprietà di un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento di animazione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-112">Definizioni di intervallo fondamentali di una funzione di animazione; sono le primitive da cui vengono compilate funzioni di animazione più complesse e di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**buffer nascosto**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-114">Un rettangolo di memoria in cui un'applicazione può scrivere direttamente.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="a5f9e-115">Il buffer nascosto non viene mai visualizzato direttamente sul monitor.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-117">Gruppo di chiamate al metodo DirectComposition elaborate atomicamente.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-119">Un buffer di colore, con o senza un canale alfa, che risiede nella memoria di sistema o video.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modalità bordo**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-121">Proprietà di un oggetto visivo Microsoft DirectComposition che influiscono sulla composizione dei bordi di una bitmap quando la bitmap viene trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="a5f9e-122">Influiscono inoltre sul modo in cui il contenuto viene ritagliato negli angoli di una clip con angoli arrotondati e al bordo di una clip trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-124">Oggetto che rappresenta un rettangolo di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**rettangolo di ritaglio**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-126">Set di coordinate che definiscono l'area del contenuto bitmap dell'oggetto visivo disegnato sullo schermo quando viene eseguito il rendering della bitmap.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**mantello**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-128">Per impedire temporaneamente a Gestione finestre desktop (DWM) di disegnare una finestra sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="a5f9e-129">Le applicazioni in genere mascherano una finestra mentre DirectComposition usa la bitmap della finestra in una composizione.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-131">Per inviare un batch di comandi a DirectCompositionDirectComposition per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modalità composita**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-133">Uno dei diversi modi per combinare due bitmap, un'origine e una destinazione, per ottenere un effetto particolare.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Composizione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-135">Raccolta di bitmap combinate e modificate applicando varie trasformazioni, effetti e animazioni per produrre un risultato visivo previsto in un'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**finestra di destinazione composizione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-137">La finestra a cui è associata una struttura ad albero visuale e in cui viene disegnata la composizione risultante.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effetto**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-139">Operazione che modifica il modo in cui le bitmap di una struttura ad albero visuale vengono rasterizzate, in genere applicando un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**gruppo effetti**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-141">Gruppo di effetti bitmap che vengono applicati insieme per modificare la rasterizzazione del sottoalbero di un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-143">Iterazione del motore di composizione che produce una rasterizzazione della struttura ad albero visuale.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**buffer anteriore**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-145">Un rettangolo di memoria convertito dalla scheda grafica e visualizzato sul monitor.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modalità di interpolazione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-147">Proprietà che determina la modalità di composizione di una bitmap quando viene trasformata in modo tale che non esista una corrispondenza uno-a-uno tra i pixel nella bitmap e i pixel sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**elemento visivo radice**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-149">Oggetto visivo da cui discendono tutti gli altri oggetti visivi in una struttura ad albero visuale.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Scambia catena**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-151">Raccolta di uno o più buffer back che possono essere presentati in modo seriale al buffer anteriore</span><span class="sxs-lookup"><span data-stu-id="a5f9e-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**area**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-153">Rappresentazione di un'area lineare della memoria di visualizzazione che in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**trasformazione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-155">Matrice che rappresenta una trasformazione delle coordinate in uno spazio bidimensionale o tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**gruppo di trasformazione**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-157">Raccolta di trasformazioni le cui matrici vengono moltiplicate insieme nell'ordine in cui sono specificate nella raccolta prima che vengano applicate a un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-159">Oggetto che contiene un riferimento facoltativo a un oggetto bitmap e un set di proprietà che determinano la posizione e il modo in cui viene eseguito il rendering della bitmap sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**oggetto visivo**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-161">Vedere [*Visual*](/windows).</span><span class="sxs-lookup"><span data-stu-id="a5f9e-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**sottoalbero visuale**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-163">Parte di una struttura ad albero visuale costituita da un oggetto visivo particolare e da tutti i relativi oggetti visivi figlio e discendente.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**struttura ad albero visuale**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-165">Raccolta gerarchica di oggetti visivi utilizzati per creare una composizione.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="a5f9e-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**catena di scambio senza finestra**</span><span class="sxs-lookup"><span data-stu-id="a5f9e-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="a5f9e-167">Catena di scambio associata a un oggetto visivo DirectComposition anziché a una finestra.</span><span class="sxs-lookup"><span data-stu-id="a5f9e-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 