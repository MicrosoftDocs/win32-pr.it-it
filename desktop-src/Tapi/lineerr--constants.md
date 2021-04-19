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
# <a name="lineerr_-constants"></a>\_Costanti LINEERR

Di seguito è riportato un elenco di codici di errore che TAPI può restituire quando si richiamano operazioni su righe, indirizzi o chiamate. Per ulteriori informazioni su come determinare quali codici di errore possono essere restituiti da una determinata funzione, vedere le descrizioni delle singole funzioni.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**\_ADDRESSBLOCKED LINEERR**
</dt> <dd> <dl> <dt>



Alla chiamata specificata viene impedito di comporre l'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**\_ADDRESSBLOCKED LINEERR**
</dt> <dd> <dl> <dt>



Per l'indirizzo di chiamata di destinazione è abilitato il blocco delle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ allocato**
</dt> <dd> <dl> <dt>



Non è possibile aprire la riga a causa di una condizione persistente, ad esempio quella di una porta seriale aperta in modo esclusivo da un altro processo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**\_BADDEVICEID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo o l'identificatore del dispositivo di linea specificato, ad esempio in un parametro *dwDeviceID* , non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**\_BEARERMODEUNAVAIL LINEERR**
</dt> <dd> <dl> <dt>



Il membro della modalità di chiamata in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) non è valido, la modalità di chiamata specificata in **LINECALLPARAMS** non è disponibile o non è possibile modificare la modalità di porta di chiamata per la modalità di chiamata specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**\_BILLINGREJECTED LINEERR**
</dt> <dd> <dl> <dt>



La modalità di fatturazione della chiamata è stata rifiutata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**\_CALLUNAVAIL LINEERR**
</dt> <dd> <dl> <dt>



Tutti gli aspetti della chiamata nell'indirizzo specificato sono attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**\_COMPLETIONOVERRUN LINEERR**
</dt> <dd> <dl> <dt>



È stato superato il numero massimo di completamenti di chiamate in attesa.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**\_CONFERENCEFULL LINEERR**
</dt> <dd> <dl> <dt>



È stato raggiunto il numero massimo di entità per una conferenza oppure non è possibile soddisfare il numero di entità richiesto.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**\_DIALBILLING LINEERR**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**\_DIALDIALTONE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**\_DIALPROMPT LINEERR**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**\_DIALQUIET LINEERR**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo collegabile contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**\_DIALVOICEDETECT LINEERR**
</dt> <dd> <dl> <dt>



Uso del modificatore di composizione (:) non è supportato. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ disconnesso**
</dt> <dd> <dl> <dt>



La chiamata è stata disconnessa. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**\_INCOMPATIBLEAPIVERSION LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione o un intervallo di versioni TAPI che non è compatibile con o che non può essere supportato da, l'implementazione dell'API di telefonia e il provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**\_INCOMPATIBLEEXTVERSION LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto un intervallo di versioni di estensione non valido o non supportato dal provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**\_INIFILECORRUPT LINEERR**
</dt> <dd> <dl> <dt>



Il file di Telephon.ini non può essere letto o interpretato correttamente da TAPI a causa di incoerenze interne o problemi di formattazione. Ad esempio, la \[ \] sezione località, \[ schede \] o \[ paesi \] del file Telephon.ini potrebbe essere danneggiata o incoerente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**\_InUse LINEERR**
</dt> <dd> <dl> <dt>



Il dispositivo a linee è in uso e non può essere attualmente configurato, consentire l'aggiunta di un'entità, consentire la risposta a una chiamata, consentire l'inserimento di una chiamata o consentire il trasferimento di una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**\_INVALADDRESS LINEERR**
</dt> <dd> <dl> <dt>



Un indirizzo specificato non è valido o non è consentito. Se non è valido, l'indirizzo contiene caratteri o cifre non validi oppure l'indirizzo di destinazione contiene caratteri di controllo di composizione (W, @, $ o?) che non sono supportati dal provider di servizi. Se non è consentito, l'indirizzo specificato non è assegnato alla riga specificata o non è valido per il reindirizzamento degli indirizzi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**\_INVALADDRESSID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore di indirizzo specificato non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**\_INVALADDRESSMODE LINEERR**
</dt> <dd> <dl> <dt>



La modalità di indirizzo specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**\_INVALADDRESSSTATE LINEERR**
</dt> <dd> <dl> <dt>



Lo stato dell'indirizzo specificato contiene uno o più bit che non [**sono \_ costanti LINEADDRESSSTATE**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**\_INVALADDRESSTYPE LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a un tipo di indirizzo non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**\_INVALAGENTACTIVITY LINEERR**
</dt> <dd> <dl> <dt>



