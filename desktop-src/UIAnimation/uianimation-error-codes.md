---
title: Codici di errore dell'animazione Windows (Winerror. h)
description: Se si verifica un errore, l'animazione di Windows restituisce un codice come valore HRESULT. In questa sezione viene fornito un elenco di codici di errore specifici dell'animazione Windows. Per un elenco di codici di errore COM generali, vedere codici di errore COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301500"
---
# <a name="windows-animation-error-codes"></a>Codici di errore dell'animazione Windows

Se si verifica un errore, l'animazione di Windows restituisce un codice come valore **HRESULT** . In questa sezione viene fornito un elenco di codici di errore specifici dell'animazione Windows. Per un elenco di codici di errore COM generali, vedere [codici di errore com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**creazione dell'interfaccia utente \_ E \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Impossibile creare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**interfaccia utente \_ E \_ chiusura \_ chiamata**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Il metodo [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) è stato chiamato sul gestore delle animazioni, causando l'arresto di gestione animazioni e tutte le variabili di animazione e gli storyboard creati per essere rilasciati.

> [!Note]  
> Non è possibile chiamare metodi su alcun oggetto di animazione dopo l' [**arresto**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**interfaccia utente E rientranza non \_ \_ valida \_**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Questo metodo non può essere chiamato durante questo tipo di callback.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**interfaccia utente \_ E \_ oggetto \_ sealed**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Questo oggetto è stato sealed, quindi questa modifica non è più consentita.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**valore dell'interfaccia utente \_ E \_ \_ non \_ impostato**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



Il valore richiesto non è mai stato impostato e pertanto non può essere recuperato.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**valore dell'interfaccia utente \_ E \_ \_ non \_ determinato**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



Impossibile determinare il valore richiesto.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**OUTPUT dell'interfaccia utente \_ E \_ non valido \_**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Un callback ha restituito un parametro di output non valido.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**prevista l'interfaccia utente \_ E un \_ valore booleano \_**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Un callback ha restituito un codice di esito positivo diverso da S \_ OK o s \_ false.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**interfaccia \_ utente \_ E \_ proprietario diverso**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Un parametro che deve essere di proprietà di questo oggetto è di proprietà di un oggetto diverso.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**interfaccia \_ utente \_ E \_ corrispondenza ambigua**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Più di un elemento corrisponde ai criteri di ricerca.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**OVERFLOW dell'interfaccia utente \_ E \_ FP \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Si è verificato un overflow a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**\_thread UI E \_ errato \_**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Questo metodo può essere chiamato solo dal thread che ha creato l'oggetto.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**interfaccia utente \_ E \_ Storyboard \_ attivi**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



Lo storyboard è attualmente nella pianificazione.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**STORYBOARD dell'interfaccia utente \_ E \_ non in \_ \_ esecuzione**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



Lo storyboard non viene riprodotto.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**interfaccia utente \_ E \_ inizio \_ fotogramma chiave \_ dopo la \_ fine**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



Il fotogramma chiave iniziale potrebbe verificarsi dopo il fotogramma chiave End.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**fotogramma chiave dell'interfaccia utente \_ E \_ fine \_ \_ non \_ determinato**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Potrebbe non essere possibile determinare l'ora di fine del fotogramma chiave quando viene raggiunto il fotogramma chiave di avvio.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_sovrapposizione di \_ cicli dell'interfaccia utente \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Due parti ripetute di uno storyboard potrebbero sovrapporsi.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**transizione interfaccia utente \_ E \_ già in \_ \_ uso**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



La transizione è già stata aggiunta a uno storyboard diverso oppure è stata aggiunta a uno storyboard che ha terminato la riproduzione ed è stata rilasciata.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**transizione dell'interfaccia utente \_ E \_ \_ non \_ nello \_ storyboard**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



La transizione non è stata aggiunta ad alcun Storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transizione dell'interfaccia utente \_ E \_ \_ eclissata**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



La transizione potrebbe eclissare l'inizio di un'altra transizione nello storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**interfaccia utente \_ E \_ tempo prima dell' \_ \_ ultimo \_ aggiornamento**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



L'ora specificata è precedente all'ora passata all'ultimo aggiornamento.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_client timer interfaccia utente E \_ \_ \_ già \_ connesso**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Questo client è già connesso a un timer.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                       |
| Intestazione<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)
</dt> </dl>

 

