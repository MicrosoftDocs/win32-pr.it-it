---
title: Rete. bufferingProgress
description: La proprietà bufferingProgress recupera la percentuale di memorizzazione nel buffer completata.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Media Player di Windows Network. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326114"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="27e59-104">Rete. bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="27e59-104">Network.bufferingProgress</span></span>

<span data-ttu-id="27e59-105">La proprietà **bufferingProgress** recupera la percentuale di memorizzazione nel buffer completata.</span><span class="sxs-lookup"><span data-stu-id="27e59-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e59-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27e59-106">Syntax</span></span>

<span data-ttu-id="27e59-107">*Player*. *rete*. **bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="27e59-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="27e59-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="27e59-108">Possible Values</span></span>

<span data-ttu-id="27e59-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="27e59-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="27e59-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="27e59-110">Remarks</span></span>

<span data-ttu-id="27e59-111">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="27e59-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="27e59-112">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="27e59-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="27e59-113">Il buffering si applica solo ai contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="27e59-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="27e59-114">Questa proprietà restituisce informazioni valide solo in fase di esecuzione, quando il *lettore*. Viene impostata la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="27e59-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="27e59-115">Usare l'evento *Player*. \* \* \* \* buffering \* \* \* \* per determinare quando il buffering viene avviato o interrotto.</span><span class="sxs-lookup"><span data-stu-id="27e59-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="27e59-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="27e59-116">Examples</span></span>

<span data-ttu-id="27e59-117">Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingProgress** per visualizzare la percentuale di memorizzazione nel buffer completata.</span><span class="sxs-lookup"><span data-stu-id="27e59-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="27e59-118">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BP".</span><span class="sxs-lookup"><span data-stu-id="27e59-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="27e59-119">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="27e59-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="27e59-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="27e59-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="27e59-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27e59-121">Requirements</span></span>



| <span data-ttu-id="27e59-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27e59-122">Requirement</span></span> | <span data-ttu-id="27e59-123">Valore</span><span class="sxs-lookup"><span data-stu-id="27e59-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27e59-124">Versione</span><span class="sxs-lookup"><span data-stu-id="27e59-124">Version</span></span><br/> | <span data-ttu-id="27e59-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="27e59-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="27e59-126">DLL</span><span class="sxs-lookup"><span data-stu-id="27e59-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="27e59-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27e59-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e59-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27e59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e59-129">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="27e59-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="27e59-130">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="27e59-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="27e59-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="27e59-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