L'attività dell'agente specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**\_INVALAGENTACTIVITY LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione che richiama questa operazione è la destinazione della continuità indiretta. Ovvero, TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con priorità più elevata per il tipo di supporto specificato. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**\_INVALAGENTGROUP LINEERR**
</dt> <dd> <dl> <dt>



Le informazioni sul gruppo di agenti specificato non sono valide o contengono errori. L'azione richiesta non è stata eseguita.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**\_INVALAGENTGROUP LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a un gruppo di agenti non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**\_INVALAGENTID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore dell'agente specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**\_INVALAGENTID LINEERR**
</dt> <dd> <dl> <dt>



È stato utilizzato un identificatore agente non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**\_INVALAGENTSESSIONSTATE LINEERR**
</dt> <dd> <dl> <dt>



Lo stato della sessione dell'agente non è valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**\_INVALAGENTSTATE LINEERR**
</dt> <dd> <dl> <dt>



Lo stato dell'agente specificato non è valido o contiene errori. Non è stata apportata alcuna modifica allo stato dell'agente dell'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**\_INVALAGENTSTATE LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a uno stato dell'agente non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**\_INVALAPPHANDLE LINEERR**
</dt> <dd> <dl> <dt>



L'handle dell'applicazione (ad esempio, specificato da un parametro *hLineApp* ) o l'handle di registrazione dell'applicazione non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**\_INVALAPPNAME LINEERR**
</dt> <dd> <dl> <dt>



Il nome dell'applicazione specificato non è valido. Se l'applicazione specifica un nome di applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e con terminazione zero.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**\_INVALBEARERMODE LINEERR**
</dt> <dd> <dl> <dt>



La modalità di porta specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**\_INVALCALLCOMPLMODE LINEERR**
</dt> <dd> <dl> <dt>



Il completamento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**\_INVALCALLHANDLE LINEERR**
</dt> <dd> <dl> <dt>



L'handle di chiamata specificato non è valido. Ad esempio, l'handle non è **null** ma non appartiene alla riga specificata. In alcuni casi, l'handle del dispositivo di chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**\_INVALCALLPARAMS LINEERR**
</dt> <dd> <dl> <dt>



I parametri di chiamata specificati non sono validi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**\_INVALCALLPRIVILEGE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro del privilegio di chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**\_INVALCALLSELECT LINEERR**
</dt> <dd> <dl> <dt>



Il parametro Select specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**\_INVALCALLSTATE LINEERR**
</dt> <dd> <dl> <dt>



Lo stato corrente di una chiamata non è in uno stato valido per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**\_INVALCALLSTATELIST LINEERR**
</dt> <dd> <dl> <dt>



L'elenco di stato della chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**\_INVALCARD LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore di scheda permanente specificato in *dwCard* non è stato trovato in nessuna voce della \[ sezione schede del \] Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**\_INVALCOMPLETIONID LINEERR**
</dt> <dd> <dl> <dt>



Identificatore di completamento non valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**\_INVALCONFCALLHANDLE LINEERR**
</dt> <dd> <dl> <dt>



L'handle di chiamata specificato per la chiamata di conferenza non è valido o non è un handle per una chiamata di conferenza.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**\_INVALCONSULTCALLHANDLE LINEERR**
</dt> <dd> <dl> <dt>



L'handle di chiamata di consultazione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**\_INVALCOUNTRYCODE LINEERR**
</dt> <dd> <dl> <dt>



Il codice paese o area geografica specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**\_INVALDEVICECLASS LINEERR**
</dt> <dd> <dl> <dt>



Al dispositivo a linee non è associato alcun dispositivo per la classe del dispositivo specificata o la riga specificata non supporta la classe del dispositivo indicata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**\_INVALDEVICEHANDLE LINEERR**
</dt> <dd> <dl> <dt>



L'handle di dispositivo linea non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**\_INVALDIALPARAMS LINEERR**
</dt> <dd> <dl> <dt>



I parametri di composizione non sono validi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**\_INVALDIGITLIST LINEERR**
</dt> <dd> <dl> <dt>



L'elenco di cifre specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**\_INVALDIGITMODE LINEERR**
</dt> <dd> <dl> <dt>



La modalità di cifra specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**\_INVALDIGITS LINEERR**
</dt> <dd> <dl> <dt>



Le cifre di terminazione specificate non sono valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**\_INVALEXTVERSION LINEERR**
</dt> <dd> <dl> <dt>



Il numero di versione dell'estensione del provider di servizi non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_INVALFEATURE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro *dwFeature* non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**\_INVALFEATURE LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha richiamato una funzionalità che non è disponibile in questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**\_INVALGROUPID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore di gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**\_INVALLINEHANDLE LINEERR**
</dt> <dd> <dl> <dt>



La chiamata, il dispositivo, il dispositivo line o l'handle di riga specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**\_INVALLINESTATE LINEERR**
</dt> <dd> <dl> <dt>



