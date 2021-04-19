---
description: Le \_ costanti del flag di bit PHONESTATE descrivono vari elementi di stato per un dispositivo telefonico.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Costanti PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326145"
---
# <a name="phonestate_-constants"></a>\_Costanti PHONESTATE

Le costanti del flag di bit **PHONESTATE \_** descrivono vari elementi di stato per un dispositivo telefonico.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**\_CAPSCHANGE PHONESTATE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) sono stati modificati. Per leggere la struttura aggiornata, l'applicazione deve usare [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) . Se un provider di servizi invia un messaggio di [**\_ stato telefonico**](phone-state.md) che contiene questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che trattano una versione precedente dell'API riceveranno \_ messaggi di stato del telefono che specificano PHONESTATE \_ reinit, che richiedono l'arresto e la reinizializzazione della connessione a TAPI per ottenere le informazioni aggiornate.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ connesso**
</dt> <dd> <dl> <dt>



La connessione tra il dispositivo telefonico e TAPI è stata appena creata. Questo errore si verifica quando viene richiamato TAPI o quando il cavo di connessione del telefono al PC viene collegato con TAPI Active.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**\_DEVSPECIFIC PHONESTATE**
</dt> <dd> <dl> <dt>



Le informazioni specifiche del dispositivo del telefono sono state modificate.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ disconnesso**
</dt> <dd> <dl> <dt>



La connessione tra il dispositivo telefonico e TAPI è stata interrotta. Questo problema si verifica quando il cavo collegato al PC viene scollegato quando il dispositivo è attivo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**\_visualizzazione PHONESTATE**
</dt> <dd> <dl> <dt>



La visualizzazione del telefono è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**\_HANDSETGAIN PHONESTATE**
</dt> <dd> <dl> <dt>



L'impostazione del guadagno del microfono del telefono è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**\_HANDSETHOOKSWITCH PHONESTATE**
</dt> <dd> <dl> <dt>



Lo stato del hookswitch del portatile è stato modificato.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**\_HANDSETVOLUME PHONESTATE**
</dt> <dd> <dl> <dt>



L'impostazione del volume altoparlante del ricevitore è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**\_HEADSETHOOKSWITCH PHONESTATE**
</dt> <dd> <dl> <dt>



Lo stato hookswitch dell'auricolare è stato modificato.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**\_HEADSETGAIN PHONESTATE**
</dt> <dd> <dl> <dt>



L'impostazione del guadagno del microfono dell'auricolare è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**\_HEADSETVOLUME PHONESTATE**
</dt> <dd> <dl> <dt>



L'impostazione del volume speaker dell'auricolare è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lampada PHONESTATE**
</dt> <dd> <dl> <dt>



Una lampada del telefono è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_monitoraggi PHONESTATE**
</dt> <dd> <dl> <dt>



Numero di monitoraggi per il dispositivo telefonico.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ altro**
</dt> <dd> <dl> <dt>



Gli elementi di stato del telefono diversi da quelli elencati di seguito sono stati modificati. L'applicazione deve controllare lo stato corrente del telefono per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_proprietario PHONESTATE**
</dt> <dd> <dl> <dt>



Numero di proprietari del dispositivo telefonico.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE \_ REinit**
</dt> <dd> <dl> <dt>



Gli elementi sono stati modificati nella configurazione dei dispositivi telefonici. Per acquisire familiarità con queste modifiche, come per l'aspetto dei nuovi dispositivi telefonici, l'applicazione deve reinizializzare l'uso di TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ rimosso**
</dt> <dd> <dl> <dt>



Indica che il dispositivo è stato rimosso dal sistema dal provider di servizi (più probabile tramite l'azione dell'utente, tramite un pannello di controllo o un'utilità simile). Un messaggio di [**\_ stato telefonico**](phone-state.md) con questo valore sarà in genere seguito immediatamente da un messaggio di [**\_ chiusura del telefono**](phone-close.md) sul dispositivo. I tentativi successivi di accesso al dispositivo prima della reinizializzazione di TAPI comporteranno \_ la restituzione di PHONEERR NODEVICE all'applicazione. Se un provider di servizi invia un \_ messaggio di stato telefonico che contiene questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**Riprendi PHONESTATE \_**
</dt> <dd> <dl> <dt>



L'uso dell'applicazione del dispositivo telefonico viene ripreso dopo essere stato sospeso per un certo periodo di tempo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**\_RINGMODE PHONESTATE**
</dt> <dd> <dl> <dt>



La modalità suoneria del telefono è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**\_RINGVOLUME PHONESTATE**
</dt> <dd> <dl> <dt>



Il volume dell'anello del telefono è stato modificato.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**\_SPEAKERHOOKSWITCH PHONESTATE**
</dt> <dd> <dl> <dt>



Lo stato hookswitch del dispositivo vivavoce è stato modificato.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**\_SPEAKERGAIN PHONESTATE**
</dt> <dd> <dl> <dt>



Lo stato dell'impostazione di miglioramento del microfono del dispositivo vivavoce è stato modificato.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**\_SPEAKERVOLUME PHONESTATE**
</dt> <dd> <dl> <dt>



L'impostazione del volume speaker del dispositivo vivavoce è cambiata.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**\_sospensione PHONESTATE**
</dt> <dd> <dl> <dt>



L'uso del telefono da parte dell'applicazione è temporaneamente sospeso.


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

[**\_chiusura telefono**](phone-close.md)
</dt> <dt>

[**\_stato telefono**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




