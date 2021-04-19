---
description: Di seguito è riportato un elenco di codici di errore che TAPI può restituire quando si richiamano operazioni su righe, indirizzi o chiamate.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Costanti LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333552"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="59cb7-103">\_Costanti LINEERR</span><span class="sxs-lookup"><span data-stu-id="59cb7-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="59cb7-104">Di seguito è riportato un elenco di codici di errore che TAPI può restituire quando si richiamano operazioni su righe, indirizzi o chiamate.</span><span class="sxs-lookup"><span data-stu-id="59cb7-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="59cb7-105">Per ulteriori informazioni su come determinare quali codici di errore possono essere restituiti da una determinata funzione, vedere le descrizioni delle singole funzioni.</span><span class="sxs-lookup"><span data-stu-id="59cb7-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="59cb7-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**\_ADDRESSBLOCKED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-107">Alla chiamata specificata viene impedito di comporre l'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**\_ADDRESSBLOCKED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-109">Per l'indirizzo di chiamata di destinazione è abilitato il blocco delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="59cb7-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="59cb7-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-111">Non è possibile aprire la riga a causa di una condizione persistente, ad esempio quella di una porta seriale aperta in modo esclusivo da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="59cb7-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**\_BADDEVICEID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-113">L'identificatore di dispositivo o l'identificatore del dispositivo di linea specificato, ad esempio in un parametro *dwDeviceID* , non è valido o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="59cb7-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**\_BEARERMODEUNAVAIL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-115">Il membro della modalità di chiamata in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) non è valido, la modalità di chiamata specificata in **LINECALLPARAMS** non è disponibile o non è possibile modificare la modalità di porta di chiamata per la modalità di chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**\_BILLINGREJECTED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-117">La modalità di fatturazione della chiamata è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**\_CALLUNAVAIL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-119">Tutti gli aspetti della chiamata nell'indirizzo specificato sono attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="59cb7-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**\_COMPLETIONOVERRUN LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-121">È stato superato il numero massimo di completamenti di chiamate in attesa.</span><span class="sxs-lookup"><span data-stu-id="59cb7-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**\_CONFERENCEFULL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-123">È stato raggiunto il numero massimo di entità per una conferenza oppure non è possibile soddisfare il numero di entità richiesto.</span><span class="sxs-lookup"><span data-stu-id="59cb7-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**\_DIALBILLING LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-125">Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**\_DIALDIALTONE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-127">Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**\_DIALPROMPT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-129">Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**\_DIALQUIET LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-131">Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**\_DIALVOICEDETECT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-133">Uso del modificatore di composizione (:) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="59cb7-134">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="59cb7-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-136">La chiamata è stata disconnessa.</span><span class="sxs-lookup"><span data-stu-id="59cb7-136">The call has been disconnected.</span></span> <span data-ttu-id="59cb7-137">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**\_INCOMPATIBLEAPIVERSION LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-139">L'applicazione ha richiesto una versione o un intervallo di versioni TAPI che non è compatibile con o che non può essere supportato da, l'implementazione dell'API di telefonia e il provider di servizi corrispondente.</span><span class="sxs-lookup"><span data-stu-id="59cb7-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**\_INCOMPATIBLEEXTVERSION LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-141">L'applicazione ha richiesto un intervallo di versioni di estensione non valido o non supportato dal provider di servizi corrispondente.</span><span class="sxs-lookup"><span data-stu-id="59cb7-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**\_INIFILECORRUPT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-143">Il file di Telephon.ini non può essere letto o interpretato correttamente da TAPI a causa di incoerenze interne o problemi di formattazione.</span><span class="sxs-lookup"><span data-stu-id="59cb7-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="59cb7-144">Ad esempio, la \[ \] sezione località, \[ schede \] o \[ paesi \] del file Telephon.ini potrebbe essere danneggiata o incoerente.</span><span class="sxs-lookup"><span data-stu-id="59cb7-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**\_InUse LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-146">Il dispositivo a linee è in uso e non può essere attualmente configurato, consentire l'aggiunta di un'entità, consentire la risposta a una chiamata, consentire l'inserimento di una chiamata o consentire il trasferimento di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**\_INVALADDRESS LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-148">Un indirizzo specificato non è valido o non è consentito.</span><span class="sxs-lookup"><span data-stu-id="59cb7-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="59cb7-149">Se non è valido, l'indirizzo contiene caratteri o cifre non validi oppure l'indirizzo di destinazione contiene caratteri di controllo di composizione (W, @, $ o?) che non sono supportati dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="59cb7-150">Se non è consentito, l'indirizzo specificato non è assegnato alla riga specificata o non è valido per il reindirizzamento degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**\_INVALADDRESSID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-152">L'identificatore di indirizzo specificato non è valido o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="59cb7-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**\_INVALADDRESSMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-154">La modalità di indirizzo specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**\_INVALADDRESSSTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-156">Lo stato dell'indirizzo specificato contiene uno o più bit che non [**sono \_ costanti LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59cb7-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**\_INVALADDRESSTYPE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-158">L'applicazione ha fatto riferimento a un tipo di indirizzo non valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="59cb7-159">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**\_INVALAGENTACTIVITY LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-161">L'attività dell'agente specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**\_INVALAGENTACTIVITY LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-163">L'applicazione che richiama questa operazione è la destinazione della continuità indiretta.</span><span class="sxs-lookup"><span data-stu-id="59cb7-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="59cb7-164">Ovvero, TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con priorità più elevata per il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="59cb7-165">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**\_INVALAGENTGROUP LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-167">Le informazioni sul gruppo di agenti specificato non sono valide o contengono errori.</span><span class="sxs-lookup"><span data-stu-id="59cb7-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="59cb7-168">L'azione richiesta non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="59cb7-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**\_INVALAGENTGROUP LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-170">L'applicazione ha fatto riferimento a un gruppo di agenti non valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="59cb7-171">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**\_INVALAGENTID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-173">L'identificatore dell'agente specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**\_INVALAGENTID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-175">È stato utilizzato un identificatore agente non valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="59cb7-176">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**\_INVALAGENTSESSIONSTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-178">Lo stato della sessione dell'agente non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-178">The agent session state is invalid.</span></span> <span data-ttu-id="59cb7-179">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**\_INVALAGENTSTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-181">Lo stato dell'agente specificato non è valido o contiene errori.</span><span class="sxs-lookup"><span data-stu-id="59cb7-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="59cb7-182">Non è stata apportata alcuna modifica allo stato dell'agente dell'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**\_INVALAGENTSTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-184">L'applicazione ha fatto riferimento a uno stato dell'agente non valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="59cb7-185">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**\_INVALAPPHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-187">L'handle dell'applicazione (ad esempio, specificato da un parametro *hLineApp* ) o l'handle di registrazione dell'applicazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**\_INVALAPPNAME LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-189">Il nome dell'applicazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-189">The specified application name is invalid.</span></span> <span data-ttu-id="59cb7-190">Se l'applicazione specifica un nome di applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e con terminazione zero.</span><span class="sxs-lookup"><span data-stu-id="59cb7-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**\_INVALBEARERMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-192">La modalità di porta specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**\_INVALCALLCOMPLMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-194">Il completamento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**\_INVALCALLHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-196">L'handle di chiamata specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-196">The specified call handle is not valid.</span></span> <span data-ttu-id="59cb7-197">Ad esempio, l'handle non è **null** ma non appartiene alla riga specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="59cb7-198">In alcuni casi, l'handle del dispositivo di chiamata specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**\_INVALCALLPARAMS LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-200">I parametri di chiamata specificati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**\_INVALCALLPRIVILEGE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-202">Il parametro del privilegio di chiamata specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**\_INVALCALLSELECT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-204">Il parametro Select specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**\_INVALCALLSTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-206">Lo stato corrente di una chiamata non è in uno stato valido per l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="59cb7-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**\_INVALCALLSTATELIST LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-208">L'elenco di stato della chiamata specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**\_INVALCARD LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-210">L'identificatore di scheda permanente specificato in *dwCard* non è stato trovato in nessuna voce della \[ sezione schede del \] Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="59cb7-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**\_INVALCOMPLETIONID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-212">Identificatore di completamento non valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**\_INVALCONFCALLHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-214">L'handle di chiamata specificato per la chiamata di conferenza non è valido o non è un handle per una chiamata di conferenza.</span><span class="sxs-lookup"><span data-stu-id="59cb7-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**\_INVALCONSULTCALLHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-216">L'handle di chiamata di consultazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**\_INVALCOUNTRYCODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-218">Il codice paese o area geografica specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**\_INVALDEVICECLASS LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-220">Al dispositivo a linee non è associato alcun dispositivo per la classe del dispositivo specificata o la riga specificata non supporta la classe del dispositivo indicata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**\_INVALDEVICEHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-222">L'handle di dispositivo linea non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**\_INVALDIALPARAMS LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-224">I parametri di composizione non sono validi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**\_INVALDIGITLIST LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-226">L'elenco di cifre specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**\_INVALDIGITMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-228">La modalità di cifra specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**\_INVALDIGITS LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-230">Le cifre di terminazione specificate non sono valide.</span><span class="sxs-lookup"><span data-stu-id="59cb7-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**\_INVALEXTVERSION LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-232">Il numero di versione dell'estensione del provider di servizi non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_INVALFEATURE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-234">Il parametro *dwFeature* non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_INVALFEATURE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-236">L'applicazione ha richiamato una funzionalità che non è disponibile in questa riga.</span><span class="sxs-lookup"><span data-stu-id="59cb7-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**\_INVALGROUPID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-238">L'identificatore di gruppo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**\_INVALLINEHANDLE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-240">La chiamata, il dispositivo, il dispositivo line o l'handle di riga specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**\_INVALLINESTATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-242">La configurazione del dispositivo potrebbe non essere cambiata nello stato della riga corrente.</span><span class="sxs-lookup"><span data-stu-id="59cb7-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="59cb7-243">La riga può essere utilizzata da un'altra applicazione o un parametro *dwLineStates* contiene uno o più bit che non sono [ \_ costanti LINEDEVSTATE](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59cb7-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="59cb7-244">Il **valore \_ INVALLINESTATE di LINEERR** può indicare anche che il dispositivo è disconnesso o fuori servizio.</span><span class="sxs-lookup"><span data-stu-id="59cb7-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="59cb7-245">Questi stati vengono indicati impostando i bit corrispondenti ai valori *di LINEDEVSTATUSFLAGS \_ Connected* e *LINEDEVSTATUSFLAGS \_ inservice* su 0 nel membro **dwDevStatusFlags** della struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) restituita dalla funzione [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="59cb7-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**\_INVALLOCATION LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-247">Impossibile trovare l'identificatore del percorso permanente specificato in *dwLocation* in alcuna voce della \[ sezione Locations \] nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="59cb7-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**\_INVALMEDIALIST LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-249">L'elenco di supporti specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**\_INVALMEDIAMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-251">L'elenco dei tipi di supporto (modalità) da monitorare contiene informazioni non valide, il parametro del tipo di supporto specificato non è valido o il provider di servizi non supporta il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="59cb7-252">I tipi di supporto supportati sulla riga sono elencati nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="59cb7-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**\_INVALMESSAGEID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-254">Il numero fornito in *dwMessageID* non è compreso nell'intervallo specificato dal membro **DwNumCompletionMessages** nella struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="59cb7-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**\_INVALPARAM LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-256">Un parametro o una struttura a cui punta un parametro contiene informazioni non valide, il codice di un paese o di un'area non è valido, un handle di finestra non è valido oppure il parametro dell'elenco di avanzamento specificato contiene informazioni non valide.</span><span class="sxs-lookup"><span data-stu-id="59cb7-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**\_INVALPARKID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-258">L'identificatore del parco non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**\_INVALPARKMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-260">La modalità del parco specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**\_INVALPASSWORD LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-262">La password specificata non è corretta e l'azione richiesta non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="59cb7-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**\_INVALPASSWORD LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-264">Per l'applicazione è stata utilizzata una password non valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-264">The application used an invalid password.</span></span> <span data-ttu-id="59cb7-265">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**\_INVALPOINTER LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-267">Uno o più parametri del puntatore specificati (ad esempio *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* e *lpToneList*) non sono validi oppure un puntatore obbligatorio a un parametro di output è **null**.</span><span class="sxs-lookup"><span data-stu-id="59cb7-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**\_INVALPRIVSELECT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-269">È stato impostato un flag o una combinazione di flag non validi per il parametro *dwPrivileges* .</span><span class="sxs-lookup"><span data-stu-id="59cb7-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**\_INVALRATE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-271">La velocità specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="59cb7-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**\_INVALREQUESTMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-273">L'indicatore [**LINEREQUESTMODE**](linerequestmode--constants.md) non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**\_INVALTERMINALID LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-275">L'identificatore del terminale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**\_INVALTERMINALMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-277">Il parametro delle modalità terminali specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**\_INVALTIMEOUT LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-279">I timeout non sono supportati o un valore non rientra nell'intervallo valido specificato in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="59cb7-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**\_INVALTONE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-281">Il tono personalizzato specificato non rappresenta un tono valido o è costituito da un numero eccessivo di frequenze oppure la struttura di tono specificata non descrive un tono valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**\_INVALTONELIST LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-283">L'elenco di toni specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**\_INVALTONEMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-285">Il parametro della modalità Tone specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**\_INVALTRANSFERMODE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-287">Il parametro della modalità di trasferimento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="59cb7-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**\_LINEMAPPERFAILED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-289">LINEMAPPER è il valore passato nel parametro *dwDeviceID* , ma non è stata trovata alcuna riga corrispondente ai requisiti specificati nel parametro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="59cb7-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**noconference LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="59cb7-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-291">La chiamata specificata non è un handle di chiamata di conferenza o una chiamata del partecipante.</span><span class="sxs-lookup"><span data-stu-id="59cb7-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**</span><span class="sxs-lookup"><span data-stu-id="59cb7-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-293">L'identificatore di dispositivo specificato, che in precedenza era valido, non viene più accettato perché il dispositivo associato è stato rimosso dal sistema dall'ultima inizializzazione di TAPI.</span><span class="sxs-lookup"><span data-stu-id="59cb7-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="59cb7-294">In alternativa, al dispositivo linea non è associato alcun dispositivo per la classe del dispositivo specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="59cb7-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-296">Non è stato possibile individuare Tapiaddr.dll o il provider del servizio telefonico per il dispositivo specificato ha rilevato che uno dei suoi componenti è mancante o danneggiato in modo che non sia stato rilevato al momento dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="59cb7-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="59cb7-297">Per risolvere il problema, è consigliabile usare il pannello di controllo telefonia.</span><span class="sxs-lookup"><span data-stu-id="59cb7-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**nome del LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="59cb7-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-299">Memoria insufficiente per eseguire l'operazione o non è possibile bloccare la memoria.</span><span class="sxs-lookup"><span data-stu-id="59cb7-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**\_NOMULTIPLEINSTANCE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-301">Un provider di servizi di telefonia che non supporta più istanze è elencato più di una volta \[ nella \] sezione provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="59cb7-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="59cb7-302">L'applicazione deve consigliare all'utente di usare il pannello di controllo della telefonia per rimuovere il driver duplicato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**\_NOMULTIPLEINSTANCE LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-304">Non sono consentite più istanze del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**norequest LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="59cb7-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-306">Attualmente non ci sono richieste in sospeso per la modalità indicata o l'applicazione non è più l'applicazione con priorità più elevata per la modalità di richiesta specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**\_NOtowner LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-308">L'applicazione non dispone del privilegio proprietario per la chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**\_NOTREGISTERED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-310">L'applicazione non è registrata come destinatario della richiesta per la modalità di richiesta indicata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**\_OPERATIONFAILED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-312">L'operazione non è riuscita per un motivo non specificato o sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="59cb7-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**\_OPERATIONUNAVAIL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-314">L'operazione non è disponibile, ad esempio per il dispositivo o la riga specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**\_RATEUNAVAIL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-316">Al provider di servizi attualmente non è disponibile una larghezza di banda sufficiente per la velocità specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="59cb7-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-318">Se è stata richiesta la reinizializzazione di TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)o [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non chiude l'utilizzo dell'API (usando [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), a quel punto la nuova configurazione diventa effettiva e le applicazioni sono nuovamente autorizzate a chiamare **lineInitialize** o **lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="59cb7-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="59cb7-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-320">L'applicazione ha tentato di inizializzare due volte TAPI.</span><span class="sxs-lookup"><span data-stu-id="59cb7-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**\_REQUESTOVERRUN LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-322">Sono in sospeso più richieste del dispositivo che può gestire.</span><span class="sxs-lookup"><span data-stu-id="59cb7-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**\_RESOURCEUNAVAIL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-324">Risorse insufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="59cb7-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="59cb7-325">Una riga, ad esempio, non può essere aperta a causa di un overcommit di una risorsa dinamica.</span><span class="sxs-lookup"><span data-stu-id="59cb7-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**\_STRUCTURETOOSMALL LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-327">Il membro **dwTotalSize** di una struttura non specifica una quantità di memoria sufficiente per contenere la parte fissa della struttura specificata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**\_TARGETNOTFOUND LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-329">Impossibile trovare una destinazione per la consegna della chiamata.</span><span class="sxs-lookup"><span data-stu-id="59cb7-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="59cb7-330">Questo problema può verificarsi se l'applicazione denominata non ha aperto la stessa riga con il \_ bit del proprietario LINECALLPRIVILEGE nel parametro *DwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="59cb7-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="59cb7-331">In alternativa, nel caso della modalità supporto, nessuna applicazione ha aperto la stessa riga con il \_ bit proprietario LINECALLPRIVILEGE nel parametro *DwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) e con il tipo di supporto specificato nel parametro *DwMediaMode* è stato specificato nel parametro *dwMediaModes* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="59cb7-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**\_TARGETSELF LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-333">L'applicazione che richiama questa operazione è la destinazione della continuità indiretta.</span><span class="sxs-lookup"><span data-stu-id="59cb7-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="59cb7-334">Ovvero, TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con priorità più elevata per il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="59cb7-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="59cb7-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-336">L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="59cb7-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**\_USERCANCELLED LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-338">La chiamata è stata annullata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="59cb7-338">The user cancelled the call.</span></span> <span data-ttu-id="59cb7-339">Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="59cb7-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59cb7-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**\_USERUSERINFOTOOBIG LINEERR**</span><span class="sxs-lookup"><span data-stu-id="59cb7-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59cb7-341">La stringa contenente le informazioni utente utente supera il numero massimo di byte specificato nel membro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** o **dwUUISendUserUserInfoSize** di [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)oppure la stringa contenente le informazioni utente utente è troppo lunga.</span><span class="sxs-lookup"><span data-stu-id="59cb7-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59cb7-342">Commenti</span><span class="sxs-lookup"><span data-stu-id="59cb7-342">Remarks</span></span>

<span data-ttu-id="59cb7-343">I valori da 0xC0000000 a 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59cb7-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="59cb7-344">I valori 0x80000000 tramite 0xBFFFFFFF sono riservati, mentre 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.</span><span class="sxs-lookup"><span data-stu-id="59cb7-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="59cb7-345">Se un'applicazione restituisce un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come un \_ OPERATIONFAILED LINEERR (per un motivo non specificato).</span><span class="sxs-lookup"><span data-stu-id="59cb7-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="59cb7-346">Quando si richiamano le \_ costanti LINEERR che sono nuove con TAPI 3,0, il file Tapierr.MC deve essere aggiornato con nuovi messaggi.</span><span class="sxs-lookup"><span data-stu-id="59cb7-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cb7-347">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59cb7-347">Requirements</span></span>



| <span data-ttu-id="59cb7-348">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cb7-348">Requirement</span></span> | <span data-ttu-id="59cb7-349">Valore</span><span class="sxs-lookup"><span data-stu-id="59cb7-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="59cb7-350">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="59cb7-350">TAPI version</span></span><br/> | <span data-ttu-id="59cb7-351">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="59cb7-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="59cb7-352">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59cb7-352">Header</span></span><br/>       | <dl> <span data-ttu-id="59cb7-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="59cb7-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59cb7-354">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59cb7-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cb7-355">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="59cb7-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="59cb7-356">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="59cb7-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="59cb7-357">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="59cb7-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="59cb7-358">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="59cb7-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="59cb7-359">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="59cb7-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="59cb7-360">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="59cb7-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="59cb7-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="59cb7-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="59cb7-362">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="59cb7-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




