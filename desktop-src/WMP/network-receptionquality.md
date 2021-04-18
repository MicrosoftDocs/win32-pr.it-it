---
title: Rete. receptionQuality
description: La proprietà receptionQuality recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Media Player di Windows Network. receptionQuality
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331379"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="dc9f5-104">Rete. receptionQuality</span><span class="sxs-lookup"><span data-stu-id="dc9f5-104">Network.receptionQuality</span></span>

<span data-ttu-id="dc9f5-105">La proprietà **receptionQuality** recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9f5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc9f5-106">Syntax</span></span>

<span data-ttu-id="dc9f5-107">*Player*. *rete*. **receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="dc9f5-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="dc9f5-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="dc9f5-108">Possible Values</span></span>

<span data-ttu-id="dc9f5-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="dc9f5-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9f5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc9f5-110">Remarks</span></span>

<span data-ttu-id="dc9f5-111">Il numero di pacchetti ricevuti, persi e ripristinati durante il flusso viene monitorato una volta al secondo.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="dc9f5-112">**receptionQuality** è la percentuale di pacchetti non persi negli ultimi 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="dc9f5-113">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="dc9f5-114">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="dc9f5-115">Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata anche la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="dc9f5-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="dc9f5-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc9f5-116">Examples</span></span>

<span data-ttu-id="dc9f5-117">Nell'esempio JScript seguente viene utilizzata la *rete*. **receptionQuality** per visualizzare la percentuale dei pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="dc9f5-118">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "RQ".</span><span class="sxs-lookup"><span data-stu-id="dc9f5-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="dc9f5-119">Nell'esempio viene utilizzato un timer con un intervallo di 30 secondi per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="dc9f5-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="dc9f5-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="dc9f5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc9f5-121">Requirements</span></span>



| <span data-ttu-id="dc9f5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc9f5-122">Requirement</span></span> | <span data-ttu-id="dc9f5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dc9f5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9f5-124">Versione</span><span class="sxs-lookup"><span data-stu-id="dc9f5-124">Version</span></span><br/> | <span data-ttu-id="dc9f5-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="dc9f5-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dc9f5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9f5-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc9f5-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc9f5-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9f5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc9f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9f5-129">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="dc9f5-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="dc9f5-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="dc9f5-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





