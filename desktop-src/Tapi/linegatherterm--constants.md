---
description: Le \_ costanti del flag di bit LINEGATHERTERM descrivono le condizioni in base alle quali viene terminata la raccolta dei numeri memorizzati nel buffer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Costanti LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333546"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="f4708-103">\_Costanti LINEGATHERTERM</span><span class="sxs-lookup"><span data-stu-id="f4708-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="f4708-104">Le costanti del flag di bit **LINEGATHERTERM \_** descrivono le condizioni in base alle quali viene terminata la raccolta dei numeri memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="f4708-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="f4708-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**\_BUFFERFULL LINEGATHERTERM**</span><span class="sxs-lookup"><span data-stu-id="f4708-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4708-106">Il numero di cifre richiesto è stato raccolto.</span><span class="sxs-lookup"><span data-stu-id="f4708-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="f4708-107">Il buffer è pieno.</span><span class="sxs-lookup"><span data-stu-id="f4708-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4708-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**\_annullamento LINEGATHERTERM**</span><span class="sxs-lookup"><span data-stu-id="f4708-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4708-109">La richiesta è stata annullata dall'applicazione, da un'altra applicazione o perché la chiamata è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="f4708-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4708-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**\_FIRSTTIMEOUT LINEGATHERTERM**</span><span class="sxs-lookup"><span data-stu-id="f4708-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4708-111">Timeout della prima cifra scaduto.</span><span class="sxs-lookup"><span data-stu-id="f4708-111">The first digit timeout expired.</span></span> <span data-ttu-id="f4708-112">Il buffer non contiene cifre.</span><span class="sxs-lookup"><span data-stu-id="f4708-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4708-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**intertimeout LINEGATHERTERM \_**</span><span class="sxs-lookup"><span data-stu-id="f4708-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4708-114">Timeout tra cifre scaduto.</span><span class="sxs-lookup"><span data-stu-id="f4708-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="f4708-115">Il buffer contiene almeno una cifra.</span><span class="sxs-lookup"><span data-stu-id="f4708-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4708-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**\_TERMDIGIT LINEGATHERTERM**</span><span class="sxs-lookup"><span data-stu-id="f4708-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4708-117">Una delle cifre di terminazione corrisponde a una cifra ricevuta.</span><span class="sxs-lookup"><span data-stu-id="f4708-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="f4708-118">La cifra di terminazione corrispondente è l'ultima cifra nel buffer.</span><span class="sxs-lookup"><span data-stu-id="f4708-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4708-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4708-119">Remarks</span></span>

<span data-ttu-id="f4708-120">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="f4708-120">No extensibility.</span></span> <span data-ttu-id="f4708-121">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f4708-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4708-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4708-122">Requirements</span></span>



| <span data-ttu-id="f4708-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4708-123">Requirement</span></span> | <span data-ttu-id="f4708-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f4708-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f4708-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f4708-125">TAPI version</span></span><br/> | <span data-ttu-id="f4708-126">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f4708-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f4708-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4708-127">Header</span></span><br/>       | <dl> <span data-ttu-id="f4708-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4708-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




