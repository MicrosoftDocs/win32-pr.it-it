---
description: Le \_ costanti LINECALLTREATMENT elencano i trattamenti per le chiamate senza risposta o in attesa. Ad eccezione della convalida dei parametri di base, il trattamento delle chiamate è un pass-through lineare di TAPI al provider di servizi.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Costanti LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332725"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="6ab2b-104">\_Costanti LINECALLTREATMENT</span><span class="sxs-lookup"><span data-stu-id="6ab2b-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="6ab2b-105">Le **costanti \_ LINECALLTREATMENT** elencano i trattamenti per le chiamate senza risposta o in attesa.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="6ab2b-106">Ad eccezione della convalida dei parametri di base, il trattamento delle chiamate è un pass-through lineare di TAPI al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="6ab2b-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="6ab2b-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6ab2b-108">Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), la parte riceve un segnale occupato.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ab2b-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_musica LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="6ab2b-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6ab2b-110">Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), l'entità ascolta la musica.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ab2b-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ risponder**</span><span class="sxs-lookup"><span data-stu-id="6ab2b-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6ab2b-112">Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), l'entità riceve un segnale di riscontro.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ab2b-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ silenzioso**</span><span class="sxs-lookup"><span data-stu-id="6ab2b-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6ab2b-114">Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), la parte sente il silenzio.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ab2b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ab2b-115">Remarks</span></span>

<span data-ttu-id="6ab2b-116">Il valore 0x00000000 è riservato per indicare che il provider di servizi non supporta i trattamenti di chiamata.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="6ab2b-117">I valori nell'intervallo compreso tra 0x00000005 e 0x000000FF sono riservati per la definizione futura.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="6ab2b-118">I valori nell'intervallo compreso tra 0x00000100 e 0xFFFFFFFF sono riservati per l'assegnazione da parte dei provider di servizi e possono includere l'identificazione di selezioni musicali specifiche o annunci registrati.</span><span class="sxs-lookup"><span data-stu-id="6ab2b-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab2b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ab2b-119">Requirements</span></span>



| <span data-ttu-id="6ab2b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab2b-120">Requirement</span></span> | <span data-ttu-id="6ab2b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6ab2b-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6ab2b-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6ab2b-122">TAPI version</span></span><br/> | <span data-ttu-id="6ab2b-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6ab2b-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6ab2b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ab2b-124">Header</span></span><br/>       | <dl> <span data-ttu-id="6ab2b-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab2b-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




