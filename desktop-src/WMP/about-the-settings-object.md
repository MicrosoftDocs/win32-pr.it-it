---
title: Informazioni sull'oggetto Settings
description: Informazioni sull'oggetto Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, oggetto Settings
- Modello a oggetti di Windows Media Player, oggetto Settings
- modello a oggetti, oggetto Settings
- Controllo ActiveX Windows Media Player, oggetto Settings
- Controllo ActiveX, oggetto Settings
- Controllo ActiveX Windows Media Player Mobile, oggetto Settings
- Windows Media Player Mobile, oggetto Settings
- Oggetto Settings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855569"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="54ff6-111">Informazioni sull'oggetto Settings</span><span class="sxs-lookup"><span data-stu-id="54ff6-111">About the Settings Object</span></span>

<span data-ttu-id="54ff6-112">L'oggetto **Settings** governa le impostazioni del controllo, ad esempio volume, Play Count, mute e così via.</span><span class="sxs-lookup"><span data-stu-id="54ff6-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="54ff6-113">È accessibile solo tramite la proprietà **Settings** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="54ff6-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="54ff6-114">La proprietà **Settings** restituisce l'oggetto **Settings** .</span><span class="sxs-lookup"><span data-stu-id="54ff6-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="54ff6-115">È possibile accedere alle proprietà dell'oggetto **Impostazioni** solo dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="54ff6-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="54ff6-116">Per ottenere, ad esempio, il valore della proprietà **volume** , è necessario usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="54ff6-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="54ff6-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54ff6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ff6-118">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="54ff6-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="54ff6-119">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="54ff6-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




