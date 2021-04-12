---
title: Attributi globali (Windows Media Player SDK)
description: Attributi globali
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player Skin, attributi globali
- interfacce, attributi globali
- riferimento per le interfacce, attributi globali
- attributi globali
- attributi, globali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104398178"
---
# <a name="global-attributes"></a><span data-ttu-id="adab3-108">Attributi globali</span><span class="sxs-lookup"><span data-stu-id="adab3-108">Global Attributes</span></span>

<span data-ttu-id="adab3-109">Gli attributi globali sono attributi che consentono di accedere facilmente a determinati elementi o oggetti dei giocatori da qualsiasi punto all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="adab3-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="adab3-110">L'attributo globale **Player** è un riferimento all'oggetto [Player](player-object.md) e viene usato per accedere alle funzionalità principali di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="adab3-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="adab3-111">Nell'esempio seguente viene usato **Player** per iniziare la riproduzione di file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="adab3-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="adab3-112">L'attributo globale del **tema** è un riferimento all'elemento [Theme](theme-element.md) .</span><span class="sxs-lookup"><span data-stu-id="adab3-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="adab3-113">Questo è il modo giusto per accedere agli attributi del **tema** , anziché specificare un ID nell'elemento **Theme** .</span><span class="sxs-lookup"><span data-stu-id="adab3-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="adab3-114">Nell'esempio seguente viene usato il **tema** per aprire una nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="adab3-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="adab3-115">L'attributo **View** Global è un riferimento alla [visualizzazione](view-element.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="adab3-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="adab3-116">Questa operazione può essere utilizzata al posto dell'ID specificato nei vari elementi di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="adab3-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="adab3-117">Nell'esempio seguente viene utilizzata la **vista** per chiudere la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="adab3-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="adab3-118">L'attributo Global dell' **evento** viene usato per accedere agli attributi degli eventi di ambiente dall'interno di gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="adab3-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="adab3-119">Nell'esempio seguente viene usato l' **evento** per determinare se il tasto ALT viene premuto quando si fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="adab3-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="adab3-120">L'attributo globale **playerApplication** è un riferimento all'oggetto [playerApplication](playerapplication-object.md) e viene usato dai file di interfaccia specificati come interfacce utente personalizzate per i controlli del lettore remoto.</span><span class="sxs-lookup"><span data-stu-id="adab3-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="adab3-121">Il controllo Player può essere incorporato in modalità remota solo nei programmi C++ che implementano l'interfaccia **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="adab3-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="adab3-122">Nell'esempio seguente viene usato **playerApplication** per passare alla modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="adab3-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="adab3-123">Per altre informazioni, vedere [attributi degli eventi di ambiente](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="adab3-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adab3-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="adab3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adab3-125">**Varie**</span><span class="sxs-lookup"><span data-stu-id="adab3-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




