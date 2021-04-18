---
description: Le \_ costanti LINECALLPARAMFLAGS descrivono diversi flag di stato relativi a una chiamata.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Costanti LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324881"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="c4de8-103">\_Costanti LINECALLPARAMFLAGS</span><span class="sxs-lookup"><span data-stu-id="c4de8-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="c4de8-104">Le **costanti \_ LINECALLPARAMFLAGS** descrivono diversi flag di stato relativi a una chiamata.</span><span class="sxs-lookup"><span data-stu-id="c4de8-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="c4de8-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**\_ID blocco LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-106">L'identità del mittente deve essere nascosta (ID chiamante del blocco).</span><span class="sxs-lookup"><span data-stu-id="c4de8-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**\_DESTOFFHOOK LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-108">Il telefono della parte chiamata dovrebbe essere Offhook automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c4de8-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="c4de8-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-110">La chiamata deve essere originata su un aspetto di chiamata inattiva e non partecipare a una chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="c4de8-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="c4de8-111">Quando si usa la funzione [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , se il \_ valore di inattività LINECALLPARAMFLAGS non è impostato ed è presente una chiamata esistente sulla riga, la funzione interrompe la chiamata esistente, se necessario, per eseguire la nuova chiamata.</span><span class="sxs-lookup"><span data-stu-id="c4de8-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="c4de8-112">Se non è presente alcuna chiamata esistente, la funzione effettua la nuova chiamata come specificato.</span><span class="sxs-lookup"><span data-stu-id="c4de8-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**\_NOHOLDCONFERENCE LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-114">Questo bit viene usato solo in combinazione con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) e [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span><span class="sxs-lookup"><span data-stu-id="c4de8-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="c4de8-115">L'indirizzo da usare per la conferenza con la chiamata corrente è specificato nel membro **targetAddress** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="c4de8-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c4de8-116">La chiamata di consultazione non consente di creare fisicamente un tono di connessione dal commutino, ma passa attraverso diversi Stati di definizione della chiamata (ad esempio, la composizione, l'esecuzione).</span><span class="sxs-lookup"><span data-stu-id="c4de8-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="c4de8-117">Quando la chiamata di consultazione raggiunge lo stato connesso, la conferenza viene stabilita automaticamente; la chiamata originale, che era rimasta nello stato connesso, entra nello stato di conferenza; la chiamata di consultazione entra nello stato di conferenza; il hConfCall entra nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="c4de8-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="c4de8-118">Se la chiamata di consultazione ha esito negativo (entra nello stato disconnesso seguito da Idle), il hConfCall entra nello stato inattivo e la chiamata originale (che potrebbe essere stata una conferenza esistente, nel caso di **linePrepareAddToConference**) rimane nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="c4de8-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="c4de8-119">L'entità o le parti originali non percepiscono mai che la chiamata è stata mantenuta.</span><span class="sxs-lookup"><span data-stu-id="c4de8-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="c4de8-120">Questa funzionalità viene spesso usata per aggiungere un supervisore a una chiamata dell'agente ACD quando necessario per monitorare le interazioni con un chiamante irato.</span><span class="sxs-lookup"><span data-stu-id="c4de8-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**\_ONESTEPTRANSFER LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-122">Questo bit viene usato solo in combinazione con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="c4de8-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="c4de8-123">Combina il funzionamento di **lineSetupTransfer** seguito da [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) nella chiamata di consultazione in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="c4de8-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="c4de8-124">L'indirizzo da comporre viene specificato nel membro **targetAddress** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="c4de8-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c4de8-125">La chiamata originale viene posizionata nello stato *onholdpendingtransfer* , come se **lineSetupTransfer** venisse chiamata normalmente e la chiamata di consultazione viene stabilita normalmente.</span><span class="sxs-lookup"><span data-stu-id="c4de8-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="c4de8-126">L'applicazione deve comunque chiamare [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) per influire sul trasferimento.</span><span class="sxs-lookup"><span data-stu-id="c4de8-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="c4de8-127">Questa funzionalità viene spesso utilizzata quando si richiama un trasferimento da un server tramite un collegamento di controllo delle chiamate di terze parti, perché tali collegamenti spesso non supportano il normale processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="c4de8-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**\_ORIGOFFHOOK LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-129">Il telefono dell'originatore dovrebbe essere Offhook automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c4de8-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**\_PREDICTIVEDIAL LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-131">Questo bit viene usato solo quando si effettua una chiamata su un indirizzo con funzionalità di composizione predittiva (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER è on nel membro **DwAddrCapFlags** in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="c4de8-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="c4de8-132">Il bit deve essere attivato per abilitare l'avanzamento della chiamata avanzata e/o le funzionalità di monitoraggio dei dispositivi multimediali del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4de8-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="c4de8-133">Se questo bit non è impostato su on, la chiamata verrà effettuata senza lo stato di avanzamento della chiamata o il monitoraggio del tipo di supporto e non verrà avviato alcun trasferimento automatico in base allo stato di chiamata.</span><span class="sxs-lookup"><span data-stu-id="c4de8-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4de8-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**\_sicurezza LINECALLPARAMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4de8-135">La chiamata deve essere configurata come protetta.</span><span class="sxs-lookup"><span data-stu-id="c4de8-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4de8-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4de8-136">Remarks</span></span>

<span data-ttu-id="c4de8-137">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="c4de8-137">No extensibility.</span></span> <span data-ttu-id="c4de8-138">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="c4de8-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4de8-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4de8-139">Requirements</span></span>



| <span data-ttu-id="c4de8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4de8-140">Requirement</span></span> | <span data-ttu-id="c4de8-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c4de8-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c4de8-142">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c4de8-142">TAPI version</span></span><br/> | <span data-ttu-id="c4de8-143">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c4de8-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c4de8-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4de8-144">Header</span></span><br/>       | <dl> <span data-ttu-id="c4de8-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4de8-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4de8-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4de8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4de8-147">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="c4de8-148">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="c4de8-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="c4de8-149">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="c4de8-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="c4de8-150">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="c4de8-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="c4de8-151">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="c4de8-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="c4de8-152">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="c4de8-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="c4de8-153">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="c4de8-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="c4de8-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="c4de8-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




