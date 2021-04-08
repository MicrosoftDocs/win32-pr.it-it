---
title: Sezione Descrizione
description: Sezione Descrizione
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Mobile Skins, sezione Descrizione
- interfacce, sezione Descrizione
- creazione di interfacce, sezione Descrizione
- scrittura del codice per le interfacce, sezione Descrizione
- Sezione Descrizione in Skins
- file di definizione dell'interfaccia, sezione Descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856797"
---
# <a name="description-section"></a><span data-ttu-id="6f8df-109">Sezione Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f8df-109">Description Section</span></span>

<span data-ttu-id="6f8df-110">Successivamente, è necessario fornire una sezione che descriva le dimensioni e l'orientamento dell'interfaccia durante la creazione di un'interfaccia per Windows Media Player 9 Series per Windows Mobile 2003 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="6f8df-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="6f8df-111">La sezione Descrizione deve iniziare con la parola Descrizione tra parentesi quadre, quindi includere una riga che specifichi le dimensioni e la risoluzione dello schermo per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f8df-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="6f8df-112">Le righe che iniziano con due barre non vengono elaborate e possono essere usate per i commenti o, come illustrato nel codice precedente, un modello che consente di ricordare cosa accade in una sezione.</span><span class="sxs-lookup"><span data-stu-id="6f8df-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="6f8df-113">È anche possibile usare i modelli per allineare tutti gli elementi alle colonne.</span><span class="sxs-lookup"><span data-stu-id="6f8df-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="6f8df-114">Per ulteriori informazioni sulla sezione Descrizione, vedere [Description](description.md) in the Skin Reference.</span><span class="sxs-lookup"><span data-stu-id="6f8df-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f8df-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f8df-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f8df-116">**Scrittura del codice**</span><span class="sxs-lookup"><span data-stu-id="6f8df-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




