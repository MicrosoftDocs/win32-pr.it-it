---
description: Le \_ costanti del flag di bit LINECALLINFOSTATE descrivono varie informazioni sulle chiamate per le quali un'applicazione può ricevere una notifica nel messaggio di riga \_ CALLINFO.
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Costanti LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324882"
---
# <a name="linecallinfostate_-constants"></a>\_Costanti LINECALLINFOSTATE

Le costanti del flag di bit **LINECALLINFOSTATE \_** descrivono varie informazioni sulle chiamate per le quali un'applicazione può ricevere una notifica nel messaggio di [**riga \_ CALLINFO**](line-callinfo.md) .

<dl> <dt>

<span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**\_APPSPECIFIC LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo specifico dell'applicazione del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**\_BEARERMODE LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il campo della modalità di porta del record delle informazioni di chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**\_CALLDATA LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il membro **CallData** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) è stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**\_CALLEDID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Uno dei campi correlati a calledID del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**\_CALLERID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Uno dei campi correlati a callerID del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**\_CALLID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo ID chiamata del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**\_CHARGINGINFO LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Informazioni di caricamento del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**\_COMPLETIONID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo dell'identificatore di completamento del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**\_CONNECTEDID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Uno dei campi correlati a connectedID del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**\_DEVSPECIFIC LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo specifico del dispositivo del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**\_DIALPARAMS LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Parametri di composizione del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**\_visualizzazione LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo di visualizzazione del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**\_HIGHLEVELCOMP LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo di compatibilità di alto livello del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**\_LOWLEVELCOMP LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo di compatibilità di basso livello del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**\_MEDIAMODE LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il campo del tipo di supporto del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**\_MONITORMODES LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Uno o più campi di monitoraggio cifre, tono o supporti nel record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**\_NUMMONITORS LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il campo numero di monitoraggi nel record delle informazioni di chiamata è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**\_NUMOWNERDECR LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il numero di campi del proprietario nel record delle informazioni di chiamata è stato ridotto.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**\_NUMOWNERINCR LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il numero di campi del proprietario nel record delle informazioni di chiamata è stato aumentato.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**\_origine LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il campo Origin del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ altro**
</dt> <dd> <dl> <dt>



Le informazioni relative alla chiamata a elementi diversi da quelli elencati di seguito sono state modificate. L'applicazione deve controllare le informazioni correnti sulla chiamata per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**\_QoS LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Uno o più membri **QoS** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) sono stati aggiornati.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**\_frequenza LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo della frequenza del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**\_motivo LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo motivo del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**\_REDIRECTINGID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Identificatore dell'indirizzo del percorso che ha reindirizzato una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**\_REDIRECTIONID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Identificatore dell'indirizzo del percorso a cui è stata reindirizzata una chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**\_RELATEDCALLID LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo ID chiamata correlato del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**\_terminale LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Informazioni sulla modalità terminale del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**\_trattamento LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Il membro **CallTreatment** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) è stato aggiornato. Questo problema può verificarsi in risposta a una funzione [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , una modifica dello stato di chiamata, una chiamata "Vector" o un altro script che controlla la chiamata o al completamento della riproduzione di un messaggio registrato (in genere, che indica una modifica a "Silence" o "Music").


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**\_trunk LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Campo trunk del record di informazioni sulle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**\_USERUSERINFO LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Informazioni utente utente del record di informazioni sulle chiamate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Quando si verificano modifiche in questa struttura di dati, all'applicazione viene inviato un messaggio di [**riga \_ CALLINFO**](line-callinfo.md) . I parametri di questo messaggio sono un handle per la chiamata e un'indicazione dell'elemento informazioni che è stato modificato. La struttura dei dati [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) indica anche quali elementi di informazioni sulle chiamate sono validi per ogni chiamata all'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ CALLINFO**](line-callinfo.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




