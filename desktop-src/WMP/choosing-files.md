---
title: Scelta di file
description: Scelta di file
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- creazione di interfacce, scelta di file
- Windows Media Player Skins, scelta di file
- interfacce, scelta di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221876"
---
# <a name="choosing-files"></a><span data-ttu-id="c20c1-106">Scelta di file</span><span class="sxs-lookup"><span data-stu-id="c20c1-106">Choosing Files</span></span>

<span data-ttu-id="c20c1-107">Se si vuole scegliere un file, è possibile usare codice simile a quello dell'esempio della playlist, ma sostituire quanto segue per la sezione PLAYelement:</span><span class="sxs-lookup"><span data-stu-id="c20c1-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="c20c1-108">Questa riga userà il metodo **openDialog** del **tema** per definire un **URL** per il lettore.</span><span class="sxs-lookup"><span data-stu-id="c20c1-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="c20c1-109">Questa operazione può essere usata per scegliere i file che non sono presenti in playlist.</span><span class="sxs-lookup"><span data-stu-id="c20c1-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="c20c1-110">Nella sezione di esempio dell'SDK è possibile vedere un esempio di **openDialog** funzionante simile.</span><span class="sxs-lookup"><span data-stu-id="c20c1-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c20c1-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c20c1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c20c1-112">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c20c1-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




