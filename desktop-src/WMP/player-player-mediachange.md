---
title: Evento Player. MediaChange
description: L'evento MediaChange si verifica quando viene modificato un elemento multimediale. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player di Windows Event MediaChange
- Windows Event MediaChange Media Player, classe Player
- Classe Player Windows Media Player, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331857"
---
# <a name="playermediachange-event"></a><span data-ttu-id="d41e9-107">Evento Player. MediaChange</span><span class="sxs-lookup"><span data-stu-id="d41e9-107">Player.MediaChange event</span></span>

<span data-ttu-id="d41e9-108">L'evento **MediaChange** si verifica quando viene modificato un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d41e9-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41e9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d41e9-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="d41e9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d41e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41e9-111">*Item*</span><span class="sxs-lookup"><span data-stu-id="d41e9-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="d41e9-112">Oggetto **multimediale** che rappresenta l'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="d41e9-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41e9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d41e9-113">Return value</span></span>

<span data-ttu-id="d41e9-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d41e9-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d41e9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d41e9-115">Remarks</span></span>

<span data-ttu-id="d41e9-116">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="d41e9-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d41e9-117">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="d41e9-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d41e9-118">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d41e9-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d41e9-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="d41e9-119">Examples</span></span>

<span data-ttu-id="d41e9-120">Nell'esempio JScript seguente viene usato un elemento DIV HTML, denominato MEDIANAME, per visualizzare il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="d41e9-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="d41e9-121">Il codice aggiorna il testo nel DIV con ogni occorrenza dell'evento **mediaChange** .</span><span class="sxs-lookup"><span data-stu-id="d41e9-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="d41e9-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d41e9-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="d41e9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d41e9-123">Requirements</span></span>



| <span data-ttu-id="d41e9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d41e9-124">Requirement</span></span> | <span data-ttu-id="d41e9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d41e9-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d41e9-126">Versione</span><span class="sxs-lookup"><span data-stu-id="d41e9-126">Version</span></span><br/> | <span data-ttu-id="d41e9-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="d41e9-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d41e9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d41e9-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d41e9-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d41e9-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d41e9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d41e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41e9-131">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="d41e9-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





