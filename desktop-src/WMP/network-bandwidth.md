---
title: Rete. larghezza di banda
description: La proprietà bandWidth recupera la larghezza di banda corrente della clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Media Player Windows per la larghezza di banda di rete
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326122"
---
# <a name="networkbandwidth"></a><span data-ttu-id="9a0b2-104">Rete. larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="9a0b2-104">Network.bandWidth</span></span>

<span data-ttu-id="9a0b2-105">La proprietà **Bandwidth** recupera la larghezza di banda corrente della clip.</span><span class="sxs-lookup"><span data-stu-id="9a0b2-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0b2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a0b2-106">Syntax</span></span>

<span data-ttu-id="9a0b2-107">*Player*. *rete*. **larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="9a0b2-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9a0b2-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9a0b2-108">Possible Values</span></span>

<span data-ttu-id="9a0b2-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="9a0b2-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0b2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a0b2-110">Remarks</span></span>

<span data-ttu-id="9a0b2-111">Questa proprietà restituisce zero se il *lettore*. La proprietà **URL** non è impostata.</span><span class="sxs-lookup"><span data-stu-id="9a0b2-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="9a0b2-112">Questa proprietà è valida solo per i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9a0b2-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="9a0b2-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9a0b2-113">Examples</span></span>

<span data-ttu-id="9a0b2-114">Nell'esempio Microsoft JScript seguente viene utilizzata la *rete*. **larghezza** di banda per visualizzare la larghezza di banda media corrente.</span><span class="sxs-lookup"><span data-stu-id="9a0b2-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="9a0b2-115">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BW".</span><span class="sxs-lookup"><span data-stu-id="9a0b2-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="9a0b2-116">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9a0b2-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="9a0b2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a0b2-117">Requirements</span></span>



| <span data-ttu-id="9a0b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0b2-118">Requirement</span></span> | <span data-ttu-id="9a0b2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9a0b2-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0b2-120">Versione</span><span class="sxs-lookup"><span data-stu-id="9a0b2-120">Version</span></span><br/> | <span data-ttu-id="9a0b2-121">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="9a0b2-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9a0b2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9a0b2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a0b2-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0b2-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0b2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a0b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0b2-125">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="9a0b2-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="9a0b2-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="9a0b2-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





