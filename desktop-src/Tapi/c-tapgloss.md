---
description: I termini seguenti sono utili per comprendere la tecnologia TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309972"
---
# <a name="c-telephony-api"></a><span data-ttu-id="97708-103">C (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="97708-103">C (Telephony API)</span></span>

<span data-ttu-id="97708-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [d](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [i](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="97708-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="97708-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**classificazione chiamata**</span><span class="sxs-lookup"><span data-stu-id="97708-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="97708-106">Processo TAPI che segnala le modifiche apportate al tipo di flusso multimediale (voce, fax, modem dati e così via) alle applicazioni partecipanti.</span><span class="sxs-lookup"><span data-stu-id="97708-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="97708-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**monitoraggio stato chiamata**</span><span class="sxs-lookup"><span data-stu-id="97708-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="97708-108">Il processo di ascolto di toni udibili, ad esempio un tono di composizione, toni di informazioni speciali, segnali occupati e richiamate per determinare lo stato di una chiamata (avanzamento attraverso la rete).</span><span class="sxs-lookup"><span data-stu-id="97708-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="97708-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**Reindirizzamento chiamate**</span><span class="sxs-lookup"><span data-stu-id="97708-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="97708-110">Funzione che consente a un'applicazione di deflettere una chiamata offerta a un altro indirizzo senza prima rispondere alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="97708-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="97708-111">Il reindirizzamento delle chiamate differisce dall'invio di chiamate in quanto l'invio delle chiamate viene eseguito dal commutere senza il coinvolgimento dell'applicazione; il reindirizzamento può essere eseguito in base a chiamate per chiamata dall'applicazione, ad esempio, basata su informazioni sull'ID chiamante.</span><span class="sxs-lookup"><span data-stu-id="97708-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="97708-112">Il trasferimento di una chiamata è diverso da quello in cui il trasferimento di una chiamata richiede che prima venga fornita una risposta alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="97708-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="97708-113">Vedere *chiamata-ID*, *ID chiamante*, [*Reindirizzamento ID*](r-tapgloss.md), [*ID Reindirizzamento*](r-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="97708-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="97708-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**ID chiamato**</span><span class="sxs-lookup"><span data-stu-id="97708-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="97708-115">Identifica l'indirizzo di destinazione originale di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="97708-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="97708-116">Vedere *Reindirizzamento delle chiamate*.</span><span class="sxs-lookup"><span data-stu-id="97708-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="97708-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**ID chiamante**</span><span class="sxs-lookup"><span data-stu-id="97708-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="97708-118">Identifica l'indirizzo di origine di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="97708-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="97708-119">Vedere *Reindirizzamento delle chiamate*.</span><span class="sxs-lookup"><span data-stu-id="97708-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="97708-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**Ufficio centrale**</span><span class="sxs-lookup"><span data-stu-id="97708-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="97708-121">La struttura locale della società telefonica che fornisce il servizio telefonico in un'area specifica.</span><span class="sxs-lookup"><span data-stu-id="97708-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="97708-122">In genere, le linee dei sottoscrittori sono unite al cambio di equipaggiamento che connette gli altri sottoscrittori tra loro, in locale e a distanza molto lungo.</span><span class="sxs-lookup"><span data-stu-id="97708-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="97708-123">Detto anche *co*.</span><span class="sxs-lookup"><span data-stu-id="97708-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="97708-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="97708-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="97708-125">Un servizio telefonico aziendale offerto da una società telefonica locale da un ufficio centrale locale.</span><span class="sxs-lookup"><span data-stu-id="97708-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="97708-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**connessione incentrata sul computer**</span><span class="sxs-lookup"><span data-stu-id="97708-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="97708-127">Connessione che utilizza una scheda del componente aggiuntivo del computer o una casella esterna connessa alla rete telefonica e al set di telefono.</span><span class="sxs-lookup"><span data-stu-id="97708-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="97708-128">Confrontare la [*connessione incentrata sul telefono*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="97708-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="97708-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**Connected-ID**</span><span class="sxs-lookup"><span data-stu-id="97708-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="97708-130">Identificatore per l'entità a cui è stata effettivamente connessa la chiamata.</span><span class="sxs-lookup"><span data-stu-id="97708-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="97708-131">Questo può essere diverso dalla parte chiamata se la chiamata è stata deviata.</span><span class="sxs-lookup"><span data-stu-id="97708-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



