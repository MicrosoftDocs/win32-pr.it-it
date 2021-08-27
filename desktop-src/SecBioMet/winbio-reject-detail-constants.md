---
title: WINBIO_REJECT_DETAIL costanti (Winbio \_ types.h)
description: Specificare il motivo per cui una procedura di acquisizione o identificazione di impronte digitali biometriche non è riuscita.
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
ms.openlocfilehash: ad5ac7a2f96555aa8ccfb305c66061ba4e0ffd468f18a1a93be215c367f034be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909349"
---
# <a name="winbio_reject_detail-constants"></a>Costanti WINBIO \_ REJECT \_ DETAIL

Le costanti seguenti possono essere usate per specificare il motivo per cui una procedura di acquisizione o identificazione di impronte digitali biometriche non è riuscita.



| Costante                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO \_ ALTO**</dt> </dl>                                                                  | La scansione delle dita è iniziata troppo in alto sul dito.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO \_ BASSO**</dt> </dl>                                                                     | La scansione delle dita è iniziata troppo in basso sul dito.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO A \_ SINISTRA**</dt> </dl>                                                                  | Il dito era troppo a sinistra durante la scansione.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO A \_ DESTRA**</dt> </dl>                                                               | Il dito era troppo a destra durante la scansione.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ FAST**</dt> </dl>                                                                  | Il dito è stato fatto scorrere troppo rapidamente sul sensore.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO \_ LENTO**</dt> </dl>                                                                  | Il dito è stato scorrere troppo lentamente sul sensore.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ FP \_ SCARSA \_ QUALITÀ**</dt> </dl>                                                      | La qualità dell'analisi era troppo bassa.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ SKEWED**</dt> </dl>                                                            | Il dito non è passato direttamente attraverso il sensore.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**FP WINBIO \_ \_ TROPPO \_ BREVE**</dt> </dl>                                                               | Il dito non è stato analizzato a sufficienza.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**ERRORE DI \_ MERGE FP WINBIO \_ \_**</dt> </dl>                                                   | Non è stato possibile combinare le acquisizioni di impronte digitali.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ RIFIUTARE \_ LA MASCHERA \_ ANTI \_ \_ SPOOFING DEI DETTAGLI**</dt> </dl> | Questa maschera copre gli 8 bit superiori del valore dei dettagli di rifiuto in cui si trovano i comportamenti di verifica della vita. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ RIFIUTARE \_ LA MASCHERA DI POSIZIONE DEI \_ \_ DETTAGLI**</dt> </dl>    | Questa maschera copre l'intervallo di bit dedicati agli errori di posizione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**MASCHERA MOTIVO DETTAGLI RIFIUTO WINBIO \_ \_ \_ \_**</dt> </dl>                       | Questa maschera copre i 16 bit inferiori in cui si trova il motivo enumerato del rifiuto. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**QUALITÀ SCADENTE DI WINBIO \_ \_ \_ IRIS**</dt> </dl>                                                | Le condizioni hanno causato l'acquisizione di un'immagine scadente da parte della fotocamera. Indicare all'utente di pulire il sensore ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ BRIGHT**</dt> </dl>                                                      | L'immagine include una quantità di luce ambientale troppo grande per ottenere una buona corrispondenza. Indicare all'utente di assicurarsi che non si trovano di fronte a un'altra sorgente di luce brillante. Questo valore è supportato a partire da Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ SCURO**</dt> </dl>                                                            | L'immagine è troppo scura per ottenere una corrispondenza. Indicare all'utente di assicurarsi che l'iris non sia nascosto da elementi come un velo, occhiali scuri o contatti colorati. Questo valore è supportato a partire da Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**RILEVATO SPOOFING DI WINBIO \_ IRIS \_ \_**</dt> </dl>                                          | Il componente di riconoscimento ritiene che l'iris non sia live, ma proviene da un feed video riprodotto, da una foto o da una svasata 3D. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ AMMORTIATO**</dt> </dl>                                                      | L'utente non sta guardando direttamente la fotocamera. Indicare all'utente di guardare direttamente la fotocamera ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ CHIUSO**</dt> </dl>                                                      | Le palpebre dell'utente stanno oscurando l'iris. Indicare all'utente di aprire gli occhi un po' di più ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ IRIS \_ GLARE**</dt> </dl>                                                                      | L'immagine include il bagliore dell'obiettivo. Indicare all'utente di rimuovere gli occhiali ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**OBIETTIVO DIRTY DI WINBIO \_ IRIS \_ \_**</dt> </dl>                                                      | L'obiettivo della fotocamera era dirty. Indicare all'utente di pulire l'obiettivo ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**WINBIO \_ IRIS \_ POOR \_ FOCUS**</dt> </dl>                                                      | Questo iris non è attivo. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**ORIENTAMENTO ERRATO DI WINBIO \_ \_ \_ IRIS**</dt> </dl>                                 | L'orientamento della fotocamera non corrisponde all'orientamento obbligatorio specificato dalla struttura [**\_ WINBIO EXTENDED SENSOR \_ \_ INFO.**](winbio-extended-sensor-info.md) Indicare all'utente di modificare l'orientamento della fotocamera ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ ALTO**</dt> </dl>                                                            | L'iris è rivolto verso l'alto. Indicare all'utente di cercare un po' verso il basso ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ BASSO**</dt> </dl>                                                               | L'iris è rivolto verso il basso. Indicare all'utente di cercare un po' ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO A \_ SINISTRA**</dt> </dl>                                                            | L'iris è troppo a sinistra. Indicare all'utente di cercare un po' più a destra ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO A \_ DESTRA**</dt> </dl>                                                         | L'iris è troppo a destra. Indicare all'utente di cercare un po' di più a sinistra ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ VICINO**</dt> </dl>                                                            | L'iris è troppo vicino alla fotocamera. Indicare all'utente di spostarsi un po' più lontano ed eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ IRIS \_ TROPPO \_ LONTANO**</dt> </dl>                                                               | L'iris è troppo lontano dalla fotocamera. Indicare all'utente di spostarsi un po' più vicino ed eseguire nuovamente l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ FACE \_ POOR \_ QUALITY**</dt> </dl>                                                | Le condizioni hanno causato l'acquisizione di un'immagine scadente da parte della fotocamera. Indicare all'utente di pulire il sensore ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ CHIARO**</dt> </dl>                                                      | L'immagine include una quantità di luce ambientale troppo grande per ottenere una corrispondenza. Indicare all'utente di assicurarsi che non si trovano di fronte a un'altra sorgente di luce. Questo valore è supportato a partire da Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ SCURO**</dt> </dl>                                                            | L'immagine è troppo scura per ottenere una corrispondenza. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**RILEVATO SPOOFING VISO WINBIO \_ \_ \_**</dt> </dl>                                          | Il componente di riconoscimento ritiene che il viso non sia live, ma proviene da un feed video riprodotto, da una foto o da una 3D. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**DESTINAZIONE AMBIGUA \_ VISO \_ WINBIO \_**</dt> </dl>                                    | Due o più visi si sovrappongono nel fotogramma della fotocamera. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ FACE \_ EYES \_ OCCLUDED**</dt> </dl>                                             | Gli occhi dell'utente sono occlusi. Indica all'utente di assicurarsi che gli occhi non siano nascosti da elementi come un discarica, gli occhiali scuri o i contatti colorati. Questo valore è supportato a partire da Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**VISO WINBIO \_ \_ CON ORIENTAMENTO \_ ERRATO**</dt> </dl>                                 | L'orientamento della fotocamera non corrisponde all'orientamento obbligatorio specificato dalla struttura [**\_ WINBIO EXTENDED SENSOR \_ \_ INFO.**](winbio-extended-sensor-info.md) Indica all'utente di modificare l'orientamento della fotocamera ed eseguire di nuovo la scansione. Questo valore è supportato a partire da Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ ALTO**</dt> </dl>                                                            | Il viso è rivolto verso l'alto. Indicare all'utente di guardare in basso ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ BASSO**</dt> </dl>                                                               | Il viso è rivolto verso il basso. Indicare all'utente di cercare un po' ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO A \_ SINISTRA**</dt> </dl>                                                            | Il viso è troppo a sinistra. Indicare all'utente di spostare un po' di più a destra ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ RIGHT**</dt> </dl>                                                         | Il viso è troppo a destra. Indicare all'utente di spostare un po' di più a sinistra ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ VICINO**</dt> </dl>                                                            | Il viso è troppo vicino alla fotocamera. Indicare all'utente di spostarsi un po' più lontano ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**VISO WINBIO \_ \_ TROPPO \_ LONTANO**</dt> </dl>                                                               | Il viso è troppo lontano dalla fotocamera. Indicare all'utente di avvicinarsi un po' di più ed eseguire di nuovo l'analisi. Questo valore è supportato a partire da Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                                                                                  |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





