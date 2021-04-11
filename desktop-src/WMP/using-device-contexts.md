---
title: Uso dei contesti di dispositivo
description: Uso dei contesti di dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- Visualizzazioni, contesto di dispositivo
- Visualizzazioni personalizzate, contesto di dispositivo
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330535"
---
# <a name="using-device-contexts"></a><span data-ttu-id="0be9a-108">Uso dei contesti di dispositivo</span><span class="sxs-lookup"><span data-stu-id="0be9a-108">Using Device Contexts</span></span>

<span data-ttu-id="0be9a-109">Il contesto di dispositivo è un handle standard per un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0be9a-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="0be9a-110">Questa operazione è necessaria per molte funzioni di disegno, in modo che Microsoft Windows conosca la finestra in cui disegnare.</span><span class="sxs-lookup"><span data-stu-id="0be9a-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="0be9a-111">Per creare un rettangolo, ad esempio, è necessario specificare il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0be9a-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="0be9a-112">Il contesto di dispositivo viene specificato da Windows Media Player tramite la funzione **Render** .</span><span class="sxs-lookup"><span data-stu-id="0be9a-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="0be9a-113">Se il plug-in viene eseguito tramite una finestra, sarà necessario usare il contesto di dispositivo di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="0be9a-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="0be9a-114">Usare questo contesto di dispositivo per qualsiasi strumento di disegno che richiede un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0be9a-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0be9a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0be9a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be9a-116">**Implementazione di rendering**</span><span class="sxs-lookup"><span data-stu-id="0be9a-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




