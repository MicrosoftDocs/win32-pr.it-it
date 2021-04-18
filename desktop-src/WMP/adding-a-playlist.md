---
title: Aggiunta di una playlist
description: Aggiunta di una playlist
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- creazione di interfacce, playlist
- Interfacce di Media Player Windows, playlist
- interfacce, playlist
- playlist, interfacce
- playlist di metafile, interfacce
- Playlist Windows Media Metafile, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298575"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="e297f-109">Aggiunta di una playlist</span><span class="sxs-lookup"><span data-stu-id="e297f-109">Adding a Playlist</span></span>

<span data-ttu-id="e297f-110">È possibile usare le playlist per scegliere tra raccolte di audio e video.</span><span class="sxs-lookup"><span data-stu-id="e297f-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="e297f-111">Usando l'immagine dalla prima interfaccia, è possibile apportare alcune modifiche al file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e297f-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="e297f-112">Il primo passaggio consiste nell'usare la shell che verrà usata per la maggior parte delle interfacce:</span><span class="sxs-lookup"><span data-stu-id="e297f-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="e297f-113">Aggiungere ora una seconda **visualizzazione** che contiene una playlist.</span><span class="sxs-lookup"><span data-stu-id="e297f-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="e297f-114">Inserire il codice seguente dopo il </VIEW> del codice della shell.</span><span class="sxs-lookup"><span data-stu-id="e297f-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="e297f-115">È necessario assegnare a questa seconda visualizzazione un ID per potervi fare riferimento in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="e297f-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="e297f-116">Aggiungere un oggetto PLAYelement e un oggetto STOPelement.</span><span class="sxs-lookup"><span data-stu-id="e297f-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="e297f-117">Questi pulsanti predefiniti semplificano la vita.</span><span class="sxs-lookup"><span data-stu-id="e297f-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="e297f-118">Infine, aggiungere un evento OnClick all'oggetto PLAYelement per visualizzare una playlist nella seconda visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="e297f-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="e297f-119">Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia della playlist di lavoro simile.</span><span class="sxs-lookup"><span data-stu-id="e297f-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e297f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e297f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e297f-121">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="e297f-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