La configurazione del dispositivo potrebbe non essere cambiata nello stato della riga corrente. La riga può essere utilizzata da un'altra applicazione o un parametro *dwLineStates* contiene uno o più bit che non sono [ \_ costanti LINEDEVSTATE](linedevstate--constants.md). Il **valore \_ INVALLINESTATE di LINEERR** può indicare anche che il dispositivo è disconnesso o fuori servizio. Questi stati vengono indicati impostando i bit corrispondenti ai valori *di LINEDEVSTATUSFLAGS \_ Connected* e *LINEDEVSTATUSFLAGS \_ inservice* su 0 nel membro **dwDevStatusFlags** della struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) restituita dalla funzione [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**\_INVALLOCATION LINEERR**
</dt> <dd> <dl> <dt>



Impossibile trovare l'identificatore del percorso permanente specificato in *dwLocation* in alcuna voce della \[ sezione Locations \] nel registro di sistema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**\_INVALMEDIALIST LINEERR**
</dt> <dd> <dl> <dt>



L'elenco di supporti specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**\_INVALMEDIAMODE LINEERR**
</dt> <dd> <dl> <dt>



L'elenco dei tipi di supporto (modalità) da monitorare contiene informazioni non valide, il parametro del tipo di supporto specificato non è valido o il provider di servizi non supporta il tipo di supporto specificato. I tipi di supporto supportati sulla riga sono elencati nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**\_INVALMESSAGEID LINEERR**
</dt> <dd> <dl> <dt>



Il numero fornito in *dwMessageID* non è compreso nell'intervallo specificato dal membro **DwNumCompletionMessages** nella struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**\_INVALPARAM LINEERR**
</dt> <dd> <dl> <dt>



Un parametro o una struttura a cui punta un parametro contiene informazioni non valide, il codice di un paese o di un'area non è valido, un handle di finestra non è valido oppure il parametro dell'elenco di avanzamento specificato contiene informazioni non valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**\_INVALPARKID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore del parco non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**\_INVALPARKMODE LINEERR**
</dt> <dd> <dl> <dt>



La modalità del parco specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**\_INVALPASSWORD LINEERR**
</dt> <dd> <dl> <dt>



La password specificata non è corretta e l'azione richiesta non è stata eseguita.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**\_INVALPASSWORD LINEERR**
</dt> <dd> <dl> <dt>



Per l'applicazione è stata utilizzata una password non valida. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**\_INVALPOINTER LINEERR**
</dt> <dd> <dl> <dt>



Uno o più parametri del puntatore specificati (ad esempio *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* e *lpToneList*) non sono validi oppure un puntatore obbligatorio a un parametro di output è **null**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**\_INVALPRIVSELECT LINEERR**
</dt> <dd> <dl> <dt>



È stato impostato un flag o una combinazione di flag non validi per il parametro *dwPrivileges* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**\_INVALRATE LINEERR**
</dt> <dd> <dl> <dt>



La velocità specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**\_INVALREQUESTMODE LINEERR**
</dt> <dd> <dl> <dt>



L'indicatore [**LINEREQUESTMODE**](linerequestmode--constants.md) non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**\_INVALTERMINALID LINEERR**
</dt> <dd> <dl> <dt>



L'identificatore del terminale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**\_INVALTERMINALMODE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro delle modalità terminali specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**\_INVALTIMEOUT LINEERR**
</dt> <dd> <dl> <dt>



I timeout non sono supportati o un valore non rientra nell'intervallo valido specificato in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**\_INVALTONE LINEERR**
</dt> <dd> <dl> <dt>



Il tono personalizzato specificato non rappresenta un tono valido o è costituito da un numero eccessivo di frequenze oppure la struttura di tono specificata non descrive un tono valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**\_INVALTONELIST LINEERR**
</dt> <dd> <dl> <dt>



L'elenco di toni specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**\_INVALTONEMODE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità Tone specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**\_INVALTRANSFERMODE LINEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità di trasferimento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**\_LINEMAPPERFAILED LINEERR**
</dt> <dd> <dl> <dt>



LINEMAPPER è il valore passato nel parametro *dwDeviceID* , ma non è stata trovata alcuna riga corrispondente ai requisiti specificati nel parametro *lpCallParams* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**noconference LINEERR \_**
</dt> <dd> <dl> <dt>



La chiamata specificata non è un handle di chiamata di conferenza o una chiamata del partecipante.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato, che in precedenza era valido, non viene più accettato perché il dispositivo associato è stato rimosso dal sistema dall'ultima inizializzazione di TAPI. In alternativa, al dispositivo linea non è associato alcun dispositivo per la classe del dispositivo specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



