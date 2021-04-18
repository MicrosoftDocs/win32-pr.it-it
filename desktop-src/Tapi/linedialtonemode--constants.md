---
description: Le \_ costanti del flag di bit LINEDIALTONEMODE descrivono tipi diversi di toni di composizione. Un tono di connessione speciale in genere porta un significato speciale (come per i messaggi in attesa).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Costanti LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325018"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="e9b0c-104">\_Costanti LINEDIALTONEMODE</span><span class="sxs-lookup"><span data-stu-id="e9b0c-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="e9b0c-105">Le costanti del flag di bit **LINEDIALTONEMODE \_** descrivono tipi diversi di toni di composizione.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="e9b0c-106">Un tono di connessione speciale in genere porta un significato speciale (come per i messaggi in attesa).</span><span class="sxs-lookup"><span data-stu-id="e9b0c-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="e9b0c-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ esterno**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-108">Si tratta di un segnale di connessione esterno (rete pubblica).</span><span class="sxs-lookup"><span data-stu-id="e9b0c-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b0c-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-110">Si tratta di un tono di connessione interna, come all'interno di un PBX.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b0c-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normale**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-112">Si tratta di un tono di linea normale, che in genere è un tono continuo.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b0c-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ speciale**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-114">Si tratta di un tono di connessione speciale che indica che è attualmente attiva una determinata condizione, nota con l'opzione o la rete.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="e9b0c-115">I toni della linea speciale usano in genere un tono interrotto.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="e9b0c-116">Come con un tono di linea normale, indica che l'opzione è pronta a ricevere il numero da comporre.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b0c-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-118">La modalità del tono di connessione non è disponibile e non viene riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b0c-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="e9b0c-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9b0c-120">La modalità del tono di connessione non è attualmente nota ma potrebbe essere nota in seguito.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9b0c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9b0c-121">Remarks</span></span>

<span data-ttu-id="e9b0c-122">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="e9b0c-123">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="e9b0c-124">Le **\_ costanti LINEDIALTONEMODE** vengono usate all'interno della struttura di dati [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) per una chiamata nello stato Dialtone.</span><span class="sxs-lookup"><span data-stu-id="e9b0c-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b0c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9b0c-125">Requirements</span></span>



| <span data-ttu-id="e9b0c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9b0c-126">Requirement</span></span> | <span data-ttu-id="e9b0c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e9b0c-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e9b0c-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e9b0c-128">TAPI version</span></span><br/> | <span data-ttu-id="e9b0c-129">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e9b0c-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e9b0c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9b0c-130">Header</span></span><br/>       | <dl> <span data-ttu-id="e9b0c-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b0c-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




