---
description: Le costanti del flag di bit LINEADDRCAPFLAGS vengono usate nel membro dwAddrCapFlags della struttura di dati LINEADDRESSCAPS per descrivere varie funzionalità degli indirizzi \_ booleani.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: LINEADDRCAPFLAGS_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee1612c0d57b98a5f3caf82bcd26988fd5d9455c34e5caea5832153af06a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003119"
---
# <a name="lineaddrcapflags_-constants"></a>Costanti LINEADDRCAPFLAGS \_

Le costanti del flag di bit **LINEADDRCAPFLAGS** vengono usate nel membro \_ **dwAddrCapFlags** della struttura di dati [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per descrivere varie funzionalità degli indirizzi booleani.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**TRUE** se una chiamata di offerta deve essere accettata tramite [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) per avviare l'avviso degli utenti a entrambe le estremità della chiamata; in caso contrario, **FALSE.** In genere viene usato solo con ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



L'indirizzo supporta i [gruppi ACD](about-call-center-controls.md#acd-group-object) in relazione alle operazioni del call center. Per [altre informazioni sui gruppi acd,](./about-call-center-controls.md) vedere Informazioni sui controlli call center.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ AUTORECONNECT**
</dt> <dd> <dl> <dt>



Specifica se l'eliminazione di una chiamata di consulenza si riconnette automaticamente alla chiamata in attesa di consulenza. **TRUE se** la riconnessione viene eseguita automaticamente. in caso contrario, **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Specifica se la rete per impostazione predefinita invia o blocca le informazioni sull'ID chiamante quando effettua una chiamata a questo indirizzo. Se **TRUE,** le informazioni sull'identificatore sono bloccate per impostazione predefinita. se **FALSE,** le informazioni sull'identificatore vengono trasmesse per impostazione predefinita.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Specifica se è possibile eseguire l'override dell'impostazione predefinita per l'invio o il blocco delle informazioni sull'ID chiamante per ogni chiamata. Se **TRUE,** l'override è possibile; Se **FALSE,** l'override non è possibile.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Specifica se gli identificatori di completamento restituiti da [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) sono utili e univoci. **TRUE se** utile; in caso contrario, **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**TRUE** se [**lineDrop in**](/windows/desktop/api/Tapi/nf-tapi-linedrop) una conferenza telefonica padre ha anche l'effetto collaterale di eliminare (ovvero disconnettere) le altre parti coinvolte nella conferenza telefonica; **FALSE** se l'eliminazione di una conferenza telefonica consente comunque alle altre parti di parlare tra loro.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**
</dt> <dd> <dl> <dt>



Specifica se è possibile eseguire una conferenza telefonica con una chiamata hard-held. Spesso, solo le chiamate in attesa di consulenza possono essere aggiunte a come conferenza telefonica.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Specifica se è possibile stabilire una chiamata completamente nuova da usare come chiamata di consulenza (da aggiungere) alla conferenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Specifica se il telefono della parte chiamata può essere automaticamente forzato durante le chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ DIALED**
</dt> <dd> <dl> <dt>



Specifica se è possibile comporre un indirizzo di destinazione su questo indirizzo per effettuare una chiamata. **TRUE** se è necessario comporre un indirizzo di destinazione. **FALSE** se l'indirizzo di destinazione è fisso (come con un "telefono a caldo").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Specifica se l'inoltro di chiamata per occupato e per nessuna risposta può usare indirizzi di inoltro diversi. Questo flag è significativo solo se l'inoltro per occupato e per nessuna risposta può essere controllato separatamente. Questo flag è **TRUE se l'inoltro** per occupato e per nessuna risposta può usare indirizzi di destinazione diversi. in caso contrario, è **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Specifica se l'inoltro di chiamata implica la creazione di una chiamata di consulenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Specifica se le chiamate interne ed esterne possono essere inoltrate a indirizzi di inoltro diversi. Questo flag è significativo solo se l'inoltro di chiamate interne ed esterne può essere controllato separatamente. Questo flag è **TRUE se** le chiamate interne ed esterne possono essere inoltrate a indirizzi di destinazione diversi. in caso contrario, è **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Specifica se è possibile specificare il numero di anelli per una risposta no quando si inoltrano chiamate senza risposta. Se **TRUE,** l'intervallo valido viene specificato nei membri **dwMinFwdNumRings** e **dwMaxFwdNumRings** della [**struttura LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Specifica se lo stato di inoltro nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) per questo indirizzo è valido o è al massimo una "stima ottimale", data l'assenza di una conferma accurata da parte del commutatore o della rete.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Quando una chiamata a questo indirizzo viene messa in attesa (usando [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o un'azione esterna), viene creata automaticamente una nuova chiamata (molto probabilmente in LINECALLSTATE \_ DIALTONE).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



L'indirizzo è associato a una riga interna in un centralino limitato in modo che non possa essere usato per effettuare chiamate a un indirizzo esterno all'interruttore (ad esempio, si tratta di un citofono). L'applicazione può usare questa indicazione per aiutare l'utente a selezionare l'aspetto corretto della chiamata da usare per effettuare una chiamata. Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate esterne, perché il provider di servizi potrebbe non essere cognizant del tipo di riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



L'indirizzo è associato a una linea co-co diretta (trunk) e non può essere usato per effettuare chiamate interne su un SISTEMA CENTRALINO. L'applicazione può usare questa indicazione per aiutare l'utente a selezionare l'aspetto corretto della chiamata da usare per effettuare una chiamata. Quando questo bit è disattivato, non indica necessariamente che l'indirizzo può essere usato per effettuare chiamate interne, perché il provider di servizi potrebbe non essere cognizant del tipo di riga.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Questo indirizzo non supporta la conversione degli indirizzi di rete telefonica con commutazione pubblica. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Specifica se il telefono dell'entità di origine può essere automaticamente preso in offhook quando si effettuano chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Specifica se la composizione parziale è disponibile.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**TRUE** se [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usato per prelevare una chiamata rilevata dall'utente come chiamata in attesa di chiamata; in caso contrario, **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Specifica se è necessario un identificatore di gruppo per il ritiro della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Questo indirizzo include funzionalità avanzate di monitoraggio dello stato di avanzamento delle chiamate che possono essere applicate alle chiamate in uscita per determinare gli stati di chiamata, ad esempio *ringback,* *busy,* *specialinfo* e *connected* o il tipo di supporto del dispositivo che risponde alla chiamata. Può anche essere in grado di trasferire automaticamente le chiamate in uscita a un altro indirizzo quando una chiamata raggiunge uno qualsiasi di un set predefinito di stati.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**CODA LINEADDRCAPFLAGS \_**
</dt> <dd> <dl> <dt>



Questo indirizzo non è associato a una stazione o a un dispositivo fisico specifico, ma è un luogo di attesa in cui le chiamate attendono un'ulteriore elaborazione. Le chiamate inserite nella coda possono ricevere un trattamento specifico. Possono anche essere trasferiti automaticamente quando una determinata risorsa diventa disponibile(ad esempio, se la coda è una coda ACD e le chiamate sono in attesa di un agente disponibile).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



Questo indirizzo non è associato a una stazione o a un dispositivo fisico specifico, ma è una posizione di attesa delle chiamate per il routing da parte dell'applicazione (l'applicazione esamina l'indirizzo chiamato e può reindirizzare la chiamata a un altro indirizzo). La chiamata può anche essere trasferita automaticamente se scade un timeout di routing (l'opzione presuppone in genere un routing predefinito).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ SICURO**
</dt> <dd> <dl> <dt>



Specifica se le chiamate su questo indirizzo possono essere rese sicure in fase di configurazione delle chiamate.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



L'applicazione può scegliere di impostare il membro **CallingPartyID** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) quando chiama [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) e altre funzioni che accettano una **struttura LINECALLPARAMS.** Se il contenuto dell'identificatore è accettabile ed è disponibile un percorso, il provider di servizi passerà l'identificatore all'entità chiamata per indicare l'identità della parte chiamante.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Specifica se la configurazione di una conferenza telefonica inizia con una chiamata iniziale (**FALSE**) o senza chiamata iniziale (**TRUE**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**TRASFERIMENTO DI LINEADDRCAPFLAGS \_**
</dt> <dd> <dl> <dt>



Specifica se è possibile trasferire una chiamata hard-held. Spesso è possibile trasferire solo le chiamate in attesa di consulenza.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Specifica se è possibile stabilire una chiamata completamente nuova da usare come chiamata consulta al trasferimento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



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

 

