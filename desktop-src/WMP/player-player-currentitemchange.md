---
title: Evento Player. CurrentItemChange
description: L'evento CurrentItemChange si verifica quando viene modificato Controls. currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Media Player di Windows Event CurrentItemChange
- Windows Event CurrentItemChange Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332677"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="380ca-106">Evento Player. CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="380ca-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="380ca-107">L'evento **CurrentItemChange** si verifica quando i *controlli*. **CurrentItem** modifiche.</span><span class="sxs-lookup"><span data-stu-id="380ca-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="380ca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="380ca-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="380ca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="380ca-109">Parameters</span></span>

<span data-ttu-id="380ca-110">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="380ca-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="380ca-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="380ca-111">Return value</span></span>

<span data-ttu-id="380ca-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="380ca-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="380ca-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="380ca-113">Examples</span></span>

<span data-ttu-id="380ca-114">Nell'esempio JScript seguente viene illustrato un gestore eventi per il *lettore*. evento **currentItemChange** .</span><span class="sxs-lookup"><span data-stu-id="380ca-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="380ca-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="380ca-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="380ca-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="380ca-116">Requirements</span></span>



| <span data-ttu-id="380ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="380ca-117">Requirement</span></span> | <span data-ttu-id="380ca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="380ca-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="380ca-119">Versione</span><span class="sxs-lookup"><span data-stu-id="380ca-119">Version</span></span><br/> | <span data-ttu-id="380ca-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="380ca-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="380ca-121">DLL</span><span class="sxs-lookup"><span data-stu-id="380ca-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="380ca-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="380ca-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380ca-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="380ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380ca-124">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="380ca-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="380ca-125">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="380ca-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





