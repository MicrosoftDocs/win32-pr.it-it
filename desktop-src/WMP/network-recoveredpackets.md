---
title: Rete. recoveredPackets
description: La proprietà recoveredPackets Recupera il numero di pacchetti ripristinati.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Media Player di Windows Network. recoveredPackets
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328714"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="4049e-104">Rete. recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="4049e-104">Network.recoveredPackets</span></span>

<span data-ttu-id="4049e-105">La proprietà **recoveredPackets** Recupera il numero di pacchetti ripristinati.</span><span class="sxs-lookup"><span data-stu-id="4049e-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="4049e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4049e-106">Syntax</span></span>

<span data-ttu-id="4049e-107">*Player*. *rete*. **recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="4049e-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4049e-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="4049e-108">Possible Values</span></span>

<span data-ttu-id="4049e-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4049e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4049e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4049e-110">Remarks</span></span>

<span data-ttu-id="4049e-111">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="4049e-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="4049e-112">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="4049e-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="4049e-113">Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata anche la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="4049e-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="4049e-114">Sarà uguale a zero quando si usa il protocollo HTTP, che è lossless.</span><span class="sxs-lookup"><span data-stu-id="4049e-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="4049e-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="4049e-115">Examples</span></span>

<span data-ttu-id="4049e-116">Nell'esempio JScript seguente viene utilizzata la *rete*. **recoveredPackets** per visualizzare il numero di pacchetti ripristinati.</span><span class="sxs-lookup"><span data-stu-id="4049e-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="4049e-117">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "PR".</span><span class="sxs-lookup"><span data-stu-id="4049e-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="4049e-118">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4049e-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="4049e-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4049e-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="4049e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4049e-120">Requirements</span></span>



| <span data-ttu-id="4049e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4049e-121">Requirement</span></span> | <span data-ttu-id="4049e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4049e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4049e-123">Versione</span><span class="sxs-lookup"><span data-stu-id="4049e-123">Version</span></span><br/> | <span data-ttu-id="4049e-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="4049e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4049e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4049e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4049e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4049e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4049e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4049e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4049e-128">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="4049e-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4049e-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="4049e-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





