---
title: Player. fullScreen
description: La proprietà fullScreen Specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324982"
---
# <a name="playerfullscreen"></a><span data-ttu-id="fb483-104">Player. fullScreen</span><span class="sxs-lookup"><span data-stu-id="fb483-104">Player.fullScreen</span></span>

<span data-ttu-id="fb483-105">La proprietà **FullScreen** specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb483-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb483-106">Syntax</span></span>

<span data-ttu-id="fb483-107">*Player* . a **schermo intero**</span><span class="sxs-lookup"><span data-stu-id="fb483-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fb483-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fb483-108">Possible Values</span></span>

<span data-ttu-id="fb483-109">Questa proprietà è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fb483-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="fb483-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fb483-110">Value</span></span> | <span data-ttu-id="fb483-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb483-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="fb483-112">true</span><span class="sxs-lookup"><span data-stu-id="fb483-112">true</span></span>  | <span data-ttu-id="fb483-113">Il contenuto video viene riprodotto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="fb483-114">false</span><span class="sxs-lookup"><span data-stu-id="fb483-114">false</span></span> | <span data-ttu-id="fb483-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="fb483-115">Default.</span></span> <span data-ttu-id="fb483-116">Il contenuto video non viene riprodotto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb483-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb483-117">Remarks</span></span>

<span data-ttu-id="fb483-118">Per il corretto funzionamento della modalità a schermo intero quando si incorpora il controllo Media Player di Windows, l'area di visualizzazione del video deve avere un'altezza e una larghezza pari ad almeno un pixel.</span><span class="sxs-lookup"><span data-stu-id="fb483-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="fb483-119">Se **uiMode** è impostato su "mini" o "full", l'altezza del controllo deve essere 65 o superiore per ospitare l'area di visualizzazione video oltre all'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fb483-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="fb483-120">Se **uiMode** è impostato su "invisibile", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="fb483-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="fb483-121">Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".</span><span class="sxs-lookup"><span data-stu-id="fb483-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="fb483-122">Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse si sposta.</span><span class="sxs-lookup"><span data-stu-id="fb483-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="fb483-123">Dopo un breve intervallo di assenza del movimento del mouse, i controlli di trasporto sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="fb483-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="fb483-124">Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="fb483-125">**Nota**</span><span class="sxs-lookup"><span data-stu-id="fb483-125">**Note**</span></span>

<span data-ttu-id="fb483-126">Per visualizzare i controlli di trasporto in modalità schermo intero, è necessario il sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb483-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="fb483-127">Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player esce automaticamente dalla modalità schermo intero quando la riproduzione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="fb483-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="fb483-128">**Nota**</span><span class="sxs-lookup"><span data-stu-id="fb483-128">**Note**</span></span>

<span data-ttu-id="fb483-129">Assicurarsi sempre di informare l'utente come tornare dalla modalità a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="fb483-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="fb483-130">Examples</span></span>

<span data-ttu-id="fb483-131">Nell'esempio seguente viene creato un pulsante di input HTML che utilizza *Player*. **FullScreen** per passare un oggetto Player incorporato alla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fb483-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="fb483-132">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fb483-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="fb483-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb483-133">Requirements</span></span>



| <span data-ttu-id="fb483-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb483-134">Requirement</span></span> | <span data-ttu-id="fb483-135">Valore</span><span class="sxs-lookup"><span data-stu-id="fb483-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb483-136">Versione</span><span class="sxs-lookup"><span data-stu-id="fb483-136">Version</span></span><br/> | <span data-ttu-id="fb483-137">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fb483-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb483-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fb483-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb483-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb483-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb483-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb483-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb483-141">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="fb483-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





