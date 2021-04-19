---
description: Le \_ costanti del flag di bit LINEADDRCAPFLAGS vengono usate nel membro dwAddrCapFlags della struttura di dati LINEADDRESSCAPS per descrivere diverse funzionalità di indirizzi booleani.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Costanti LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326622"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="de105-103">\_Costanti LINEADDRCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="de105-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="de105-104">Le  \_ costanti del flag di bit LINEADDRCAPFLAGS vengono usate nel membro **dwAddrCapFlags** della struttura di dati [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per descrivere diverse funzionalità di indirizzi booleani.</span><span class="sxs-lookup"><span data-stu-id="de105-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="de105-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**\_ACCEPTTOALERT LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-106">**True** se è necessario accettare una chiamata all'offerta usando [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) per avviare l'invio di avvisi agli utenti a entrambe le estremità della chiamata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="de105-107">Questa operazione viene in genere usata solo con ISDN.</span><span class="sxs-lookup"><span data-stu-id="de105-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**\_ACDGROUP LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-109">L'indirizzo supporta i [gruppi ACD](about-call-center-controls.md#acd-group-object) in relazione alle operazioni del Call Center.</span><span class="sxs-lookup"><span data-stu-id="de105-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="de105-110">Per ulteriori informazioni sui gruppi ACD, vedere informazioni [sui controlli del Call Center](./about-call-center-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="de105-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**\_AUTORECONNECT LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-112">Specifica se l'eliminazione di una chiamata di consultazione si riconnette automaticamente alla chiamata in attesa di consultazione.</span><span class="sxs-lookup"><span data-stu-id="de105-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="de105-113">**True** se la riconnessione viene eseguita automaticamente; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**\_BLOCKIDDEFAULT LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-115">Specifica se per impostazione predefinita la rete invia o blocca le informazioni relative all'ID chiamante quando si effettua una chiamata su questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="de105-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="de105-116">Se **true**, le informazioni sull'identificatore sono bloccate per impostazione predefinita; Se **false**, le informazioni sull'identificatore vengono trasmesse per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="de105-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**\_BLOCKIDOVERRIDE LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-118">Specifica se è possibile eseguire l'override dell'impostazione predefinita per l'invio o il blocco di informazioni sull'ID chiamante per ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="de105-119">Se **true**, è possibile eseguire l'override di. Se **false**, non è possibile eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="de105-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**\_COMPLETIONID LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-121">Specifica se gli identificatori di completamento restituiti da [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) sono utili e univoci.</span><span class="sxs-lookup"><span data-stu-id="de105-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="de105-122">**True** se utile; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**\_CONFDROP LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-124">**True** se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) in un padre di chiamata di conferenza ha anche l'effetto collaterale dell'eliminazione (ovvero la disconnessione) delle altre parti coinvolte nella chiamata di conferenza; **False** se l'eliminazione di una chiamata di conferenza consente ancora alle altre parti di comunicare tra loro.</span><span class="sxs-lookup"><span data-stu-id="de105-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**\_CONFERENCEHELD LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-126">Specifica se è possibile eseguire la conferenza a una chiamata a.</span><span class="sxs-lookup"><span data-stu-id="de105-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="de105-127">Spesso è possibile aggiungere a come chiamata per la conferenza solo le chiamate su una richiesta di consultazione.</span><span class="sxs-lookup"><span data-stu-id="de105-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**\_CONFERENCEMAKE LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-129">Specifica se è possibile stabilire una chiamata completamente nuova da utilizzare come chiamata di consultazione (da aggiungere) alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="de105-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**\_DESTOFFHOOK LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-131">Specifica se il telefono dell'entità chiamata può essere forzato automaticamente Offhook quando si effettuano chiamate.</span><span class="sxs-lookup"><span data-stu-id="de105-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS con \_ connessione**</span><span class="sxs-lookup"><span data-stu-id="de105-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-133">Specifica se è possibile comporre un indirizzo di destinazione in questo indirizzo per effettuare una chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="de105-134">**True** se è necessario comporre un indirizzo di destinazione. **False** se l'indirizzo di destinazione è fisso (come con un "telefono caldo").</span><span class="sxs-lookup"><span data-stu-id="de105-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**\_FWDBUSYNAADDR LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-136">Specifica se l'invio della chiamata per l'attività di occupato e per nessuna risposta può utilizzare indirizzi di inoltri diversi.</span><span class="sxs-lookup"><span data-stu-id="de105-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="de105-137">Questo flag è significativo solo se l'operazione di invio è occupata e per nessuna risposta può essere controllata separatamente.</span><span class="sxs-lookup"><span data-stu-id="de105-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="de105-138">Questo flag è **true** se l'invio di occupato e per nessuna risposta può utilizzare indirizzi di destinazione diversi. in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**\_FWDCONSULT LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-140">Specifica se l'invio della chiamata implica la creazione di una chiamata di consultazione.</span><span class="sxs-lookup"><span data-stu-id="de105-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**\_FWDINTEXTADDR LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-142">Specifica se le chiamate interne ed esterne possono essere indirizzate a indirizzi di inoltri diversi.</span><span class="sxs-lookup"><span data-stu-id="de105-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="de105-143">Questo flag è significativo solo se l'invio di chiamate interne ed esterne può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="de105-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="de105-144">Questo flag è **true** se è possibile inviare chiamate interne ed esterne a indirizzi di destinazione diversi. in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**\_FWDNUMRINGS LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-146">Specifica se è possibile specificare il numero di anelli per una risposta No quando si inviano chiamate senza risposta.</span><span class="sxs-lookup"><span data-stu-id="de105-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="de105-147">Se **true**, l'intervallo valido viene fornito nei membri **dwMinFwdNumRings** e **dwMaxFwdNumRings** della struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="de105-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**\_FWDSTATUSVALID LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-149">Specifica se lo stato di avanzamento nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) per questo indirizzo è valido o se è al massimo una "stima migliore", dato l'assenza di una conferma accurata da parte del Commuter o della rete.</span><span class="sxs-lookup"><span data-stu-id="de105-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**\_HOLDMAKESNEW LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-151">Quando una chiamata a questo indirizzo viene posizionata in attesa (usando [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o un'azione esterna), viene creata automaticamente una nuova chiamata (probabilmente in LINECALLSTATE \_ Dialtone).</span><span class="sxs-lookup"><span data-stu-id="de105-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**\_NOEXTERNALCALLS LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-153">L'indirizzo è associato a una linea interna in un PBX che è limitato in modo tale da non poter essere usato per inserire chiamate a un indirizzo all'esterno dell'opzione (ad esempio, è un interfono).</span><span class="sxs-lookup"><span data-stu-id="de105-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="de105-154">L'applicazione può usare questa indicazione per consentire all'utente di selezionare l'aspetto della chiamata corretto da usare per effettuare una chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="de105-155">Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate esterne, perché il provider di servizi potrebbe non essere consapevole del tipo di riga.</span><span class="sxs-lookup"><span data-stu-id="de105-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**\_NOINTERNALCALLS LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-157">L'indirizzo è associato a una linea di CO diretta (trunk) e non può essere usato per effettuare chiamate interne su un PBX.</span><span class="sxs-lookup"><span data-stu-id="de105-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="de105-158">L'applicazione può usare questa indicazione per consentire all'utente di selezionare l'aspetto della chiamata corretto da usare per effettuare una chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="de105-159">Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate interne, perché il provider di servizi potrebbe non essere consapevole del tipo di riga.</span><span class="sxs-lookup"><span data-stu-id="de105-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**\_NOPSTNADDRESSTRANSLATION LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-161">Questo indirizzo non supporta il Network Address Translation telefonico a commutazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="de105-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="de105-162">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="de105-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**\_ORIGOFFHOOK LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-164">Specifica se il telefono dell'entità di origine può essere creato automaticamente Offhook quando si effettuano chiamate.</span><span class="sxs-lookup"><span data-stu-id="de105-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**\_PARTIALDIAL LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-166">Specifica se è disponibile la composizione parziale.</span><span class="sxs-lookup"><span data-stu-id="de105-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**\_PICKUPCALLWAIT LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-168">**True** se è possibile utilizzare [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) per prelevare una chiamata rilevata dall'utente come chiamata in attesa. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="de105-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**\_PICKUPGROUPID LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-170">Specifica se è necessario un identificatore di gruppo per il prelievo della chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**\_PREDICTIVEDIALER LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-172">Questo indirizzo dispone di funzionalità avanzate di monitoraggio dello stato di avanzamento delle chiamate che possono essere applicate alle chiamate in uscita per determinare gli Stati di *chiamata, ad* esempio la riattivazione, il *specialinfo* e la *connessione* *, oppure* il tipo di supporto del dispositivo che risponde alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="de105-173">Può anche essere in grado di trasferire automaticamente le chiamate in uscita a un altro indirizzo quando una chiamata raggiunge uno qualsiasi di un set predefinito di Stati.</span><span class="sxs-lookup"><span data-stu-id="de105-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_coda LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-175">Questo indirizzo non è associato a una particolare stazione o dispositivo fisico, ma è una posizione in cui le chiamate attendono un'ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="de105-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="de105-176">Le chiamate inserite nella coda possono ricevere un particolare trattamento.</span><span class="sxs-lookup"><span data-stu-id="de105-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="de105-177">Possono anche essere trasferiti automaticamente quando una determinata risorsa diventa disponibile (ad esempio, se la coda è una coda ACD e le chiamate sono in attesa di un agente disponibile).</span><span class="sxs-lookup"><span data-stu-id="de105-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**\_punto rotta LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-179">Questo indirizzo non è associato a una particolare stazione o dispositivo fisico, ma è una posizione in cui le chiamate attendono il routing da parte dell'applicazione (l'applicazione esamina l'indirizzo chiamato ed è in grado di reindirizzare la chiamata a un altro indirizzo).</span><span class="sxs-lookup"><span data-stu-id="de105-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="de105-180">La chiamata può essere trasferita automaticamente anche in caso di scadenza di un timeout di routing (l'opzione in genere presuppone un routing predefinito).</span><span class="sxs-lookup"><span data-stu-id="de105-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**\_sicurezza LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-182">Specifica se le chiamate a questo indirizzo possono essere rese sicure al momento dell'installazione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="de105-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**\_SETCALLINGID LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-184">L'applicazione può scegliere di impostare il membro **CallingPartyID** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) quando si chiamano [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) e altre funzioni che accettano una struttura **LINECALLPARAMS** .</span><span class="sxs-lookup"><span data-stu-id="de105-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="de105-185">Se il contenuto dell'identificatore è accettabile ed è disponibile un percorso, il provider di servizi deve passare l'identificatore alla parte chiamata per indicare l'identità dell'entità chiamante.</span><span class="sxs-lookup"><span data-stu-id="de105-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**\_SETUPCONFNULL LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-187">Specifica se la configurazione di una chiamata di conferenza inizia con una chiamata iniziale (**false**) o senza una chiamata iniziale (**true**).</span><span class="sxs-lookup"><span data-stu-id="de105-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**\_TRANSFERHELD LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-189">Specifica se è possibile trasferire una chiamata a un disco rigido.</span><span class="sxs-lookup"><span data-stu-id="de105-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="de105-190">Spesso è possibile trasferire solo le chiamate su una tenuta di consultazione.</span><span class="sxs-lookup"><span data-stu-id="de105-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de105-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**\_TRANSFERMAKE LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="de105-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="de105-192">Specifica se è possibile stabilire una chiamata completamente nuova da utilizzare come chiamata di consultazione al trasferimento.</span><span class="sxs-lookup"><span data-stu-id="de105-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de105-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="de105-193">Remarks</span></span>

<span data-ttu-id="de105-194">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="de105-194">No extensibility.</span></span> <span data-ttu-id="de105-195">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="de105-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="de105-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de105-196">Requirements</span></span>



| <span data-ttu-id="de105-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="de105-197">Requirement</span></span> | <span data-ttu-id="de105-198">Valore</span><span class="sxs-lookup"><span data-stu-id="de105-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="de105-199">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="de105-199">TAPI version</span></span><br/> | <span data-ttu-id="de105-200">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="de105-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="de105-201">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de105-201">Header</span></span><br/>       | <dl> <span data-ttu-id="de105-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="de105-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de105-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de105-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de105-204">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="de105-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="de105-205">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="de105-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="de105-206">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="de105-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="de105-207">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="de105-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="de105-208">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="de105-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="de105-209">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="de105-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="de105-210">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="de105-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="de105-211">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="de105-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="de105-212">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="de105-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

