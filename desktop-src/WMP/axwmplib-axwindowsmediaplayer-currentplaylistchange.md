---
title: Evento CurrentPlaylistChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentPlaylistChange si verifica quando viene apportata una modifica all'interno della playlist corrente. | Evento CurrentPlaylistChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Evento CurrentPlaylistChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324108"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e046f-105">Evento CurrentPlaylistChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="e046f-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e046f-106">L'evento CurrentPlaylistChange si verifica quando viene apportata una modifica all'interno della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e046f-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="e046f-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="e046f-107">Event Data</span></span>

<span data-ttu-id="e046f-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CurrentPlaylistChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="e046f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="e046f-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="e046f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="e046f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e046f-110">Property</span></span> | <span data-ttu-id="e046f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e046f-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e046f-112">change (modifica)</span><span class="sxs-lookup"><span data-stu-id="e046f-112">change</span></span>   | <span data-ttu-id="e046f-113">Valore di enumerazione WMPLib. WMPPlaylistChangeEventTypeAn che indica il tipo di modifica apportata alla playlist.</span><span class="sxs-lookup"><span data-stu-id="e046f-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e046f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e046f-114">Remarks</span></span>

<span data-ttu-id="e046f-115">Questo evento non si verifica quando una playlist diversa diventa la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e046f-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="e046f-116">Si verifica solo quando si verifica una modifica all'interno della playlist corrente, ad esempio un elemento multimediale aggiunto alla playlist.</span><span class="sxs-lookup"><span data-stu-id="e046f-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="e046f-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e046f-117">Examples</span></span>

<span data-ttu-id="e046f-118">Nell'esempio seguente vengono visualizzati i nomi di tutti gli elementi multimediali nella playlist corrente in risposta all'evento CurrentPlaylistChange.</span><span class="sxs-lookup"><span data-stu-id="e046f-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="e046f-119">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="e046f-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e046f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e046f-120">Requirements</span></span>



| <span data-ttu-id="e046f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e046f-121">Requirement</span></span> | <span data-ttu-id="e046f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e046f-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e046f-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e046f-123">Version</span></span><br/>   | <span data-ttu-id="e046f-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e046f-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e046f-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e046f-125">Namespace</span></span><br/> | <span data-ttu-id="e046f-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e046f-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e046f-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="e046f-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e046f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e046f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e046f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e046f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e046f-130">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e046f-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e046f-131">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e046f-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e046f-132">**Evento AxWindowsMediaPlayer. PlaylistChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e046f-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="e046f-133">**WMPPlaylistChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="e046f-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





