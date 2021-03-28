---
description: È possibile avviare una visualizzazione radice di un punto di giunzione tramite un file di collegamento a tale punto di giunzione.
title: Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227430"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="47fa5-103">Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento</span><span class="sxs-lookup"><span data-stu-id="47fa5-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="47fa5-104">È possibile avviare una visualizzazione radice di un punto di giunzione tramite un [file di collegamento](./links.md) a tale punto di giunzione.</span><span class="sxs-lookup"><span data-stu-id="47fa5-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="47fa5-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="47fa5-105">Instructions</span></span>


<span data-ttu-id="47fa5-106">Impostare la riga di destinazione del file di collegamento su Explorer.exe con un flag/root.</span><span class="sxs-lookup"><span data-stu-id="47fa5-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="47fa5-107">Il formato esatto del comando dipende dalla posizione del punto di giunzione:</span><span class="sxs-lookup"><span data-stu-id="47fa5-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="47fa5-108">Se il punto di giunzione è una sottocartella del desktop, usare:</span><span class="sxs-lookup"><span data-stu-id="47fa5-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="47fa5-109">Se il punto di giunzione è una cartella file system, usare:</span><span class="sxs-lookup"><span data-stu-id="47fa5-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="47fa5-110">Se il punto di giunzione è una sottocartella di una cartella virtuale di sistema, usare:</span><span class="sxs-lookup"><span data-stu-id="47fa5-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="47fa5-111">Le cartelle virtuali di sistema che possono contenere punti di giunzione hanno gli identificatori di classe seguenti (CLSID):</span><span class="sxs-lookup"><span data-stu-id="47fa5-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="47fa5-112">Risorse del computer</span><span class="sxs-lookup"><span data-stu-id="47fa5-112">My Computer</span></span>       | <span data-ttu-id="47fa5-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="47fa5-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="47fa5-114">Risorse di rete</span><span class="sxs-lookup"><span data-stu-id="47fa5-114">My Network Places</span></span> | <span data-ttu-id="47fa5-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="47fa5-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="47fa5-116">Control panel</span><span class="sxs-lookup"><span data-stu-id="47fa5-116">Control Panel</span></span>     | <span data-ttu-id="47fa5-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="47fa5-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="47fa5-118">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="47fa5-118">Internet Explorer</span></span> | <span data-ttu-id="47fa5-119">871C5380-42A0-1069-A2EA-08002B30309D</span><span class="sxs-lookup"><span data-stu-id="47fa5-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="47fa5-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47fa5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fa5-121">Impostazione della posizione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47fa5-121">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="47fa5-122">Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="47fa5-122">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
