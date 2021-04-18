---
title: WMPEFFECTS
description: Si tratta di effetti predefiniti con i seguenti valori predefiniti.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- Media Player Windows WMPEFFECTS
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329677"
---
# <a name="wmpeffects"></a><span data-ttu-id="bae4b-104">WMPEFFECTS</span><span class="sxs-lookup"><span data-stu-id="bae4b-104">WMPEFFECTS</span></span>

<span data-ttu-id="bae4b-105">Si tratta di **effetti** predefiniti con i seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bae4b-105">This is a predefined **EFFECTS** with the following default values.</span></span>

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a><span data-ttu-id="bae4b-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="bae4b-106">Remarks</span></span>

<span data-ttu-id="bae4b-107">Verrà creato un elemento **Effects** che eseguirà l'istruzione nei set di impostazioni di visualizzazione quando l'utente fa clic sul controllo.</span><span class="sxs-lookup"><span data-stu-id="bae4b-107">This will create an **EFFECTS** element that will step through the visualization presets when the user clicks the control.</span></span> <span data-ttu-id="bae4b-108">Si estenderanno anche le visualizzazioni quando il lettore viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="bae4b-108">It will also stretch the visualizations when the player is resized.</span></span>

<span data-ttu-id="bae4b-109">Il set di impostazioni di visualizzazione iniziale visualizzato è quello selezionato nel menu **Visualizza** in **visualizzazioni**.</span><span class="sxs-lookup"><span data-stu-id="bae4b-109">The initial visualization preset shown is the one selected on the **View** menu under **Visualizations**.</span></span> <span data-ttu-id="bae4b-110">Se si modifica la selezione in questo menu, il set di impostazioni visualizzato da questo elemento verrà modificato automaticamente quando il lettore è in modalità Skin.</span><span class="sxs-lookup"><span data-stu-id="bae4b-110">Changing the selection on this menu will automatically change the preset displayed by this element when the Player is in skin mode.</span></span> <span data-ttu-id="bae4b-111">Il menu **Visualizza** viene visualizzato nella modalità completa del lettore o quando l'attributo **View. barra** del titolo è impostato su true in un'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bae4b-111">The **View** menu is displayed in the full mode of the Player or when the **VIEW.titleBar** attribute is set to true in a skin.</span></span>

<span data-ttu-id="bae4b-112">È possibile eseguire l'override di tutte le proprietà di questo elemento **Effects** specificandone le proprietà in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="bae4b-112">All properties of this **EFFECTS** element can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae4b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bae4b-113">Requirements</span></span>



| <span data-ttu-id="bae4b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bae4b-114">Requirement</span></span> | <span data-ttu-id="bae4b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bae4b-115">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="bae4b-116">Versione</span><span class="sxs-lookup"><span data-stu-id="bae4b-116">Version</span></span><br/> | <span data-ttu-id="bae4b-117">Windows Media Player 7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bae4b-117">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bae4b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bae4b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae4b-119">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="bae4b-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





