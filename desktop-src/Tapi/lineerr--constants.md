---
description: Di seguito è riportato un elenco di codici di errore che TAPI può restituire quando si richiamano operazioni su righe, indirizzi o chiamate.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: LINEERR_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e362e942f7819b0e15fcd7e8359c308e931868d57cc9da84acd62fe9e531d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254636"
---
# <a name="lineerr_-constants"></a>Costanti \_ LINEERR

Di seguito è riportato un elenco di codici di errore che TAPI può restituire quando si richiamano operazioni su righe, indirizzi o chiamate. Per altre informazioni su come determinare quali di questi codici di errore possono essere restituiti da una determinata funzione, vedere le descrizioni delle singole funzioni.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



Alla chiamata specificata non è possibile comporre l'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



Per l'indirizzo di chiamata di destinazione è abilitato il blocco delle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ ALLOCATO**
</dt> <dd> <dl> <dt>



La riga non può essere aperta a causa di una condizione persistente, ad esempio quella di una porta seriale aperta esclusivamente da un altro processo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato o l'identificatore di dispositivo di linea, ad esempio in *un parametro dwDeviceID,* non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



Il membro della modalità di bearer in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) non è valido, la modalità di bearer specificata in **LINECALLPARAMS** non è disponibile o la modalità di bearer delle chiamate non può essere impostata sulla modalità di bearer specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



La modalità di fatturazione della chiamata è stata rifiutata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



Tutte le chiamate all'indirizzo specificato sono attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**COMPLETAMENTO DI \_ LINEERROVERRUN**
</dt> <dd> <dl> <dt>



È stato superato il numero massimo di completamenti di chiamata in sospeso.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



È stato raggiunto il numero massimo di parti per una conferenza o il numero richiesto di parti non può essere soddisfatto.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo dialable contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIAGNOE**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo dialable contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo dialable contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Il parametro dell'indirizzo dialable contiene caratteri di controllo di composizione non elaborati dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



Uso del modificatore dial (:) non è supportato. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ DISCONNESSO**
</dt> <dd> <dl> <dt>



La chiamata è stata disconnessa. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione TAPI o un intervallo di versioni che non è compatibile o non può essere supportato dall'implementazione dell'API di telefonia e dal provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto un intervallo di versioni dell'estensione non valido o non supportato dal provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



Il Telephon.ini file non può essere letto o riconosciuto correttamente da TAPI a causa di incoerenze interne o problemi di formattazione. Ad esempio, la sezione Locations , Cards o Countries del \[ file Telephon.ini potrebbe essere \] \[ \] \[ \] danneggiata o incoerente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**
</dt> <dd> <dl> <dt>



Il dispositivo line è in uso e non può essere attualmente configurato, consentire l'aggiunta di un'entità, consentire una risposta a una chiamata, consentire l'esecuzione di una chiamata o consentire il trasferimento di una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



Un indirizzo specificato non è valido o non è consentito. Se non è valido, l'indirizzo contiene caratteri o cifre non validi oppure l'indirizzo di destinazione contiene caratteri di controllo di composizione (W, @, $o ?) non supportati dal provider di servizi. Se non consentito, l'indirizzo specificato non è assegnato alla riga specificata o non è valido per il reindirizzamento degli indirizzi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



L'identificatore di indirizzo specificato non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



La modalità indirizzo specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



Lo stato dell'indirizzo specificato contiene uno o più bit che non sono [**\_ costanti LINEADDRESSSTATE**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a un tipo di indirizzo non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



L'attività dell'agente specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



L'applicazione che richiama questa operazione è la destinazione della consegna indiretta. Ciò significa che TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con la priorità più alta per il tipo di supporto specificato. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



Le informazioni sul gruppo di agenti specificato non sono valide o contengono errori. L'azione richiesta non è stata eseguita.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a un gruppo di agenti non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



L'identificatore dell'agente specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



È stato usato un identificatore dell'agente non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



Lo stato della sessione dell'agente non è valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



Lo stato dell'agente specificato non è valido o contiene errori. Non sono state apportate modifiche allo stato dell'agente dell'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



L'applicazione ha fatto riferimento a uno stato dell'agente non valido. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



L'handle dell'applicazione (ad esempio specificato da *un parametro hLineApp)* o l'handle di registrazione dell'applicazione non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



Il nome dell'applicazione specificato non è valido. Se l'applicazione specifica un nome di applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e che sia con terminazione zero.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



