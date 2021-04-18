---
description: Le \_ costanti del flag di bit LINETERMMODE descrivono i diversi tipi di eventi su una linea telefonica che possono essere indirizzati a un dispositivo terminale.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Costanti LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326879"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="ec1cd-103">\_Costanti LINETERMMODE</span><span class="sxs-lookup"><span data-stu-id="ec1cd-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="ec1cd-104">Le costanti del flag di bit **LINETERMMODE \_** descrivono i diversi tipi di eventi su una linea telefonica che possono essere indirizzati a un dispositivo terminale.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="ec1cd-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_pulsanti LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-106">Si tratta di eventi di pressione del pulsante inviati dal terminale alla riga.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**\_visualizzazione LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-108">Vengono visualizzate le informazioni inviate dalla riga al terminale.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**\_HOOKSWITCH LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-110">Si tratta di eventi hookswitch inviati dal terminale alla riga.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lampade LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-112">Si tratta di eventi Lamp inviati dalla riga al terminale.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**\_MEDIABIDIRECT LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-114">Si tratta del flusso multimediale bidirezionale associato a una chiamata sulla riga e sul terminale.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="ec1cd-115">Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata non può essere controllato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**\_MEDIAFROMLINE LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-117">Si tratta del flusso multimediale unidirezionale dalla riga al terminale associato a una chiamata sulla riga.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="ec1cd-118">Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**\_MEDIATOLINE LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-120">Si tratta del flusso multimediale unidirezionale dal terminale alla riga associata a una chiamata sulla riga.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="ec1cd-121">Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec1cd-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ Ringer**</span><span class="sxs-lookup"><span data-stu-id="ec1cd-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec1cd-123">Si tratta di informazioni di controllo suoneria inviate dal passaggio al terminale.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec1cd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec1cd-124">Remarks</span></span>

<span data-ttu-id="ec1cd-125">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-125">No extensibility.</span></span> <span data-ttu-id="ec1cd-126">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="ec1cd-127">Queste costanti descrivono le classi di flussi di controllo e di informazioni che possono essere indirizzate direttamente tra un dispositivo a linee e un dispositivo Terminal (ad esempio un set di telefono).</span><span class="sxs-lookup"><span data-stu-id="ec1cd-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1cd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec1cd-128">Requirements</span></span>



| <span data-ttu-id="ec1cd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec1cd-129">Requirement</span></span> | <span data-ttu-id="ec1cd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ec1cd-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ec1cd-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-131">TAPI version</span></span><br/> | <span data-ttu-id="ec1cd-132">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ec1cd-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ec1cd-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec1cd-133">Header</span></span><br/>       | <dl> <span data-ttu-id="ec1cd-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec1cd-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 




