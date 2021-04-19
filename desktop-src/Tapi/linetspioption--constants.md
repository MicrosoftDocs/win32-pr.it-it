---
description: Le \_ costanti LINETSPIOPTION descrivono l'ordine in cui i provider di servizi devono essere chiamati.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Costanti LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333540"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="b3c56-103">\_Costanti LINETSPIOPTION</span><span class="sxs-lookup"><span data-stu-id="b3c56-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="b3c56-104">Le **\_ costanti LINETSPIOPTION** descrivono l'ordine in cui i provider di servizi devono essere chiamati.</span><span class="sxs-lookup"><span data-stu-id="b3c56-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="b3c56-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**\_NONREENTRANT LINETSPIOPTION**</span><span class="sxs-lookup"><span data-stu-id="b3c56-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3c56-106">TAPI deve chiamare le funzioni in questo provider di servizi uno alla volta. deve attendere che ogni funzione restituisca (ma non per il completamento delle funzioni asincrone) prima di chiamare la stessa o un'altra funzione, nello stesso o in un altro thread, nello stesso o in un processore diverso.</span><span class="sxs-lookup"><span data-stu-id="b3c56-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3c56-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3c56-107">Requirements</span></span>



| <span data-ttu-id="b3c56-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c56-108">Requirement</span></span> | <span data-ttu-id="b3c56-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b3c56-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b3c56-110">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b3c56-110">TAPI version</span></span><br/> | <span data-ttu-id="b3c56-111">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b3c56-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b3c56-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3c56-112">Header</span></span><br/>       | <dl> <span data-ttu-id="b3c56-113"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c56-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




