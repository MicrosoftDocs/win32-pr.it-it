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
# <a name="lineaddrcapflags_-constants"></a>\_Costanti LINEADDRCAPFLAGS

Le  \_ costanti del flag di bit LINEADDRCAPFLAGS vengono usate nel membro **dwAddrCapFlags** della struttura di dati [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per descrivere diverse funzionalità di indirizzi booleani.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**\_ACCEPTTOALERT LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



**True** se è necessario accettare una chiamata all'offerta usando [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) per avviare l'invio di avvisi agli utenti a entrambe le estremità della chiamata; in caso contrario, **false**. Questa operazione viene in genere usata solo con ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**\_ACDGROUP LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



L'indirizzo supporta i [gruppi ACD](about-call-center-controls.md#acd-group-object) in relazione alle operazioni del Call Center. Per ulteriori informazioni sui gruppi ACD, vedere informazioni [sui controlli del Call Center](./about-call-center-controls.md) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**\_AUTORECONNECT LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se l'eliminazione di una chiamata di consultazione si riconnette automaticamente alla chiamata in attesa di consultazione. **True** se la riconnessione viene eseguita automaticamente; in caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**\_BLOCKIDDEFAULT LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se per impostazione predefinita la rete invia o blocca le informazioni relative all'ID chiamante quando si effettua una chiamata su questo indirizzo. Se **true**, le informazioni sull'identificatore sono bloccate per impostazione predefinita; Se **false**, le informazioni sull'identificatore vengono trasmesse per impostazione predefinita.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**\_BLOCKIDOVERRIDE LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile eseguire l'override dell'impostazione predefinita per l'invio o il blocco di informazioni sull'ID chiamante per ogni chiamata. Se **true**, è possibile eseguire l'override di. Se **false**, non è possibile eseguire l'override.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**\_COMPLETIONID LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se gli identificatori di completamento restituiti da [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) sono utili e univoci. **True** se utile; in caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**\_CONFDROP LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



**True** se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) in un padre di chiamata di conferenza ha anche l'effetto collaterale dell'eliminazione (ovvero la disconnessione) delle altre parti coinvolte nella chiamata di conferenza; **False** se l'eliminazione di una chiamata di conferenza consente ancora alle altre parti di comunicare tra loro.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**\_CONFERENCEHELD LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile eseguire la conferenza a una chiamata a. Spesso è possibile aggiungere a come chiamata per la conferenza solo le chiamate su una richiesta di consultazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**\_CONFERENCEMAKE LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile stabilire una chiamata completamente nuova da utilizzare come chiamata di consultazione (da aggiungere) alla conferenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**\_DESTOFFHOOK LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se il telefono dell'entità chiamata può essere forzato automaticamente Offhook quando si effettuano chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS con \_ connessione**
</dt> <dd> <dl> <dt>



Specifica se è possibile comporre un indirizzo di destinazione in questo indirizzo per effettuare una chiamata. **True** se è necessario comporre un indirizzo di destinazione. **False** se l'indirizzo di destinazione è fisso (come con un "telefono caldo").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**\_FWDBUSYNAADDR LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se l'invio della chiamata per l'attività di occupato e per nessuna risposta può utilizzare indirizzi di inoltri diversi. Questo flag è significativo solo se l'operazione di invio è occupata e per nessuna risposta può essere controllata separatamente. Questo flag è **true** se l'invio di occupato e per nessuna risposta può utilizzare indirizzi di destinazione diversi. in caso contrario, è **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**\_FWDCONSULT LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se l'invio della chiamata implica la creazione di una chiamata di consultazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**\_FWDINTEXTADDR LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se le chiamate interne ed esterne possono essere indirizzate a indirizzi di inoltri diversi. Questo flag è significativo solo se l'invio di chiamate interne ed esterne può essere controllato separatamente. Questo flag è **true** se è possibile inviare chiamate interne ed esterne a indirizzi di destinazione diversi. in caso contrario, è **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**\_FWDNUMRINGS LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile specificare il numero di anelli per una risposta No quando si inviano chiamate senza risposta. Se **true**, l'intervallo valido viene fornito nei membri **dwMinFwdNumRings** e **dwMaxFwdNumRings** della struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**\_FWDSTATUSVALID LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se lo stato di avanzamento nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) per questo indirizzo è valido o se è al massimo una "stima migliore", dato l'assenza di una conferma accurata da parte del Commuter o della rete.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**\_HOLDMAKESNEW LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Quando una chiamata a questo indirizzo viene posizionata in attesa (usando [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o un'azione esterna), viene creata automaticamente una nuova chiamata (probabilmente in LINECALLSTATE \_ Dialtone).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**\_NOEXTERNALCALLS LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



