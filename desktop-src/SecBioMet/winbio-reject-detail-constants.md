---
title: Costanti WINBIO_REJECT_DETAIL (tipi WinBio \_ . h)
description: Specificare il motivo per cui un'acquisizione o una procedura di identificazione delle impronte digitali biometriche non è riuscita.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743863"
---
# <a name="winbio_reject_detail-constants"></a>WINBIO \_ le \_ costanti di dettaglio di rifiuto

È possibile usare le costanti seguenti per specificare il motivo per cui un'acquisizione o una procedura di identificazione delle impronte digitali biometriche ha avuto esito negativo.



| Costante                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ alta**</dt> </dl>                                                                  | L'analisi del dito è iniziata troppo alta sul dito.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ basso**</dt> </dl>                                                                     | L'analisi del dito è iniziata troppo bassa sul dito.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ troppo a \_ sinistra**</dt> </dl>                                                                  | Il dito è rimasto troppo a lungo durante l'analisi.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ troppo a \_ destra**</dt> </dl>                                                               | Il dito è troppo lungo durante l'analisi.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ veloce**</dt> </dl>                                                                  | Il dito è stato troppo rapidamente nel sensore.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ lento**</dt> </dl>                                                                  | Il dito è stato troppo lentamente sul sensore.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ FP \_ scarsa \_ qualità**</dt> </dl>                                                      | La qualità della scansione è troppo insufficiente.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ sbilanciato**</dt> </dl>                                                            | Il dito non è passato direttamente nel sensore.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ troppo \_ breve**</dt> </dl>                                                               | Il dito non è stato analizzato.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**\_errore di \_ merge WINBIO FP \_**</dt> </dl>                                                   | Non è stato possibile combinare le acquisizioni delle impronte digitali.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ RIFIUTO \_ \_ \_ \_ maschera dettagli anti spoofing**</dt> </dl> | Questa maschera copre gli 8 bit superiori del valore del dettaglio di rifiuto in cui si trovano i comportamenti di prova di vita. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ \_maschera di \_ posizionamento \_ di rifiuto dettagli**</dt> </dl>    | Questa maschera copre l'intervallo di bit dedicato alla posizione degli errori. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**\_maschera del \_ \_ motivo per i dettagli del rifiuto WINBIO \_**</dt> </dl>                       | Questa maschera copre i 16 bit inferiori in cui si trova il motivo enumerato per il rifiuto. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**\_ \_ qualità scadente di WINBIO Iris \_**</dt> </dl>                                                | Le condizioni hanno causato l'acquisizione di un'immagine insufficiente da parte della fotocamera. Indicare all'utente di pulire il sensore e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ luminosa**</dt> </dl>                                                      | L'immagine include una quantità eccessiva di luce ambientale per ottenere una corrispondenza corretta. Indicare all'utente di assicurarsi che non si trovino in un'altra sorgente luminosa. Questo valore è supportato a partire da Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ scuro**</dt> </dl>                                                            | L'immagine è troppo scura per ottenere una corrispondenza corretta. Indicare all'utente di assicurarsi che l'iride non sia nascosta da elementi come un velo, occhiali scuri o contatti colorati. Questo valore è supportato a partire da Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**\_ \_ rilevato spoofing Iris \_ WINBIO**</dt> </dl>                                          | Il componente di riconoscimento ritiene che Iris non sia attivo, ma provenga da un feed video riprodotto, una foto o una scultura 3D. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ asimmetrica**</dt> </dl>                                                      | L'utente non sta cercando direttamente la fotocamera. Indicare all'utente di eseguire la ricerca direttamente nella fotocamera e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ chiuso**</dt> </dl>                                                      | Le palpebre dell'utente nascondono l'iride. Chiedere all'utente di aprire gli occhi e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**\_ \_ abbagliamento Iris WINBIO**</dt> </dl>                                                                      | L'immagine include l'abbagliamento della lente. Indicare all'utente di rimuovere gli occhiali e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**WINBIO \_ Iris \_ Dirty \_ Lens**</dt> </dl>                                                      | L'obiettivo della fotocamera è stato modificato. Indicare all'utente di pulire l'obiettivo ed eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**WINBIO \_ Iris \_ insufficiente \_**</dt> </dl>                                                      | Questo Iris non è attivo. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**\_ \_ orientamento errato WINBIO \_ Iris**</dt> </dl>                                 | L'orientamento della fotocamera non corrisponde all'orientamento obbligatorio specificato dalla struttura di [**\_ \_ \_ informazioni del sensore esteso WINBIO**](winbio-extended-sensor-info.md) . Indicare all'utente di modificare l'orientamento della fotocamera e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ alta**</dt> </dl>                                                            | L'iride è rivolte verso l'alto. Indicare all'utente di cercare un po' e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ bassa**</dt> </dl>                                                               | L'iride è rivolta verso il basso. Indicare all'utente di cercare un po' e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ Iris \_ troppo a \_ sinistra**</dt> </dl>                                                            | L'iride è troppo lontano a sinistra. Chiedere all'utente di esaminare più a destra e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ Iris \_ a \_ destra**</dt> </dl>                                                         | Il diaframma è troppo lontano a destra. Chiedere all'utente di esaminare di nuovo la sinistra e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ vicino**</dt> </dl>                                                            | Il diaframma è troppo vicino alla fotocamera. Chiedere all'utente di spostarsi più a fondo e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ Iris \_ troppo \_ lontano**</dt> </dl>                                                               | Il diaframma è troppo lontano dalla fotocamera. Chiedere all'utente di spostarsi più a breve e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ faccia \_ scarsa \_ qualità**</dt> </dl>                                                | Le condizioni hanno causato l'acquisizione di un'immagine insufficiente da parte della fotocamera. Indicare all'utente di pulire il sensore e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO \_ faccia \_ troppo \_ luminosa**</dt> </dl>                                                      | L'immagine include una quantità eccessiva di luce ambientale per ottenere una corrispondenza corretta. Indicare all'utente di assicurarsi che non si trovino in un'altra sorgente luminosa. Questo valore è supportato a partire da Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO \_ faccia \_ troppo \_ scura**</dt> </dl>                                                            | L'immagine è troppo scura per ottenere una corrispondenza corretta. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**\_ \_ rilevato spoofing della faccia WINBIO \_**</dt> </dl>                                          | Il componente di riconoscimento ritiene che il volto non sia attivo, ma provenga da un feed video riprodotto, una foto o una scultura 3D. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_ \_ destinazione ambigua WINBIO Face \_**</dt> </dl>                                    | Due o più visi si sovrappongono nel frame della fotocamera. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ faccia \_ occhi \_ bloccati**</dt> </dl>                                             | Gli occhi dell'utente sono bloccati. Indicare all'utente di assicurarsi che gli occhi non siano nascosti da elementi come un velo, occhiali scuri o contatti colorati. Questo valore è supportato a partire da Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**\_orientamento WINBIO volto \_ errato \_**</dt> </dl>                                 | L'orientamento della fotocamera non corrisponde all'orientamento obbligatorio specificato dalla struttura di [**\_ \_ \_ informazioni del sensore esteso WINBIO**](winbio-extended-sensor-info.md) . Indicare all'utente di modificare l'orientamento della fotocamera e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO \_ faccia \_ troppo \_ alta**</dt> </dl>                                                            | Il volto è rivolto verso l'alto. Indicare all'utente di cercare un po' e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**WINBIO \_ faccia \_ troppo \_ bassa**</dt> </dl>                                                               | Il volto è rivolto verso il basso. Indicare all'utente di cercare un po' e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ faccia \_ \_ sinistra**</dt> </dl>                                                            | Il volto è troppo lontano a sinistra. Chiedere all'utente di spostare leggermente a destra e di eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ faccia \_ troppo a \_ destra**</dt> </dl>                                                         | Il volto è troppo lontano a destra. Indicare all'utente di spostare leggermente più a sinistra e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO \_ \_ troppo \_ vicino**</dt> </dl>                                                            | Il volto è troppo vicino alla fotocamera. Chiedere all'utente di spostarsi più a fondo e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO \_ faccia \_ troppo a \_ lungo**</dt> </dl>                                                               | Il volto è troppo lontano dalla fotocamera. Chiedere all'utente di spostarsi più a breve e di eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                                                                                  |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





