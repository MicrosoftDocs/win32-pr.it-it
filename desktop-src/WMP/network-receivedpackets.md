---
title: Rete. receivedPackets
description: La proprietà receivedPackets Recupera il numero di pacchetti ricevuti.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Media Player di Windows Network. receivedPackets
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331382"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="fc7ee-104">Rete. receivedPackets</span><span class="sxs-lookup"><span data-stu-id="fc7ee-104">Network.receivedPackets</span></span>

<span data-ttu-id="fc7ee-105">La proprietà **receivedPackets** Recupera il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7ee-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc7ee-106">Syntax</span></span>

<span data-ttu-id="fc7ee-107">*Player*. *rete*. **receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="fc7ee-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fc7ee-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fc7ee-108">Possible Values</span></span>

<span data-ttu-id="fc7ee-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="fc7ee-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7ee-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc7ee-110">Remarks</span></span>

<span data-ttu-id="fc7ee-111">Ogni volta che la riproduzione clip viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="fc7ee-112">Non viene reimpostato se la riproduzione del file viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="fc7ee-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="fc7ee-113">Examples</span></span>

<span data-ttu-id="fc7ee-114">Nell'esempio JScript seguente viene utilizzata la *rete*. **receivedPackets** per visualizzare il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="fc7ee-115">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "RP".</span><span class="sxs-lookup"><span data-stu-id="fc7ee-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="fc7ee-116">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="fc7ee-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fc7ee-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="fc7ee-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc7ee-118">Requirements</span></span>



| <span data-ttu-id="fc7ee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7ee-119">Requirement</span></span> | <span data-ttu-id="fc7ee-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fc7ee-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7ee-121">Versione</span><span class="sxs-lookup"><span data-stu-id="fc7ee-121">Version</span></span><br/> | <span data-ttu-id="fc7ee-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fc7ee-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fc7ee-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fc7ee-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc7ee-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc7ee-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7ee-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc7ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7ee-126">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="fc7ee-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





