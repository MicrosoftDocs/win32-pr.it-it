---
title: Rete. maxBandwidth
description: La proprietà maxBandwidth specifica o recupera la larghezza di banda massima consentita.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Media Player di Windows Network. maxBandwidth
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324381"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="e2222-104">Rete. maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="e2222-104">Network.maxBandwidth</span></span>

<span data-ttu-id="e2222-105">La proprietà **maxBandwidth** specifica o recupera la larghezza di banda massima consentita.</span><span class="sxs-lookup"><span data-stu-id="e2222-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2222-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2222-106">Syntax</span></span>

<span data-ttu-id="e2222-107">*Player*. *rete*. **maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="e2222-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e2222-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e2222-108">Possible Values</span></span>

<span data-ttu-id="e2222-109">Questa proprietà è un **numero** di lettura/scrittura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e2222-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2222-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2222-110">Remarks</span></span>

<span data-ttu-id="e2222-111">Nessun valore predefinito per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2222-111">This property has no default value.</span></span> <span data-ttu-id="e2222-112">Il valore può essere specificato durante la riproduzione di Windows Media Player, ma la modifica non verrà applicata fino a quando l'elemento multimediale corrente non viene rilasciato aprendone un altro o chiamando *Player*. **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="e2222-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="e2222-113">Windows Media Player tenta di ottenere la massima larghezza di banda possibile.</span><span class="sxs-lookup"><span data-stu-id="e2222-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="e2222-114">Solo nel caso del valore impostato, si verificherà una riduzione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="e2222-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="e2222-115">Questa impostazione è utile per ridurre la quantità di larghezza di banda usata, in particolare nel caso di un flusso a più velocità in bit (MBR).</span><span class="sxs-lookup"><span data-stu-id="e2222-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="e2222-116">Un flusso MBR contiene più flussi con velocità in bit diverse.</span><span class="sxs-lookup"><span data-stu-id="e2222-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="e2222-117">In alcuni casi, può essere utile usare un flusso con una velocità in bit inferiore a quella richiesta dal client.</span><span class="sxs-lookup"><span data-stu-id="e2222-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="e2222-118">In questo caso, l'impostazione della proprietà **maxBandwidth** consente di selezionare un flusso a velocità in bit inferiore.</span><span class="sxs-lookup"><span data-stu-id="e2222-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="e2222-119">Ad esempio, un flusso MBR può includere flussi codificati a 20 kilobit al secondo (Kbps), 37 kbps e 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="e2222-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="e2222-120">Se si imposta la proprietà **maxBandwidth** su 50.000 (50 Kbps), si selezionerà il flusso 37 Kbps anziché il flusso da 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="e2222-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2222-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2222-121">Requirements</span></span>



| <span data-ttu-id="e2222-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2222-122">Requirement</span></span> | <span data-ttu-id="e2222-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e2222-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2222-124">Versione</span><span class="sxs-lookup"><span data-stu-id="e2222-124">Version</span></span><br/> | <span data-ttu-id="e2222-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e2222-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e2222-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e2222-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2222-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2222-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2222-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2222-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2222-129">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="e2222-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="e2222-130">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="e2222-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





