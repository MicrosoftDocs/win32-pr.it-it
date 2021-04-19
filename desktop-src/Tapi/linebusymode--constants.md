---
description: Le \_ costanti del flag di bit LINEBUSYMODE descrivono segnali di occupato diversi che possono essere generati dall'opzione o dalla rete. Questi segnali di occupato indicano in genere che un'altra risorsa necessaria per effettuare una chiamata è attualmente in uso.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Costanti LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332900"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="7e9cb-104">\_Costanti LINEBUSYMODE</span><span class="sxs-lookup"><span data-stu-id="7e9cb-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="7e9cb-105">Le costanti del flag di bit **LINEBUSYMODE \_** descrivono segnali di occupato diversi che possono essere generati dall'opzione o dalla rete.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="7e9cb-106">Questi segnali di occupato indicano in genere che un'altra risorsa necessaria per effettuare una chiamata è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="7e9cb-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_stazione LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="7e9cb-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e9cb-108">Il segnale di occupato indica che la stazione dell'entità chiamata è occupata.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="7e9cb-109">Questa operazione viene in genere segnalata con un tono occupato *normale* .</span><span class="sxs-lookup"><span data-stu-id="7e9cb-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e9cb-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_trunk LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="7e9cb-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e9cb-111">Il segnale occupato indica che un tronco o un circuito è occupato.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="7e9cb-112">Questa operazione viene in genere segnalata con un tono di disponibilità *elevata* .</span><span class="sxs-lookup"><span data-stu-id="7e9cb-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e9cb-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7e9cb-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e9cb-114">La modalità specifica del segnale occupato è attualmente sconosciuta, ma potrebbe essere nota in seguito.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e9cb-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="7e9cb-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7e9cb-116">La modalità specifica del segnale occupato non è disponibile e non viene riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e9cb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e9cb-117">Remarks</span></span>

<span data-ttu-id="7e9cb-118">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="7e9cb-119">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="7e9cb-120">I segnali occupati possono essere inviati come segnali acustici o fuori banda.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="7e9cb-121">TAPI non presuppone il meccanismo di segnalazione specifico.</span><span class="sxs-lookup"><span data-stu-id="7e9cb-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e9cb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e9cb-122">Requirements</span></span>



| <span data-ttu-id="7e9cb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9cb-123">Requirement</span></span> | <span data-ttu-id="7e9cb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9cb-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7e9cb-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7e9cb-125">TAPI version</span></span><br/> | <span data-ttu-id="7e9cb-126">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7e9cb-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7e9cb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e9cb-127">Header</span></span><br/>       | <dl> <span data-ttu-id="7e9cb-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e9cb-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




