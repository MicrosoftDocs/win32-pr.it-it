---
title: Rete. frameRate
description: La proprietà frameRate recupera la frequenza dei fotogrammi video corrente in frame per cento secondi. Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Media Player Windows di rete. frameRate
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329442"
---
# <a name="networkframerate"></a><span data-ttu-id="da962-105">Rete. frameRate</span><span class="sxs-lookup"><span data-stu-id="da962-105">Network.frameRate</span></span>

<span data-ttu-id="da962-106">La proprietà **framerate** recupera la frequenza dei fotogrammi video corrente in frame per cento secondi.</span><span class="sxs-lookup"><span data-stu-id="da962-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="da962-107">Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="da962-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="da962-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da962-108">Syntax</span></span>

<span data-ttu-id="da962-109">*Player*. *rete*. **framerate**</span><span class="sxs-lookup"><span data-stu-id="da962-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="da962-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="da962-110">Possible Values</span></span>

<span data-ttu-id="da962-111">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="da962-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="da962-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="da962-112">Examples</span></span>

<span data-ttu-id="da962-113">Nell'esempio JScript seguente viene utilizzata la *rete*. **framerate** per visualizzare la frequenza dei fotogrammi corrente.</span><span class="sxs-lookup"><span data-stu-id="da962-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="da962-114">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="da962-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="da962-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="da962-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="da962-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da962-116">Requirements</span></span>



| <span data-ttu-id="da962-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="da962-117">Requirement</span></span> | <span data-ttu-id="da962-118">Valore</span><span class="sxs-lookup"><span data-stu-id="da962-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da962-119">Versione</span><span class="sxs-lookup"><span data-stu-id="da962-119">Version</span></span><br/> | <span data-ttu-id="da962-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="da962-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="da962-121">DLL</span><span class="sxs-lookup"><span data-stu-id="da962-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="da962-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da962-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da962-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da962-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da962-124">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="da962-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="da962-125">**Rete. encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="da962-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





