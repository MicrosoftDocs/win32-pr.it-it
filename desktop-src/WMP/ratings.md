---
title: Classificazioni
description: Classificazioni
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Interfacce di Windows Media Player Mobile, classificazioni
- interfacce, classificazioni
- riferimento per interfacce, classificazioni
- classificazioni in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298698"
---
# <a name="ratings"></a><span data-ttu-id="63336-107">Classificazioni</span><span class="sxs-lookup"><span data-stu-id="63336-107">Ratings</span></span>

<span data-ttu-id="63336-108">Quando si crea un'interfaccia personalizzata per Windows Media Player 10,1 Mobile, è possibile visualizzare la classificazione associata al contenuto basato su Windows Media Audio in corso di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="63336-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="63336-109">La classificazione viene visualizzata come stella con un numero.</span><span class="sxs-lookup"><span data-stu-id="63336-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="63336-110">La stella sarà numerata da uno a cinque, indicando la classificazione corrente per quel contenuto.</span><span class="sxs-lookup"><span data-stu-id="63336-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="63336-111">Se il contenuto non viene valutato, la stella sarà numerata zero.</span><span class="sxs-lookup"><span data-stu-id="63336-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="63336-112">La sezione classificazioni del file di definizione dell'interfaccia personalizzata inizia con questa riga:</span><span class="sxs-lookup"><span data-stu-id="63336-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="63336-113">È quindi necessario aggiungere una riga che contiene informazioni sulle dimensioni e la posizione dell'icona di classificazione nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63336-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="63336-114">È possibile usare il modello seguente per la sezione ratings del file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="63336-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="63336-115">È anche possibile assegnare un valore di classificazione a un elemento multimediale tramite l'interfaccia utente in Windows Media Player 10,1 mobile e alla successiva sincronizzazione del dispositivo con il computer, il nuovo valore delle classificazioni verrà propagato a tale elemento multimediale se risiede nella libreria di Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="63336-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63336-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63336-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63336-117">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="63336-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




