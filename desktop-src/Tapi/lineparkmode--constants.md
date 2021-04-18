---
description: Le \_ costanti del flag di bit LINEPARKMODE descrivono modi diversi di chiamate di parcheggio.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Costanti LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331254"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="7c7ca-103">\_Costanti LINEPARKMODE</span><span class="sxs-lookup"><span data-stu-id="7c7ca-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="7c7ca-104">Le costanti del flag di bit **LINEPARKMODE \_** descrivono modi diversi di chiamate di parcheggio.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="7c7ca-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ diretto**</span><span class="sxs-lookup"><span data-stu-id="7c7ca-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7c7ca-106">Specifica il Call Park diretto.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-106">Specifies directed call park.</span></span> <span data-ttu-id="7c7ca-107">L'indirizzo in cui deve essere parcheggiata la chiamata deve essere fornito all'opzione.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c7ca-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE non \_ indirizzato**</span><span class="sxs-lookup"><span data-stu-id="7c7ca-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7c7ca-109">Specifica il Call Park non indirizzato.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-109">Specifies nondirected call park.</span></span> <span data-ttu-id="7c7ca-110">L'indirizzo in cui viene parcheggiata la chiamata viene selezionato dall'opzione e fornito dal passaggio all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c7ca-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c7ca-111">Remarks</span></span>

<span data-ttu-id="7c7ca-112">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-112">No extensibility.</span></span> <span data-ttu-id="7c7ca-113">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="7c7ca-114">Le **\_ costanti LINEPARKMODE** vengono usate per il parcheggio di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="7c7ca-115">Consultare le funzionalità del dispositivo address di una linea per individuare la modalità del parco disponibile.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c7ca-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c7ca-116">Requirements</span></span>



| <span data-ttu-id="7c7ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c7ca-117">Requirement</span></span> | <span data-ttu-id="7c7ca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7c7ca-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7c7ca-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7c7ca-119">TAPI version</span></span><br/> | <span data-ttu-id="7c7ca-120">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7c7ca-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7c7ca-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c7ca-121">Header</span></span><br/>       | <dl> <span data-ttu-id="7c7ca-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c7ca-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




