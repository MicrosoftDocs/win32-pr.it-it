---
title: Visualizza timerInterval
description: L'attributo timerInterval specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- Visualizza Media Player Windows timerInterval
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325115"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="a5cce-104">Visualizza timerInterval</span><span class="sxs-lookup"><span data-stu-id="a5cce-104">VIEW.timerInterval</span></span>

<span data-ttu-id="a5cce-105">L'attributo **timerInterval** specifica o recupera l'intervallo, in millisecondi, in cui il timer genera eventi nel gestore eventi **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="a5cce-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="a5cce-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a5cce-106">Possible Values</span></span>

<span data-ttu-id="a5cce-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore predefinito di 1000.</span><span class="sxs-lookup"><span data-stu-id="a5cce-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="a5cce-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a5cce-108">Value</span></span>        | <span data-ttu-id="a5cce-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5cce-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="a5cce-110">0</span><span class="sxs-lookup"><span data-stu-id="a5cce-110">0</span></span>            | <span data-ttu-id="a5cce-111">L'evento timer non viene attivato.</span><span class="sxs-lookup"><span data-stu-id="a5cce-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="a5cce-112">50 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="a5cce-112">50 and above</span></span> | <span data-ttu-id="a5cce-113">Intervallo in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a5cce-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="a5cce-114">Qualsiasi valore inferiore a 50 (inclusi i numeri negativi, ma non incluso zero) genera un errore e viene mantenuto il valore precedente.</span><span class="sxs-lookup"><span data-stu-id="a5cce-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5cce-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5cce-115">Remarks</span></span>

<span data-ttu-id="a5cce-116">Questa operazione non viene eseguita automaticamente se non viene implementato alcun gestore eventi **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="a5cce-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="a5cce-117">In questo modo non si verifica alcun calo delle prestazioni, anche se il valore predefinito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a5cce-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5cce-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5cce-118">Requirements</span></span>



| <span data-ttu-id="a5cce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5cce-119">Requirement</span></span> | <span data-ttu-id="a5cce-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a5cce-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a5cce-121">Versione</span><span class="sxs-lookup"><span data-stu-id="a5cce-121">Version</span></span><br/> | <span data-ttu-id="a5cce-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a5cce-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5cce-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5cce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5cce-124">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="a5cce-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="a5cce-125">**Visualizza. OnTimer**</span><span class="sxs-lookup"><span data-stu-id="a5cce-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 





