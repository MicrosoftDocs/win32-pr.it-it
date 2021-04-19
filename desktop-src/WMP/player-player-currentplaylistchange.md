---
title: Evento Player. CurrentPlaylistChange
description: L'evento CurrentPlaylistChange si verifica quando viene apportata una modifica all'interno della playlist corrente. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Media Player di Windows Event CurrentPlaylistChange
- Windows Event CurrentPlaylistChange Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326225"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="8274a-107">Evento Player. CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="8274a-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="8274a-108">L'evento **CurrentPlaylistChange** si verifica quando viene apportata una modifica all'interno della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="8274a-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="8274a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8274a-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="8274a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8274a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8274a-111">*change*</span><span class="sxs-lookup"><span data-stu-id="8274a-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="8274a-112">**Numero** (**Long**) che indica il tipo di modifica apportata alla playlist.</span><span class="sxs-lookup"><span data-stu-id="8274a-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="8274a-113">Vedere il *lettore*. Evento **PlaylistChange** per una tabella di valori possibili.</span><span class="sxs-lookup"><span data-stu-id="8274a-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8274a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8274a-114">Return value</span></span>

<span data-ttu-id="8274a-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8274a-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8274a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8274a-116">Remarks</span></span>

<span data-ttu-id="8274a-117">Questo evento non si verifica quando una playlist diversa diventa la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="8274a-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="8274a-118">Si verifica solo quando si verifica una modifica all'interno della playlist corrente, ad esempio un elemento multimediale aggiunto alla playlist.</span><span class="sxs-lookup"><span data-stu-id="8274a-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="8274a-119">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="8274a-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="8274a-120">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="8274a-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="8274a-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="8274a-121">Examples</span></span>

<span data-ttu-id="8274a-122">Nell'esempio JScript seguente viene aggiornato il testo in un elemento DIV HTML, denominato PlItems, per visualizzare i nomi degli elementi multimediali nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="8274a-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="8274a-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8274a-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="8274a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8274a-124">Requirements</span></span>



| <span data-ttu-id="8274a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8274a-125">Requirement</span></span> | <span data-ttu-id="8274a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8274a-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8274a-127">Versione</span><span class="sxs-lookup"><span data-stu-id="8274a-127">Version</span></span><br/> | <span data-ttu-id="8274a-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="8274a-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8274a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8274a-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="8274a-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8274a-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8274a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8274a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8274a-132">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="8274a-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8274a-133">**Player. currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="8274a-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="8274a-134">**Player. PlaylistChange**</span><span class="sxs-lookup"><span data-stu-id="8274a-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





