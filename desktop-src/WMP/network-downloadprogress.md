---
title: Rete. downloadProgress
description: La proprietà downloadProgress recupera la percentuale di download completato.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Media Player di Windows Network. downloadProgress
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326110"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="c391f-104">Rete. downloadProgress</span><span class="sxs-lookup"><span data-stu-id="c391f-104">Network.downloadProgress</span></span>

<span data-ttu-id="c391f-105">La proprietà **downloadProgress** recupera la percentuale di download completato.</span><span class="sxs-lookup"><span data-stu-id="c391f-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c391f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c391f-106">Syntax</span></span>

<span data-ttu-id="c391f-107">*Player*. *rete*. **downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="c391f-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c391f-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c391f-108">Possible Values</span></span>

<span data-ttu-id="c391f-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c391f-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c391f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c391f-110">Remarks</span></span>

<span data-ttu-id="c391f-111">Quando il controllo Windows Media Player è connesso a un file multimediale che può essere riprodotto e scaricato nello stesso momento, la proprietà **downloadProgress** restituisce la percentuale del file totale che è stato scaricato.</span><span class="sxs-lookup"><span data-stu-id="c391f-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="c391f-112">Questa funzionalità è attualmente supportata solo nei server Web.</span><span class="sxs-lookup"><span data-stu-id="c391f-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="c391f-113">I formati di file seguenti possono essere scaricati e riprodotti contemporaneamente:</span><span class="sxs-lookup"><span data-stu-id="c391f-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="c391f-114">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="c391f-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="c391f-115">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="c391f-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="c391f-116">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="c391f-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="c391f-117">MP3</span><span class="sxs-lookup"><span data-stu-id="c391f-117">MP3</span></span>
-   <span data-ttu-id="c391f-118">MPEG</span><span class="sxs-lookup"><span data-stu-id="c391f-118">MPEG</span></span>
-   <span data-ttu-id="c391f-119">WAV</span><span class="sxs-lookup"><span data-stu-id="c391f-119">WAV</span></span>
-   <span data-ttu-id="c391f-120">Alcuni file AVI</span><span class="sxs-lookup"><span data-stu-id="c391f-120">Some AVI files</span></span>

<span data-ttu-id="c391f-121">Usare il *lettore*. Evento di **buffering** per determinare l'inizio e la fine del download.</span><span class="sxs-lookup"><span data-stu-id="c391f-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="c391f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="c391f-122">Examples</span></span>

<span data-ttu-id="c391f-123">Nell'esempio JScript seguente viene utilizzata la *rete*. **downloadProgress** per visualizzare la percentuale di download completata.</span><span class="sxs-lookup"><span data-stu-id="c391f-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="c391f-124">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "DP".</span><span class="sxs-lookup"><span data-stu-id="c391f-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="c391f-125">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c391f-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="c391f-126">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c391f-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c391f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c391f-127">Requirements</span></span>



| <span data-ttu-id="c391f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c391f-128">Requirement</span></span> | <span data-ttu-id="c391f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c391f-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c391f-130">Versione</span><span class="sxs-lookup"><span data-stu-id="c391f-130">Version</span></span><br/> | <span data-ttu-id="c391f-131">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c391f-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c391f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c391f-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="c391f-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c391f-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c391f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c391f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c391f-135">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="c391f-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c391f-136">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="c391f-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





