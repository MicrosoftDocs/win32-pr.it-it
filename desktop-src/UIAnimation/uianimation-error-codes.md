---
title: Windows Codici di errore di animazione (Winerror.h)
description: Se si verifica un errore, Windows animation restituisce un codice come valore HRESULT. Questa sezione fornisce un elenco di codici di errore specifici per l'Windows animazione. Per un elenco di codici di errore COM generali, vedere Codici di errore COM.
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
ms.openlocfilehash: 44d725874de9c511558cef6ebbe8652905a7f5dac6372230385eaa3253ba3454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513661"
---
# <a name="windows-animation-error-codes"></a>Windows Codici di errore di animazione

Se si verifica un errore, Windows animation restituisce un codice come **valore HRESULT.** Questa sezione fornisce un elenco di codici di errore specifici per l'Windows animazione. Per un elenco dei codici di errore COM generali, vedere [Codici di errore COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**CREAZIONE \_ DELL'INTERFACCIA UTENTE \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Impossibile creare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**CHIAMATA \_ DELL'ARRESTO E \_ \_ DELL'INTERFACCIA UTENTE**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Il [**metodo Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) è stato chiamato nel gestore dell'animazione, causando l'arresto del gestore dell'animazione e il rilascio di tutte le variabili di animazione e gli storyboard creati.

> [!Note]  
> Non è possibile chiamare alcun metodo su qualsiasi oggetto di animazione dopo [**l'arresto.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**REENTRANCY NON VALIDA \_ \_ \_ DELL'INTERFACCIA UTENTE**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Questo metodo non può essere chiamato durante questo tipo di callback.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**SEALED \_ DELL'OGGETTO E \_ \_ DELL'INTERFACCIA UTENTE**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Questo oggetto è stato bloccato, quindi questa modifica non è più consentita.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**VALORE \_ E \_ DELL'INTERFACCIA \_ UTENTE NON \_ IMPOSTATO**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



Il valore richiesto non è mai stato impostato e pertanto non può essere recuperato.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**VALORE \_ E \_ DELL'INTERFACCIA \_ UTENTE NON \_ DETERMINATO**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



Impossibile determinare il valore richiesto.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**OUTPUT \_ DELL'INTERFACCIA UTENTE E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Un callback ha restituito un parametro di output non valido.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**PREVISTO \_ VALORE BOOLEANO E \_ \_ DELL'INTERFACCIA UTENTE**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Un callback ha restituito un codice di esito positivo diverso da S \_ OK o S \_ FALSE.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**INTERFACCIA \_ UTENTE E PROPRIETARIO \_ \_ DIVERSO**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Un parametro che deve essere di proprietà di questo oggetto è di proprietà di un oggetto diverso.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**CORRISPONDENZA \_ AMBIGUA DELL'INTERFACCIA \_ \_ UTENTE**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Più di un elemento corrisponde ai criteri di ricerca.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**OVERFLOW \_ FP dell'interfaccia \_ utente E \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Si è verificato un overflow a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**INTERFACCIA \_ UTENTE E THREAD \_ \_ ERRATO**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Questo metodo può essere chiamato solo dal thread che ha creato l'oggetto .


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI \_ E \_ STORYBOARD \_ ACTIVE**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



Lo storyboard è attualmente in fase di pianificazione.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**STORYBOARD \_ E \_ DELL'INTERFACCIA UTENTE NON IN \_ \_ RIPRODUZIONE**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



Lo storyboard non viene riprodotto.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**FOTOGRAMMI \_ CHIAVE DI AVVIO \_ DELL'INTERFACCIA UTENTE \_ E DOPO LA \_ \_ FINE**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



Il fotogramma chiave iniziale potrebbe verificarsi dopo il fotogramma chiave finale.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**FOTOGRAMMA \_ CHIAVE FINALE \_ DELL'INTERFACCIA UTENTE E NON \_ \_ \_ DETERMINATO**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Potrebbe non essere possibile determinare l'ora del fotogramma chiave finale quando viene raggiunto il fotogramma chiave iniziale.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**SOVRAPPOSIZIONE \_ DEI CICLI E \_ \_ DELL'INTERFACCIA UTENTE**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Due parti ripetute di uno storyboard potrebbero sovrapporsi.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**TRANSIZIONE \_ E \_ DELL'INTERFACCIA UTENTE GIÀ \_ \_ USATA**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



La transizione è già stata aggiunta a uno storyboard diverso o è stata aggiunta a uno storyboard che ha terminato la riproduzione e il rilascio.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**TRANSIZIONE \_ DELL'INTERFACCIA UTENTE E \_ NON NELLO \_ \_ \_ STORYBOARD**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



La transizione non è stata aggiunta ad alcuno storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**TRANSIZIONE \_ E DELL'INTERFACCIA \_ UTENTE \_ ECLISSATA**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



La transizione potrebbe eclissare l'inizio di un'altra transizione nello storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**ORA \_ E \_ DELL'INTERFACCIA \_ UTENTE PRIMA \_ DELL'ULTIMO \_ AGGIORNAMENTO**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



L'ora specificata è precedente a quella passata all'ultimo aggiornamento.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**CLIENT \_ TIMER E \_ \_ DELL'INTERFACCIA \_ UTENTE GIÀ \_ CONNESSO**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Questo client è già connesso a un timer.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista e l'aggiornamento della piattaforma solo per Windows app desktop di Vista \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                       |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)
</dt> </dl>

 

