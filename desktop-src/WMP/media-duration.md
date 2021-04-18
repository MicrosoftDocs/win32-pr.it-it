---
title: Media. durata
description: La proprietà Duration recupera la durata dell'elemento multimediale corrente in secondi.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331385"
---
# <a name="mediaduration"></a><span data-ttu-id="fe952-104">Media. durata</span><span class="sxs-lookup"><span data-stu-id="fe952-104">Media.duration</span></span>

<span data-ttu-id="fe952-105">La proprietà **Duration** recupera la durata dell'elemento multimediale corrente in secondi.</span><span class="sxs-lookup"><span data-stu-id="fe952-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe952-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe952-106">Syntax</span></span>

<span data-ttu-id="fe952-107">*Player*. *currentMedia*. **durata**</span><span class="sxs-lookup"><span data-stu-id="fe952-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fe952-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fe952-108">Possible Values</span></span>

<span data-ttu-id="fe952-109">Questa proprietà è un **numero** di sola lettura ( **Double**).</span><span class="sxs-lookup"><span data-stu-id="fe952-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe952-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe952-110">Remarks</span></span>

<span data-ttu-id="fe952-111">Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in *Player*. **currentMedia**, non può contenere un valore valido.</span><span class="sxs-lookup"><span data-stu-id="fe952-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="fe952-112">Per recuperare la durata per i file che non si trovano nella libreria dell'utente, è necessario attendere che Windows Media Player Apra il file; ovvero, il OpenState corrente deve essere uguale a MediaOpen.</span><span class="sxs-lookup"><span data-stu-id="fe952-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="fe952-113">Per verificarlo, è possibile gestire il *lettore*. Evento **OpenStateChange** o verificando periodicamente il valore di *Player*. **openState**.</span><span class="sxs-lookup"><span data-stu-id="fe952-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="fe952-114">Per le playlist, la durata di ogni elemento multimediale può essere recuperata quando viene aperto il singolo elemento multimediale, anziché quando viene aperta la playlist.</span><span class="sxs-lookup"><span data-stu-id="fe952-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="fe952-115">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="fe952-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="fe952-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fe952-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fe952-117">Nell'esempio JScript seguente viene usato il *supporto*. **durata** per visualizzare il tempo rimanente nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="fe952-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="fe952-118">Un elemento DIV HTML denominato RemTime Visualizza le informazioni.</span><span class="sxs-lookup"><span data-stu-id="fe952-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="fe952-119">Un timer HTML aggiorna il testo nell'elemento DIV ogni secondo.</span><span class="sxs-lookup"><span data-stu-id="fe952-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="fe952-120">Il codice JScript seguente avvia il timer:</span><span class="sxs-lookup"><span data-stu-id="fe952-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="fe952-121">Il codice JScript seguente arresta il timer:</span><span class="sxs-lookup"><span data-stu-id="fe952-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="fe952-122">Usare il *lettore*. Evento **PlayStateChange** con un'istruzione **Switch** per determinare quando avviare e arrestare il timer.</span><span class="sxs-lookup"><span data-stu-id="fe952-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="fe952-123">Il codice JScript seguente viene eseguito ogni volta che il timer chiama la funzione Update:</span><span class="sxs-lookup"><span data-stu-id="fe952-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="fe952-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe952-124">Requirements</span></span>



| <span data-ttu-id="fe952-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe952-125">Requirement</span></span> | <span data-ttu-id="fe952-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fe952-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe952-127">Versione</span><span class="sxs-lookup"><span data-stu-id="fe952-127">Version</span></span><br/> | <span data-ttu-id="fe952-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fe952-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fe952-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fe952-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe952-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe952-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe952-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe952-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe952-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="fe952-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="fe952-133">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="fe952-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="fe952-134">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="fe952-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="fe952-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fe952-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fe952-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fe952-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





