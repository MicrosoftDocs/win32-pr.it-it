---
description: Le costanti del flag di bit LINEDEVCAPFLAGS sono una raccolta di valori booleani che \_ descrivono varie funzionalità del dispositivo linea.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761718"
---
# <a name="linedevcapflags_-constants"></a>Costanti LINEDEVCAPFLAGS \_

Le costanti del flag di bit **LINEDEVCAPFLAGS \_** sono una raccolta di valori booleani che descrivono varie funzionalità del dispositivo linea.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indica se gli hub chiamate sono supportati in questa riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indica se il rilevamento dell'hub chiamate è supportato in questa riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Specifica cosa accade quando una riga aperta viene chiusa mentre l'applicazione ha chiamate attive sulla riga. Se **TRUE,** il provider di servizi elimina (cancella) tutte le chiamate attive sulla riga quando l'ultima applicazione che ha aperto la riga la chiude con [**lineClose.**](/windows/desktop/api/Tapi/nf-tapi-lineclose) Se **FALSE,** il provider di servizi non elimina le chiamate attive in questi casi. Al contrario, le chiamate rimangono attive e sotto il controllo dei dispositivi esterni. Un provider di servizi imposta in genere questo bit su **FALSE** se è presente un altro dispositivo in grado di mantenere attiva la chiamata, ad esempio se una linea analoga ha il computer e il telefono impostati entrambi per connettersi direttamente a essi in una configurazione party-line, il telefono offhook manterà automaticamente la chiamata attiva anche dopo che il computer si è spento.

Le applicazioni devono controllare questo flag per determinare se avvisare l'utente (con una finestra di dialogo OK/Annulla) che le chiamate attive andranno perse.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Specifica se le chiamate su indirizzi diversi in questa riga possono essere conferenze.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Questi flag indicano se il modificatore di stringa selezionabile "$", "@" o "W" è supportato per un determinato dispositivo di linea. È TRUE **se** il modificatore è supportato. in caso contrario, **FALSE.** L'oggetto "?" (richiedere all'utente di continuare la composizione) non è mai supportato da un dispositivo di linea. Questi flag consentono a un'applicazione di determinare in anticipo quali modificatori avrebbero comportato la generazione di un oggetto LINEERR. L'applicazione può scegliere di pre-analizzare le stringhe dialable per i caratteri non supportati o di passare la stringa "raw" da [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) direttamente al provider come parte di funzioni come [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e consentire alla funzione di generare un errore per indicare quale modificatore non supportato si verifica per primo nella stringa.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Specifica se gli elementi di informazioni di compatibilità di alto livello sono supportati in questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Specifica se gli elementi di informazioni sulla compatibilità di basso livello sono supportati in questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Specifica se le operazioni di controllo multimediale sono disponibili per le chiamate a questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Indica se un provider di servizi multimediali (MSP) è associato alla riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Specifica se [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) [**lineDial,**](/windows/desktop/api/Tapi/nf-tapi-linedial) [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) è in grado di gestire più indirizzi contemporaneamente (come per il multiplexing inverso).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**OGGETTI PRIVATI LINEDEVCAPFLAGS \_**
</dt> <dd> <dl> <dt>



Indica se sono [state implementate interfacce specifiche](./provider-specific-interfaces.md) del provider. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


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

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

