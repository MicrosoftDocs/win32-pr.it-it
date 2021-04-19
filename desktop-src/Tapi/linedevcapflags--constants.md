---
description: Le \_ costanti dei flag di bit LINEDEVCAPFLAGS sono una raccolta di valori booleani che descrivono diverse funzionalità del dispositivo line.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Costanti LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332724"
---
# <a name="linedevcapflags_-constants"></a>\_Costanti LINEDEVCAPFLAGS

Le costanti dei flag di bit **LINEDEVCAPFLAGS \_** sono una raccolta di valori booleani che descrivono diverse funzionalità del dispositivo line.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**\_CALLHUB LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Indica se gli hub di chiamata sono supportati in questa riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**\_CALLHUBTRACKING LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Indica se la verifica dell'hub chiamate è supportata in questa riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**\_CLOSEDROP LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica cosa accade quando una linea aperta viene chiusa mentre l'applicazione ha chiamate attive sulla riga. Se **true**, il provider di servizi Elimina (Cancella) tutte le chiamate attive sulla riga quando l'ultima applicazione che ha aperto la riga la chiude con [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Se **false**, il provider di servizi non elimina le chiamate attive in tali casi. Al contrario, le chiamate rimangono attive e controllano i dispositivi esterni. Un provider di servizi imposta in genere questo bit su **false** se è presente un altro dispositivo che può mantenerla attiva. ad esempio, se una linea analoga ha il computer e il set di telefono entrambi si connettono direttamente a essi in una configurazione a livello di entità, il telefono Offhook manterrà automaticamente la chiamata attiva anche dopo il rallentamento del computer.

Le applicazioni devono selezionare questo flag per determinare se avvisare l'utente (con una finestra di dialogo OK/Annulla) che le chiamate attive andranno perse.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**\_CROSSADDRCONF LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se le chiamate su indirizzi diversi in questa riga possono essere contrattate.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**\_DIALBILLING LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**\_DIALDIALTONE LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**\_DIALQUIET LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Questi flag indicano se il modificatore di stringa componibile "$", "@" o "W" è supportato per una determinata periferica di linea. È **true** se il modificatore è supportato; in caso contrario, **false**. "?" (Richiedi all'utente di continuare la composizione) non è mai supportato da un dispositivo a linee. Questi flag consentono a un'applicazione di determinare prima di tutto i modificatori comportano la generazione di un LINEERR. Nell'applicazione è possibile scegliere di eseguire la pre-analisi delle stringhe che è possibile comporre per i caratteri non supportati o di passare la stringa "non elaborata" da [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) direttamente al provider come parte di funzioni quali [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e lasciare che la funzione generi un errore per indicare quale modificatore non supportato si verifica per primo nella stringa.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**\_HIGHLEVCOMP LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se in questa riga sono supportati gli elementi di informazioni sulla compatibilità di alto livello.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**\_LOWLEVCOMP LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se gli elementi di informazioni sulla compatibilità di basso livello sono supportati in questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**\_MEDIACONTROL LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se le operazioni di controllo del supporto sono disponibili per le chiamate a questa riga.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**\_msp LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Indica se un provider di servizi multimediali (MSP) è associato alla riga. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**\_MULTIPLEADDR LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Specifica se [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) è in grado di gestire più indirizzi contemporaneamente (come per il multiplexing inverso).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**\_PRIVATEOBJECTS LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Indica se le [interfacce specifiche del provider](./provider-specific-interfaces.md) sono state implementate. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


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

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

