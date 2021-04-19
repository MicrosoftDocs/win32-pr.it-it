---
description: Il messaggio TSPI LINE \_ CALLDEVSPECIFICFEATURE viene inviato alla funzione di callback LineEvent per notificare a TAPI gli eventi specifici del dispositivo che si verificano su una riga o un indirizzo.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Messaggio LINE_CALLDEVSPECIFICFEATURE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332255"
---
# <a name="line_calldevspecificfeature-message"></a><span data-ttu-id="95d53-103">\_Messaggio linea CALLDEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="95d53-103">LINE\_CALLDEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="95d53-104">Il messaggio TSPI **line \_ CALLDEVSPECIFICFEATURE** viene inviato alla funzione di callback [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) per notificare a TAPI gli eventi specifici del dispositivo che si verificano su una riga o un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="95d53-104">The TSPI **LINE\_CALLDEVSPECIFICFEATURE** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a line or address.</span></span> <span data-ttu-id="95d53-105">Il significato del messaggio e l'interpretazione del *dwParam1* tramite i parametri di *dwParam3* sono specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d53-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="95d53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95d53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d53-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="95d53-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-108">Handle di oggetto opaco TAPI al dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="95d53-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="95d53-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="95d53-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-110">Handle di oggetto opaco TAPI al dispositivo di chiamata.</span><span class="sxs-lookup"><span data-stu-id="95d53-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="95d53-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="95d53-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-112">RIGA del valore \_ CALLDEVSPECIFICFEATURE.</span><span class="sxs-lookup"><span data-stu-id="95d53-112">The value LINE\_CALLDEVSPECIFICFEATURE.</span></span>

</dd> <dt>

<span data-ttu-id="95d53-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="95d53-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-114">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d53-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="95d53-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="95d53-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-116">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d53-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="95d53-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="95d53-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="95d53-118">Specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d53-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d53-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="95d53-119">Remarks</span></span>

<span data-ttu-id="95d53-120">Il messaggio di **riga \_ CALLDEVSPECIFICFEATURE** viene utilizzato da un provider di servizi insieme alla funzione [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="95d53-120">The **LINE\_CALLDEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) function.</span></span> <span data-ttu-id="95d53-121">Il suo significato è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d53-121">Its meaning is device specific.</span></span>

<span data-ttu-id="95d53-122">TAPI invia il messaggio di [**riga \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) alle applicazioni in risposta alla ricezione di questo messaggio da un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="95d53-122">TAPI sends the [**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="95d53-123">I parametri *htLine* e *htCall* vengono convertiti nel *hCall* appropriato come parametro *hDevice* a livello di TAPI.</span><span class="sxs-lookup"><span data-stu-id="95d53-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="95d53-124">I parametri *dwParam1*, *dwParam2* e *dwParam3* vengono passati senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="95d53-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="95d53-125">Non esiste alcun messaggio direttamente corrispondente a livello di TAPI, sebbene questo messaggio sia molto simile alla riga \_ DEVSPECIFICFEATURE.</span><span class="sxs-lookup"><span data-stu-id="95d53-125">There is no directly corresponding message at the TAPI level, although this message is very similar to LINE\_DEVSPECIFICFEATURE.</span></span> <span data-ttu-id="95d53-126">A livello di TSPI, i messaggi relativi alle funzionalità specifiche del dispositivo vengono suddivisi tra gli eventi di Reporting sulle righe e sugli indirizzi e gli eventi di Reporting sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="95d53-126">At the TSPI level, the device-specific feature messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d53-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d53-127">Requirements</span></span>



| <span data-ttu-id="95d53-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d53-128">Requirement</span></span> | <span data-ttu-id="95d53-129">Valore</span><span class="sxs-lookup"><span data-stu-id="95d53-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="95d53-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="95d53-130">TAPI version</span></span><br/> | <span data-ttu-id="95d53-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="95d53-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="95d53-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95d53-132">Header</span></span><br/>       | <dl> <span data-ttu-id="95d53-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d53-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d53-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d53-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="95d53-135">[**LINEA \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95d53-135">[**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="95d53-136">**\_LINEDEVSPECIFICFEATURE TSPI**</span><span class="sxs-lookup"><span data-stu-id="95d53-136">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