La modalità di bearer specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Il completamento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



L'handle di chiamata specificato non è valido. Ad esempio, l'handle non **è NULL** ma non appartiene alla riga specificata. In alcuni casi, l'handle del dispositivo di chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



I parametri di chiamata specificati non sono validi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



Il parametro del privilegio di chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



Il parametro select specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



Lo stato corrente di una chiamata non è valido per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



L'elenco di stati di chiamata specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



L'identificatore di scheda permanente specificato in *dwCard* non è stato trovato in alcuna voce nella \[ sezione Cards del Registro di \] sistema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



L'identificatore di completamento non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



L'handle di chiamata specificato per la conferenza non è valido o non è un handle per una conferenza telefonica.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



L'handle di chiamata di consulenza specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



Il codice paese o area geografica specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



Al dispositivo linea non è associato alcun dispositivo per la classe di dispositivi specificata oppure la linea specificata non supporta la classe di dispositivo indicata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



L'handle del dispositivo linea non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



I parametri di composizione non sono validi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



L'elenco di cifre specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



La modalità cifra specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



Le cifre di terminazione specificate non sono valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



Il numero di versione dell'estensione del provider di servizi non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



Il *parametro dwFeature* non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



L'applicazione ha richiamato una funzionalità non disponibile in questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



L'identificatore di gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



La chiamata, il dispositivo, il dispositivo line o l'handle di riga specificati non sono validi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



La configurazione del dispositivo potrebbe non essere modificata nello stato corrente della riga. La riga può essere utilizzata da un'altra applicazione o un *parametro dwLineStates* contiene uno o più bit che non sono [ \_ costanti LINEDEVSTATE](linedevstate--constants.md). Il **valore \_ LINEERR INVALLINESTATE** può anche indicare che il dispositivo è disconnesso o fuori servizio. Questi stati vengono indicati impostando i bit corrispondenti ai valori *LINEDEVSTATUSFLAGS \_ CONNECTED* e *LINEDEVSTATUSFLAGS \_ INSERVICE* su 0 nel membro **dwDevStatusFlags** della struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) restituita dalla funzione [**lineGetLineDevStatus.**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**
</dt> <dd> <dl> <dt>



L'identificatore di posizione permanente specificato in *dwLocation* non è stato trovato in alcuna voce nella \[ sezione Percorsi del Registro di \] sistema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



L'elenco di supporti specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



L'elenco dei tipi di supporti (modalità) da monitorare contiene informazioni non valide, il parametro del tipo di supporto specificato non è valido o il provider di servizi non supporta il tipo di supporto specificato. I tipi di supporti supportati nella riga sono elencati nel **membro dwMediaModes** nella [**struttura LINEDEVCAPS.**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



Il numero specificato in *dwMessageID non* è compreso nell'intervallo specificato dal **membro dwNumCompletionMessages** nella [**struttura LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un parametro o una struttura a cui punta un parametro contiene informazioni non valide, un codice di paese o area geografica non valido, un handle di finestra non valido o il parametro dell'elenco di inoltro specificato contiene informazioni non valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



L'identificatore del park non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



La modalità park specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



La password specificata non è corretta e l'azione richiesta non è stata eseguita.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



L'applicazione ha usato una password non valida. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Uno o più parametri di puntatore specificati (ad esempio *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* e *lpToneList*) non sono validi oppure un puntatore obbligatorio a un parametro di output è **NULL.**


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



È stato impostato un flag o una combinazione di flag non valida per *il parametro dwPrivileges.*


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**
</dt> <dd> <dl> <dt>



La frequenza specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



