---
description: Il messaggio NEWCALL della riga TSPI \_ viene inviato alla funzione di callback LineEvent ogni volta che una nuova chiamata non originata da TAPI arriva su una riga aperta da TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Messaggio LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327987"
---
# <a name="line_newcall-message"></a><span data-ttu-id="b502d-103">\_Messaggio linea NEWCALL</span><span class="sxs-lookup"><span data-stu-id="b502d-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="b502d-104">Il messaggio **\_ NEWCALL della riga** TSPI viene inviato alla funzione di callback [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) ogni volta che una nuova chiamata non originata da TAPI arriva su una riga aperta da TAPI.</span><span class="sxs-lookup"><span data-stu-id="b502d-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="b502d-105">Deve essere il primo messaggio inviato in merito a tale chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="b502d-106">TAPI scrive l'handle opaco *htCall* nella posizione passata dal provider di servizi come *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="b502d-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="b502d-107">Ciò consente al provider di servizi di usare il valore *htCall* nei messaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="b502d-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b502d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b502d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b502d-109">*htLine*</span><span class="sxs-lookup"><span data-stu-id="b502d-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-110">Handle di oggetto opaco TAPI al dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="b502d-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="b502d-111">*htCall*</span><span class="sxs-lookup"><span data-stu-id="b502d-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b502d-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b502d-113">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="b502d-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-114">RIGA del valore \_ NEWCALL.</span><span class="sxs-lookup"><span data-stu-id="b502d-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="b502d-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b502d-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-116">Handle opaco del provider di servizi per la chiamata di tipo [**HDRVCALL**](hdrvline.md).</span><span class="sxs-lookup"><span data-stu-id="b502d-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="b502d-117">TAPI passa questo valore come parametro *hdCall* per identificare la chiamata nelle procedure successive richiamate per operare sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="b502d-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b502d-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-119">Puntatore di tipo LPHTAPICALL che punta a un [**HTAPICALL**](htapicall.md).</span><span class="sxs-lookup"><span data-stu-id="b502d-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="b502d-120">TAPI scrive l'handle opaco TAPI per la chiamata alla posizione indicata.</span><span class="sxs-lookup"><span data-stu-id="b502d-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="b502d-121">Il provider di servizi deve salvare questo valore e passarlo come parametro *htCall* per identificare la chiamata negli eventi successivi segnalati per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="b502d-122">Questo parametro può inoltre acquisire un valore **null** (vedere la sezione Osservazioni riportata di seguito).</span><span class="sxs-lookup"><span data-stu-id="b502d-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="b502d-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b502d-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b502d-124">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b502d-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b502d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b502d-125">Remarks</span></span>

<span data-ttu-id="b502d-126">Il provider di servizi deve inviare il messaggio di [**riga \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) come messaggio successivo per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="b502d-127">L'evento **line \_ NEWCALL** è insolito in quanto restituisce anche un valore al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="b502d-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="b502d-128">Questa funzione segnala le nuove chiamate che hanno origine nel provider di servizi (in ingresso, in uscita, avviate al telefono e così via) per cui TAPI e il provider di servizi non hanno ancora scambiato gli handle opachi.</span><span class="sxs-lookup"><span data-stu-id="b502d-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="b502d-129">Gli handle vengono scambiati in modo che TAPI e il provider di servizi possano successivamente effettuare richieste ed eventi di report che coinvolgono la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="b502d-130">Poiché queste nuove chiamate non sono necessariamente in ingresso, le chiamate possono essere inizialmente in qualsiasi stato, non necessariamente lo stato dell' *offerta* .</span><span class="sxs-lookup"><span data-stu-id="b502d-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="b502d-131">Se il provider di servizi viene avviato e rileva che una o più chiamate sono già attive sulla riga, informa TAPI con messaggi di **riga \_ NEWCALL** seguiti dai messaggi della [**riga \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) che indicano lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="b502d-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="b502d-132">Una nuova chiamata in uscita, avviata dal telefono da parte dell'utente, verrebbe segnalata con un messaggio di **riga \_ NEWCALL** e il messaggio di **riga iniziale \_ CALLSTATE** indicherebbe che la chiamata era in stato **Dialtone** (e quindi continua da qui).</span><span class="sxs-lookup"><span data-stu-id="b502d-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="b502d-133">Se il provider di servizi passa un numero elevato di chiamate a TAPI in un intervallo di tempo molto breve (durante lo stesso ciclo di interrupt), è possibile che TAPI venga sottoposta a backlog nell'elaborazione di tali chiamate.</span><span class="sxs-lookup"><span data-stu-id="b502d-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="b502d-134">Quando si verifica questo problema, TAPI segnala al provider di servizi di attendere un breve periodo di tempo prima di inviare ulteriori chiamate.</span><span class="sxs-lookup"><span data-stu-id="b502d-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="b502d-135">Segnala questo problema scrivendo un valore **null**, anziché un [**HTAPICALL**](htapicall.md)valido, nella posizione a cui punta il parametro *dwParam2* della **riga \_ NEWCALL**.</span><span class="sxs-lookup"><span data-stu-id="b502d-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="b502d-136">Ciò indica che il tentativo di elaborare l'handle di chiamata appena offerto non è stato eseguito correttamente, probabilmente a causa di un'impossibilità temporanea di allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="b502d-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="b502d-137">Il provider di servizi può rispondere eliminando la chiamata o inviando di nuovo il messaggio di **riga \_ NEWCALL** dopo un ritardo di pianificazione (durante il quale il provider di servizi deve cedere il processore per consentire a TAPI di elaborare altre azioni in sospeso).</span><span class="sxs-lookup"><span data-stu-id="b502d-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="b502d-138">In ogni caso, nessun altro messaggio relativo alla nuova chiamata può essere passato a TAPI fino a quando lo scambio di handle non riesce.</span><span class="sxs-lookup"><span data-stu-id="b502d-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="b502d-139">Quando la posizione a cui punta *dwParam2* acquisisce un valore non **null** , il provider di servizi sa che questo valore è un handle [**HTAPICALL**](htapicall.md) valido per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="b502d-140">Al livello TAPI non è associato alcun messaggio direttamente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b502d-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="b502d-141">Questo messaggio viene usato a livello di TSPI per introdurre in modo univoco e senza ambiguità una nuova chiamata in ingresso a TAPI e recuperare l'identificatore opaco TAPI per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b502d-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="b502d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b502d-142">Requirements</span></span>



| <span data-ttu-id="b502d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b502d-143">Requirement</span></span> | <span data-ttu-id="b502d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b502d-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b502d-145">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b502d-145">TAPI version</span></span><br/> | <span data-ttu-id="b502d-146">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b502d-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b502d-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b502d-147">Header</span></span><br/>       | <dl> <span data-ttu-id="b502d-148"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b502d-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b502d-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b502d-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="b502d-150">[**LINEA \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b502d-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b502d-151">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="b502d-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

