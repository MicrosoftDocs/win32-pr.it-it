---
title: Rete. lostPackets
description: La proprietà lostPackets Recupera il numero di pacchetti persi.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Media Player di Windows Network. lostPackets
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328294"
---
# <a name="networklostpackets"></a><span data-ttu-id="fe57b-104">Rete. lostPackets</span><span class="sxs-lookup"><span data-stu-id="fe57b-104">Network.lostPackets</span></span>

<span data-ttu-id="fe57b-105">La proprietà **lostPackets** Recupera il numero di pacchetti persi.</span><span class="sxs-lookup"><span data-stu-id="fe57b-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe57b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe57b-106">Syntax</span></span>

<span data-ttu-id="fe57b-107">*Player*. *rete*. **lostPackets**</span><span class="sxs-lookup"><span data-stu-id="fe57b-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fe57b-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fe57b-108">Possible Values</span></span>

<span data-ttu-id="fe57b-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="fe57b-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe57b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe57b-110">Remarks</span></span>

<span data-ttu-id="fe57b-111">Questa proprietà è valida solo per i flussi multimediali e sarà uguale a zero quando si usa il protocollo HTTP, che è senza perdita di contenuti.</span><span class="sxs-lookup"><span data-stu-id="fe57b-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="fe57b-112">I pacchetti possono essere persi per diversi motivi, ad esempio il tipo e la qualità della connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="fe57b-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="fe57b-113">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="fe57b-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="fe57b-114">Non viene reimpostato se la riproduzione viene sospesa e riavviata.</span><span class="sxs-lookup"><span data-stu-id="fe57b-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="fe57b-115">Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="fe57b-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="fe57b-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe57b-116">Examples</span></span>

<span data-ttu-id="fe57b-117">Nell'esempio JScript seguente viene utilizzata la *rete*. **lostPackets** per visualizzare il numero totale di pacchetti persi durante la riproduzione quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="fe57b-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="fe57b-118">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "LP".</span><span class="sxs-lookup"><span data-stu-id="fe57b-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="fe57b-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fe57b-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="fe57b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe57b-120">Requirements</span></span>



| <span data-ttu-id="fe57b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe57b-121">Requirement</span></span> | <span data-ttu-id="fe57b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fe57b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe57b-123">Versione</span><span class="sxs-lookup"><span data-stu-id="fe57b-123">Version</span></span><br/> | <span data-ttu-id="fe57b-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fe57b-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fe57b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe57b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe57b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe57b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe57b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe57b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe57b-128">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="fe57b-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="fe57b-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="fe57b-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





