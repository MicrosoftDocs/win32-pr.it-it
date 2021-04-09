---
title: Sezione bitmap
description: Sezione bitmap
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- creazione di interfacce, sezione bitmap
- scrittura di codice per interfacce, sezione bitmap
- bitmap in interfacce, sezione bitmap
- file di definizione dell'interfaccia, sezione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044631"
---
# <a name="bitmaps-section"></a><span data-ttu-id="aecd4-109">Sezione bitmap</span><span class="sxs-lookup"><span data-stu-id="aecd4-109">Bitmaps Section</span></span>

<span data-ttu-id="aecd4-110">Successivamente, è necessario disporre di una sezione che definisce ognuno dei file bitmap.</span><span class="sxs-lookup"><span data-stu-id="aecd4-110">Next, you must have a section that defines each of your bitmap files.</span></span> <span data-ttu-id="aecd4-111">Ogni tipo di bitmap che verrà usato deve avere un file assegnato, sebbene sia possibile avere più di un tipo usando la stessa bitmap.</span><span class="sxs-lookup"><span data-stu-id="aecd4-111">Each type of bitmap you will use must have a file assigned to it, though you can have more than one type using the same bitmap.</span></span>


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="aecd4-112">La sezione bitmap deve iniziare con le bitmap di Word tra parentesi quadre, quindi una riga per ogni tipo di bitmap che si vuole definire.</span><span class="sxs-lookup"><span data-stu-id="aecd4-112">The Bitmaps section must begin with the word Bitmaps in brackets and then a line for each bitmap type you want to define.</span></span> <span data-ttu-id="aecd4-113">In questo esempio sono stati definiti cinque tipi di bitmap.</span><span class="sxs-lookup"><span data-stu-id="aecd4-113">In this example, five types of bitmaps were defined.</span></span> <span data-ttu-id="aecd4-114">Per ulteriori informazioni sulla sezione bitmap, vedere [bitmap](bitmaps.md) nel riferimento all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="aecd4-114">For more about the Bitmaps section, see [Bitmaps](bitmaps.md) in the Skin Reference.</span></span>

> [!Note]  
> <span data-ttu-id="aecd4-115">L'area e le bitmap con privilegi avanzati sono deprecate in Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="aecd4-115">The Region and Super bitmaps are deprecated in Windows Media Player 10 Mobile or later skins.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aecd4-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aecd4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aecd4-117">**Scrittura del codice**</span><span class="sxs-lookup"><span data-stu-id="aecd4-117">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