L'indirizzo è associato a una linea interna in un PBX che è limitato in modo tale da non poter essere usato per inserire chiamate a un indirizzo all'esterno dell'opzione (ad esempio, è un interfono). L'applicazione può usare questa indicazione per consentire all'utente di selezionare l'aspetto della chiamata corretto da usare per effettuare una chiamata. Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate esterne, perché il provider di servizi potrebbe non essere consapevole del tipo di riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**\_NOINTERNALCALLS LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



L'indirizzo è associato a una linea di CO diretta (trunk) e non può essere usato per effettuare chiamate interne su un PBX. L'applicazione può usare questa indicazione per consentire all'utente di selezionare l'aspetto della chiamata corretto da usare per effettuare una chiamata. Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate interne, perché il provider di servizi potrebbe non essere consapevole del tipo di riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**\_NOPSTNADDRESSTRANSLATION LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Questo indirizzo non supporta il Network Address Translation telefonico a commutazione pubblica. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**\_ORIGOFFHOOK LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se il telefono dell'entità di origine può essere creato automaticamente Offhook quando si effettuano chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**\_PARTIALDIAL LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è disponibile la composizione parziale.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**\_PICKUPCALLWAIT LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



**True** se è possibile utilizzare [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) per prelevare una chiamata rilevata dall'utente come chiamata in attesa. in caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**\_PICKUPGROUPID LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è necessario un identificatore di gruppo per il prelievo della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**\_PREDICTIVEDIALER LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Questo indirizzo dispone di funzionalità avanzate di monitoraggio dello stato di avanzamento delle chiamate che possono essere applicate alle chiamate in uscita per determinare gli Stati di *chiamata, ad* esempio la riattivazione, il *specialinfo* e la *connessione* *, oppure* il tipo di supporto del dispositivo che risponde alla chiamata. Può anche essere in grado di trasferire automaticamente le chiamate in uscita a un altro indirizzo quando una chiamata raggiunge uno qualsiasi di un set predefinito di Stati.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_coda LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Questo indirizzo non è associato a una particolare stazione o dispositivo fisico, ma è una posizione in cui le chiamate attendono un'ulteriore elaborazione. Le chiamate inserite nella coda possono ricevere un particolare trattamento. Possono anche essere trasferiti automaticamente quando una determinata risorsa diventa disponibile (ad esempio, se la coda è una coda ACD e le chiamate sono in attesa di un agente disponibile).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**\_punto rotta LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Questo indirizzo non è associato a una particolare stazione o dispositivo fisico, ma è una posizione in cui le chiamate attendono il routing da parte dell'applicazione (l'applicazione esamina l'indirizzo chiamato ed è in grado di reindirizzare la chiamata a un altro indirizzo). La chiamata può essere trasferita automaticamente anche in caso di scadenza di un timeout di routing (l'opzione in genere presuppone un routing predefinito).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**\_sicurezza LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se le chiamate a questo indirizzo possono essere rese sicure al momento dell'installazione della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**\_SETCALLINGID LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



L'applicazione può scegliere di impostare il membro **CallingPartyID** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) quando si chiamano [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) e altre funzioni che accettano una struttura **LINECALLPARAMS** . Se il contenuto dell'identificatore è accettabile ed è disponibile un percorso, il provider di servizi deve passare l'identificatore alla parte chiamata per indicare l'identità dell'entità chiamante.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**\_SETUPCONFNULL LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se la configurazione di una chiamata di conferenza inizia con una chiamata iniziale (**false**) o senza una chiamata iniziale (**true**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**\_TRANSFERHELD LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile trasferire una chiamata a un disco rigido. Spesso è possibile trasferire solo le chiamate su una tenuta di consultazione.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**\_TRANSFERMAKE LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile stabilire una chiamata completamente nuova da utilizzare come chiamata di consultazione al trasferimento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