[**L'indicatore LINEREQUESTMODE**](linerequestmode--constants.md) non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



L'identificatore del terminale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



Il parametro delle modalità terminale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



I timeout non sono supportati o un valore non rientra nell'intervallo valido specificato in [**LINEDEVCAPS.**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVARIABILE**
</dt> <dd> <dl> <dt>



Il tono personalizzato specificato non rappresenta un tono valido o è costituito da troppe frequenze oppure la struttura del tono specificata non descrive un tono valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVARIANTELIST**
</dt> <dd> <dl> <dt>



L'elenco di toni specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVARIANTEMODE**
</dt> <dd> <dl> <dt>



Il parametro della modalità tono specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



Il parametro della modalità di trasferimento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER è il valore passato nel *parametro dwDeviceID,* ma non sono state trovate righe corrispondenti ai requisiti specificati nel parametro *lpCallParams.*


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOCONFERENCE**
</dt> <dd> <dl> <dt>



La chiamata specificata non è un handle di conferenza o una chiamata del partecipante.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NODEVICE**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato, precedentemente valido, non è più accettato perché il dispositivo associato è stato rimosso dal sistema dall'ultima inizializzazione tapI. In alternativa, al dispositivo linea non è associato alcun dispositivo per la classe di dispositivi specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NODRIVER**
</dt> <dd> <dl> <dt>



Impossibile Tapiaddr.dll stato individuato oppure il provider di servizi telefonici per il dispositivo specificato ha rilevato che uno dei relativi componenti è mancante o danneggiato in un modo che non è stato rilevato in fase di inizializzazione. Per risolvere il problema, è consigliabile usare il Pannello di controllo telefonia.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Memoria insufficiente per eseguire l'operazione o impossibile bloccare la memoria.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Un provider di servizi di telefonia che non supporta più istanze viene elencato più volte nella \[ sezione Provider del Registro di \] sistema. L'applicazione deve consigliare all'utente di usare il Pannello di controllo di telefonia per rimuovere il driver duplicato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Non sono consentite più istanze di questo provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOREQUEST**
</dt> <dd> <dl> <dt>



Attualmente non è presente alcuna richiesta in sospeso della modalità indicata oppure l'applicazione non è più l'applicazione con priorità più alta per la modalità di richiesta specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOTOWNER**
</dt> <dd> <dl> <dt>



L'applicazione non dispone dei privilegi di proprietario per la chiamata specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**
</dt> <dd> <dl> <dt>



L'applicazione non è registrata come destinatario della richiesta per la modalità di richiesta indicata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



L'operazione non è riuscita per un motivo sconosciuto o non specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



L'operazione non è disponibile, ad esempio per il dispositivo o la riga specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



Il provider di servizi attualmente non dispone di larghezza di banda sufficiente per la velocità specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REINIT**
</dt> <dd> <dl> <dt>



Se è stata richiesta la reinizializzazione TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)o [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non arresta l'utilizzo dell'API (tramite [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), quando la nuova configurazione diventa effettiva e le applicazioni sono ancora una volta autorizzate a chiamare **lineInitialize** o **lineInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ REINIT**
</dt> <dd> <dl> <dt>



L'applicazione ha tentato di inizializzare TAPI due volte.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Sono in sospeso più richieste di quelle che il dispositivo è in grado di gestire.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



Risorse insufficienti per completare l'operazione. Ad esempio, non è possibile aprire una riga a causa di un overcommit della risorsa dinamica.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



Il **membro dwTotalSize** di una struttura non specifica memoria sufficiente per contenere la parte fissa della struttura specificata.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



Non è stata trovata una destinazione per la consegna della chiamata. Ciò può verificarsi se l'applicazione denominata non ha aperto la stessa riga con il bit LINECALLPRIVILEGE OWNER nel \_ *parametro dwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen). In caso di consegna in modalità media, nessuna applicazione ha aperto la stessa riga con il bit LINECALLPRIVILEGE OWNER nel parametro \_ *dwPrivileges* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) e con il tipo di supporto specificato nel parametro *dwMediaMode* specificato nel parametro *dwMediaModes* di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



L'applicazione che richiama questa operazione è la destinazione della consegna indiretta. Ciò significa che TAPI ha determinato che l'applicazione chiamante è anche l'applicazione con la priorità più alta per il tipo di supporto specificato.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ NON INIZIALIZZATO**
</dt> <dd> <dl> <dt>



L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) [**o lineInitializeEx.**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**
</dt> <dd> <dl> <dt>



L'utente ha annullato la chiamata. Questo valore viene esposto solo alle applicazioni che negoziano una versione TAPI 2.2 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**
</dt> <dd> <dl> <dt>



La stringa contenente informazioni utente supera il numero massimo di byte specificato nel membro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** o **dwUUISendUserUserInfoSize** di [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)oppure la stringa contenente informazioni utente è troppo lunga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I valori 0xC0000000 da 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo. I valori 0x80000000 a 0xBFFFFFFF sono riservati, mentre 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.

Se un'applicazione riceve un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come LINEERR \_ OPERATIONFAILED (per un motivo non specificato).

Quando si richiamano le costanti LINEERR nuove con \_ TAPI 3.0, il file Tapierr.mc deve essere aggiornato con nuovi messaggi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



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

 

 




