---
title: Modifica dei valori di attributo
description: Modifica dei valori di attributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, modifica di valori
- modifica dei valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044865"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="238df-114">Modifica dei valori di attributo</span><span class="sxs-lookup"><span data-stu-id="238df-114">Changing Attribute Values</span></span>

<span data-ttu-id="238df-115">È possibile modificare il valore di un attributo se la pagina Web o l'applicazione ha accesso in lettura/scrittura alla libreria e l'attributo può essere letto e scritto.</span><span class="sxs-lookup"><span data-stu-id="238df-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="238df-116">È possibile modificare un attributo dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="238df-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="238df-117">Per modificare gli attributi di più elementi multimediali, è possibile assegnare ognuno di essi a turno al *lettore*. proprietà **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="238df-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="238df-118">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="238df-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="238df-119">Per modificare un attributo, chiamare il *lettore*. *currentMedia*. metodo **setItemInfo** come illustrato nell'esempio di C# seguente.</span><span class="sxs-lookup"><span data-stu-id="238df-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="238df-120">Si consiglia di chiamare il *supporto*. metodo **isReadOnlyItem** per determinare se è possibile modificare un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="238df-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="238df-121">Se si incorpora il controllo nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="238df-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="238df-122">Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che vengono modificati verranno scritti nel file multimediale digitale subito dopo aver apportato le modifiche.</span><span class="sxs-lookup"><span data-stu-id="238df-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="238df-123">In entrambi i casi, le modifiche sono immediatamente disponibili tramite la libreria.</span><span class="sxs-lookup"><span data-stu-id="238df-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="238df-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="238df-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="238df-125">**Attributi elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="238df-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="238df-126">**Accesso alla libreria**</span><span class="sxs-lookup"><span data-stu-id="238df-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="238df-127">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="238df-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="238df-128">**Lettura di valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="238df-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




