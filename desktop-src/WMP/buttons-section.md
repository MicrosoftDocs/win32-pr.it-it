---
title: Sezione pulsanti
description: Sezione pulsanti
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Interfacce di Windows Media Player Mobile, sezione pulsanti
- interfacce, sezione pulsanti
- creazione di interfacce, sezione pulsanti
- scrittura di codice per interfacce, sezione pulsanti
- pulsanti nella sezione interfacce, pulsanti
- file di definizione dell'interfaccia, sezione pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044934"
---
# <a name="buttons-section"></a><span data-ttu-id="47a1d-109">Sezione pulsanti</span><span class="sxs-lookup"><span data-stu-id="47a1d-109">Buttons Section</span></span>

<span data-ttu-id="47a1d-110">Successivamente, è necessario definire i pulsanti che verranno utilizzati:</span><span class="sxs-lookup"><span data-stu-id="47a1d-110">Next, you must define the buttons you will be using:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



<span data-ttu-id="47a1d-111">In questa sezione sono definiti quattro pulsanti.</span><span class="sxs-lookup"><span data-stu-id="47a1d-111">There are four buttons defined in this section.</span></span> <span data-ttu-id="47a1d-112">La pagina visualizzata può eseguire il wrapping di queste righe, ma quando si digita il codice, non è necessario eseguire il wrapping delle righe; ovvero ogni riga deve essere completa e terminare con un segno di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="47a1d-112">The page you are viewing may wrap these lines, but when you type in the code, you must not wrap lines; that is, each line must be complete and end with a paragraph mark.</span></span>

> [!Note]  
> <span data-ttu-id="47a1d-113">I tipi di pulsanti sono deprecati in Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="47a1d-113">Buttons types are deprecated in Windows Media Player 10 Mobile or later skins.</span></span> <span data-ttu-id="47a1d-114">Invece di un tipo di pulsante dichiarato nel file skin, immettere "NA" per ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="47a1d-114">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

<span data-ttu-id="47a1d-115">Per ogni pulsante è necessario definire la funzione, il tipo, il percorso, l'origine dell'immagine push, l'origine disabilitata e il colore (per i pulsanti di tipo hit).</span><span class="sxs-lookup"><span data-stu-id="47a1d-115">For each button you must define the function, type, location, pushed image source, disabled source, and color (for hit-type buttons).</span></span> <span data-ttu-id="47a1d-116">Inoltre, per il pulsante come playpause, è necessario definire le origini delle immagini normale e push per lo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="47a1d-116">In addition, for the PlayPause button, you must define the normal and pushed image sources for the paused state.</span></span>

<span data-ttu-id="47a1d-117">Per ulteriori informazioni sulla sezione Buttons del file di definizione dell'interfaccia personalizzata, vedere [Buttons](buttons.md) in the Skin Reference.</span><span class="sxs-lookup"><span data-stu-id="47a1d-117">For more about the Buttons section of the skin definition file, see [Buttons](buttons.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47a1d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47a1d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a1d-119">**Scrittura del codice**</span><span class="sxs-lookup"><span data-stu-id="47a1d-119">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




