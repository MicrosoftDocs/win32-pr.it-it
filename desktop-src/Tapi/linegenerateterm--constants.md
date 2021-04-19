---
description: Le \_ costanti del flag di bit LINEGENERATETERM descrivono le condizioni in base alle quali viene terminata la generazione di numeri o toni.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Costanti LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333545"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="5be15-103">\_Costanti LINEGENERATETERM</span><span class="sxs-lookup"><span data-stu-id="5be15-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="5be15-104">Le costanti del flag di bit **LINEGENERATETERM \_** descrivono le condizioni in base alle quali viene terminata la generazione di numeri o toni.</span><span class="sxs-lookup"><span data-stu-id="5be15-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="5be15-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**\_annullamento LINEGENERATETERM**</span><span class="sxs-lookup"><span data-stu-id="5be15-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5be15-106">La richiesta di generazione di numeri o toni è stata annullata dall'applicazione, da un'altra applicazione o dalla chiamata terminata.</span><span class="sxs-lookup"><span data-stu-id="5be15-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="5be15-107">Questo valore può essere restituito anche quando non è possibile completare la generazione di numeri o toni a causa di un errore interno del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="5be15-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5be15-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="5be15-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5be15-109">Il numero richiesto di cifre o i toni richiesti sono stati generati per la durata richiesta.</span><span class="sxs-lookup"><span data-stu-id="5be15-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5be15-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5be15-110">Remarks</span></span>

<span data-ttu-id="5be15-111">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="5be15-111">No extensibility.</span></span> <span data-ttu-id="5be15-112">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="5be15-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be15-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5be15-113">Requirements</span></span>



| <span data-ttu-id="5be15-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be15-114">Requirement</span></span> | <span data-ttu-id="5be15-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5be15-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5be15-116">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5be15-116">TAPI version</span></span><br/> | <span data-ttu-id="5be15-117">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5be15-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5be15-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5be15-118">Header</span></span><br/>       | <dl> <span data-ttu-id="5be15-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be15-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




