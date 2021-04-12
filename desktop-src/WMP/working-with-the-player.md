---
title: Utilizzo del lettore
description: Utilizzo del lettore
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player Skin, attributo Player in JScript
- interfacce, attributo Player in JScript
- attributi, lettore
- attributo Player
- File JScript per interfacce, attributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396879"
---
# <a name="working-with-the-player"></a><span data-ttu-id="3b02a-108">Utilizzo del lettore</span><span class="sxs-lookup"><span data-stu-id="3b02a-108">Working with the Player</span></span>

<span data-ttu-id="3b02a-109">Quando si utilizza Microsoft JScript per accedere ai metodi e alle proprietà di Media Player di Windows, è necessario utilizzare il nome "Player" per il nome del controllo.</span><span class="sxs-lookup"><span data-stu-id="3b02a-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="3b02a-110">Per fare riferimento al metodo Stop, ad esempio, è necessario digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3b02a-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="3b02a-111">L'attributo globale **Player** è la chiave per accedere al controllo Media Player Windows tramite lo script dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3b02a-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="3b02a-112">Tramite questo attributo, tutti gli oggetti del controllo Media Player di Windows diventano accessibili per la modifica in fase di esecuzione tramite le proprietà e i metodi.</span><span class="sxs-lookup"><span data-stu-id="3b02a-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="3b02a-113">Inoltre, l'elemento **Player** è disponibile, in modo che sia possibile specificare i gestori eventi e l'attributo **URL** in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="3b02a-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b02a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b02a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b02a-115">**Utilizzo di JScript**</span><span class="sxs-lookup"><span data-stu-id="3b02a-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




