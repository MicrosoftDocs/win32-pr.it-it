---
description: È possibile avviare una visualizzazione radice di un punto di giunzione tramite un file di collegamento a tale punto di giunzione.
title: Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581609"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="825db-103">Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento</span><span class="sxs-lookup"><span data-stu-id="825db-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="825db-104">È possibile avviare una visualizzazione radice di un punto di giunzione tramite un [file di collegamento](./links.md) a tale punto di giunzione.</span><span class="sxs-lookup"><span data-stu-id="825db-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="825db-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="825db-105">Instructions</span></span>


<span data-ttu-id="825db-106">Impostare la riga di destinazione del file di collegamento Explorer.exe con un flag /root.</span><span class="sxs-lookup"><span data-stu-id="825db-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="825db-107">La forma esatta del comando dipende dalla posizione del punto di giunzione:</span><span class="sxs-lookup"><span data-stu-id="825db-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="825db-108">Se il punto di giunzione è una sottocartella del desktop, usare:</span><span class="sxs-lookup"><span data-stu-id="825db-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="825db-109">Se il punto di giunzione è una file system, usare:</span><span class="sxs-lookup"><span data-stu-id="825db-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="825db-110">Se il punto di giunzione è una sottocartella di una cartella virtuale di sistema, usare:</span><span class="sxs-lookup"><span data-stu-id="825db-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="825db-111">Le cartelle virtuali di sistema che possono contenere punti di giunzione hanno gli identificatori di classe (CLSID) seguenti:</span><span class="sxs-lookup"><span data-stu-id="825db-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="825db-112">Cartella di sistema</span><span class="sxs-lookup"><span data-stu-id="825db-112">System folder</span></span>     | <span data-ttu-id="825db-113">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="825db-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="825db-114">Risorse del computer</span><span class="sxs-lookup"><span data-stu-id="825db-114">My Computer</span></span>       | <span data-ttu-id="825db-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825db-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="825db-116">Risorse di rete</span><span class="sxs-lookup"><span data-stu-id="825db-116">My Network Places</span></span> | <span data-ttu-id="825db-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825db-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="825db-118">Control panel</span><span class="sxs-lookup"><span data-stu-id="825db-118">Control Panel</span></span>     | <span data-ttu-id="825db-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825db-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="825db-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="825db-120">Internet Explorer</span></span> | <span data-ttu-id="825db-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825db-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="825db-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="825db-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825db-123">Specifica del percorso di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="825db-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="825db-124">Come aprire una visualizzazione radice di un punto di giunzione tramite il Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="825db-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
