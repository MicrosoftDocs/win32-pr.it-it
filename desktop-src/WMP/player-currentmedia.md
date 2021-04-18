---
title: Player. currentMedia
description: La proprietà currentMedia specifica o recupera l'oggetto multimediale corrente.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player. currentMedia Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328208"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="24fba-104">Player. currentMedia</span><span class="sxs-lookup"><span data-stu-id="24fba-104">Player.currentMedia</span></span>

<span data-ttu-id="24fba-105">La proprietà **currentMedia** specifica o recupera l'oggetto multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="24fba-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="24fba-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24fba-106">Syntax</span></span>

<span data-ttu-id="24fba-107">*Player* . **currentMedia**</span><span class="sxs-lookup"><span data-stu-id="24fba-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="24fba-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="24fba-108">Possible Values</span></span>

<span data-ttu-id="24fba-109">Questa proprietà è un oggetto multimediale di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="24fba-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24fba-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="24fba-110">Remarks</span></span>

<span data-ttu-id="24fba-111">Se le *Impostazioni*. la proprietà **autostart** è true, la riproduzione viene avviata automaticamente quando si imposta **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="24fba-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="24fba-112">Questa proprietà accetta un oggetto multimediale, che può essere acquisito tramite *playlist*. **elemento**.</span><span class="sxs-lookup"><span data-stu-id="24fba-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="24fba-113">Per caricare un elemento **multimediale** usando un nome di file, impostare la proprietà URL o usare **newMedia**.</span><span class="sxs-lookup"><span data-stu-id="24fba-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="24fba-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="24fba-114">Examples</span></span>

<span data-ttu-id="24fba-115">Nell'esempio JScript seguente viene recuperato il primo elemento multimediale nella libreria.</span><span class="sxs-lookup"><span data-stu-id="24fba-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="24fba-116">USA quindi **currentMedia** per rendere l'elemento multimediale recuperato l'elemento multimediale corrente e quindi per visualizzare il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="24fba-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="24fba-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="24fba-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="24fba-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24fba-118">Requirements</span></span>



| <span data-ttu-id="24fba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="24fba-119">Requirement</span></span> | <span data-ttu-id="24fba-120">Valore</span><span class="sxs-lookup"><span data-stu-id="24fba-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24fba-121">Versione</span><span class="sxs-lookup"><span data-stu-id="24fba-121">Version</span></span><br/> | <span data-ttu-id="24fba-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="24fba-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="24fba-123">DLL</span><span class="sxs-lookup"><span data-stu-id="24fba-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="24fba-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24fba-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24fba-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24fba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24fba-126">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="24fba-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="24fba-127">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="24fba-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="24fba-128">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="24fba-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="24fba-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="24fba-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="24fba-130">**Impostazioni. avvio automatico**</span><span class="sxs-lookup"><span data-stu-id="24fba-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





