---
title: Rete. bufferingCount
description: La proprietà bufferingCount Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione della clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Media Player di Windows Network. bufferingCount
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326118"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="967c9-104">Rete. bufferingCount</span><span class="sxs-lookup"><span data-stu-id="967c9-104">Network.bufferingCount</span></span>

<span data-ttu-id="967c9-105">La proprietà **bufferingCount** Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione della clip.</span><span class="sxs-lookup"><span data-stu-id="967c9-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="967c9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="967c9-106">Syntax</span></span>

<span data-ttu-id="967c9-107">*Player*. *rete*. **bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="967c9-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="967c9-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="967c9-108">Possible Values</span></span>

<span data-ttu-id="967c9-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="967c9-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="967c9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="967c9-110">Remarks</span></span>

<span data-ttu-id="967c9-111">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="967c9-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="967c9-112">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="967c9-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="967c9-113">Il buffering si applica solo ai contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="967c9-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="967c9-114">Questa proprietà restituisce informazioni valide solo in fase di esecuzione quando il *lettore*. Viene impostata la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="967c9-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="967c9-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="967c9-115">Examples</span></span>

<span data-ttu-id="967c9-116">Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingCount** per visualizzare il numero di volte in cui si verifica il buffer durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="967c9-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="967c9-117">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "CB".</span><span class="sxs-lookup"><span data-stu-id="967c9-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="967c9-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="967c9-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="967c9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="967c9-119">Requirements</span></span>



| <span data-ttu-id="967c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="967c9-120">Requirement</span></span> | <span data-ttu-id="967c9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="967c9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="967c9-122">Versione</span><span class="sxs-lookup"><span data-stu-id="967c9-122">Version</span></span><br/> | <span data-ttu-id="967c9-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="967c9-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="967c9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="967c9-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="967c9-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967c9-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967c9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="967c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967c9-127">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="967c9-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="967c9-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="967c9-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