Non è stato possibile individuare Tapiaddr.dll o il provider del servizio telefonico per il dispositivo specificato ha rilevato che uno dei suoi componenti è mancante o danneggiato in modo che non sia stato rilevato al momento dell'inizializzazione. Per risolvere il problema, è consigliabile usare il pannello di controllo telefonia.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**nome del LINEERR \_**
</dt> <dd> <dl> <dt>



Memoria insufficiente per eseguire l'operazione o non è possibile bloccare la memoria.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**\_NOMULTIPLEINSTANCE LINEERR**
</dt> <dd> <dl> <dt>



Un provider di servizi di telefonia che non supporta più istanze è elencato più di una volta \[ nella \] sezione provider del registro di sistema. L'applicazione deve consigliare all'utente di usare il pannello di controllo della telefonia per rimuovere il driver duplicato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**\_NOMULTIPLEINSTANCE LINEERR**
</dt> <dd> <dl> <dt>



Non sono consentite più istanze del provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**norequest LINEERR \_**
</dt> <dd> <dl> <dt>



Attualmente non ci sono richieste in sospeso per la modalità indicata o l'applicazione non è più l'applicazione con priorità più elevata per la modalità di richiesta specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**\_NOtowner LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione non dispone del privilegio proprietario per la chiamata specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**\_NOTREGISTERED LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione non è registrata come destinatario della richiesta per la modalità di richiesta indicata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**\_OPERATIONFAILED LINEERR**
</dt> <dd> <dl> <dt>



L'operazione non è riuscita per un motivo non specificato o sconosciuto.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**\_OPERATIONUNAVAIL LINEERR**
</dt> <dd> <dl> <dt>



L'operazione non è disponibile, ad esempio per il dispositivo o la riga specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**\_RATEUNAVAIL LINEERR**
</dt> <dd> <dl> <dt>



Al provider di servizi attualmente non è disponibile una larghezza di banda sufficiente per la velocità specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REinit**
</dt> <dd> <dl> <dt>



Se è stata richiesta la reinizializzazione di TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)o [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non chiude l'utilizzo dell'API (usando [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), a quel punto la nuova configurazione diventa effettiva e le applicazioni sono nuovamente autorizzate a chiamare **lineInitialize** o **lineInitializeEx**


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REinit**
</dt> <dd> <dl> <dt>



L'applicazione ha tentato di inizializzare due volte TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**\_REQUESTOVERRUN LINEERR**
</dt> <dd> <dl> <dt>



Sono in sospeso più richieste del dispositivo che può gestire.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**\_RESOURCEUNAVAIL LINEERR**
</dt> <dd> <dl> <dt>



Risorse insufficienti per completare l'operazione. Una riga, ad esempio, non può essere aperta a causa di un overcommit di una risorsa dinamica.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**\_STRUCTURETOOSMALL LINEERR**
</dt> <dd> <dl> <dt>



Il membro **dwTotalSize** di una struttura non specifica una quantità di memoria sufficiente per contenere la parte fissa della struttura specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**\_TARGETNOTFOUND LINEERR**
</dt> <dd> <dl> <dt>



Impossibile trovare una destinazione per la consegna della chiamata. Questo problema può verificarsi se l'applicazione denominata non ha aperto la stessa riga con il \_ bit del proprietario LINECALLPRIVILEGE nel parametro *DwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen). In alternativa, nel caso della modalità supporto, nessuna applicazione ha aperto la stessa riga con il \_ bit proprietario LINECALLPRIVILEGE nel parametro *DwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) e con il tipo di supporto specificato nel parametro *DwMediaMode* è stato specificato nel parametro *dwMediaModes* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**\_TARGETSELF LINEERR**
</dt> <dd> <dl> <dt>



L'applicazione che richiama questa operazione è la destinazione della continuità indiretta. Ovvero, TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con priorità più elevata per il tipo di supporto specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR non \_ inizializzato**
</dt> <dd> <dl> <dt>



L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**\_USERCANCELLED LINEERR**
</dt> <dd> <dl> <dt>



La chiamata è stata annullata dall'utente. Questo valore viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**\_USERUSERINFOTOOBIG LINEERR**
</dt> <dd> <dl> <dt>



La stringa contenente le informazioni utente utente supera il numero massimo di byte specificato nel membro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** o **dwUUISendUserUserInfoSize** di [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)oppure la stringa contenente le informazioni utente utente è troppo lunga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I valori da 0xC0000000 a 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo. I valori 0x80000000 tramite 0xBFFFFFFF sono riservati, mentre 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.

Se un'applicazione restituisce un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come un \_ OPERATIONFAILED LINEERR (per un motivo non specificato).

Quando si richiamano le \_ costanti LINEERR che sono nuove con TAPI 3,0, il file Tapierr.MC deve essere aggiornato con nuovi messaggi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




