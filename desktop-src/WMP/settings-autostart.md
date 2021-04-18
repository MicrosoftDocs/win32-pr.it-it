---
title: Impostazioni. avvio automatico
description: La proprietà AutoStart specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Impostazioni. avvio automatico di Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325139"
---
# <a name="settingsautostart"></a><span data-ttu-id="77fd1-104">Impostazioni. avvio automatico</span><span class="sxs-lookup"><span data-stu-id="77fd1-104">Settings.autoStart</span></span>

<span data-ttu-id="77fd1-105">La proprietà **autostart** specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.</span><span class="sxs-lookup"><span data-stu-id="77fd1-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="77fd1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77fd1-106">Syntax</span></span>

<span data-ttu-id="77fd1-107">Player. Settings. autostart</span><span class="sxs-lookup"><span data-stu-id="77fd1-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="77fd1-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="77fd1-108">Possible Values</span></span>

<span data-ttu-id="77fd1-109">Questa proprietà è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="77fd1-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="77fd1-110">Valore</span><span class="sxs-lookup"><span data-stu-id="77fd1-110">Value</span></span> | <span data-ttu-id="77fd1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77fd1-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="77fd1-112">true</span><span class="sxs-lookup"><span data-stu-id="77fd1-112">true</span></span>  | <span data-ttu-id="77fd1-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="77fd1-113">Default.</span></span> <span data-ttu-id="77fd1-114">L'elemento multimediale inizia la riproduzione automatica (vedere la sezione Osservazioni).</span><span class="sxs-lookup"><span data-stu-id="77fd1-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="77fd1-115">false</span><span class="sxs-lookup"><span data-stu-id="77fd1-115">false</span></span> | <span data-ttu-id="77fd1-116">L'elemento multimediale non inizia la riproduzione automatica.</span><span class="sxs-lookup"><span data-stu-id="77fd1-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="77fd1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="77fd1-117">Remarks</span></span>

<span data-ttu-id="77fd1-118">Se **autostart** è impostato su true, l'elemento multimediale inizierà a riprodurre quando il *lettore*. **URL**, *Player*. **currentPlaylist** o *Player*. **currentMedia** è impostato.</span><span class="sxs-lookup"><span data-stu-id="77fd1-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="77fd1-119">In caso contrario, non verrà avviata la riproduzione fino ai *controlli*. viene chiamato il metodo **Play** .</span><span class="sxs-lookup"><span data-stu-id="77fd1-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="77fd1-120">Poiché la proprietà di **avvio automatico** per la modalità completa di Windows Media Player può essere impostata a livello globale da eventi esterni (ad esempio il caricamento di un CD), non esiste alcun valore predefinito affidabile per le interfacce e i controlli del lettore remoto.</span><span class="sxs-lookup"><span data-stu-id="77fd1-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="77fd1-121">Questo perché il motore di riproduzione del lettore in modalità completa viene usato in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="77fd1-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="77fd1-122">È necessario impostare **avvio automatico** su false immediatamente prima di impostare *Player*. **URL**, *Player*. **currentPlaylist** o *Player*. **currentMedia** in interfacce e finestre Remote Media Player controlla se si desidera assicurarsi che la riproduzione dell'elemento multimediale non venga avviata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="77fd1-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="77fd1-123">Inoltre, a meno che non si imposti l' **avvio automatico** su true immediatamente prima di specificare un elemento multimediale, è consigliabile non fare affidamento su questa impostazione come sostituto per l'utilizzo dei *controlli*. metodo **Play** .</span><span class="sxs-lookup"><span data-stu-id="77fd1-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="77fd1-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="77fd1-124">Examples</span></span>

<span data-ttu-id="77fd1-125">Nell'esempio seguente viene creato un elemento CHECKBOX HTML che consente all'utente di specificare se il controllo Player riproduce automaticamente l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="77fd1-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="77fd1-126">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="77fd1-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="77fd1-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77fd1-127">Requirements</span></span>



| <span data-ttu-id="77fd1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="77fd1-128">Requirement</span></span> | <span data-ttu-id="77fd1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="77fd1-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77fd1-130">Versione</span><span class="sxs-lookup"><span data-stu-id="77fd1-130">Version</span></span><br/> | <span data-ttu-id="77fd1-131">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="77fd1-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="77fd1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="77fd1-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="77fd1-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77fd1-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77fd1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77fd1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77fd1-135">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="77fd1-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="77fd1-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="77fd1-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="77fd1-137">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="77fd1-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





