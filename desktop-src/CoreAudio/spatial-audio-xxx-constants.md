---
description: Le costanti SPATIAL \_ AUDIO XXX definiscono i valori correlati alle funzionalità del suono \_ spaziale.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: SPATIAL_AUDIO_XXX costanti (SpatialAudioMetadata.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db363260b21f47676c12aeb5eaf3c10149b571ed2771a4d9f907e98b0ba17aed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018249"
---
# <a name="spatial_audio_xxx-constants"></a>Costanti SPATIAL \_ AUDIO \_ XXX

Le costanti SPATIAL \_ AUDIO XXX definiscono i valori correlati alle funzionalità del suono \_ spaziale.



| Costante/valore                                                                                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**SPAZIALE \_ POSIZIONE \_ AUDIO**</dt> <dt>200</dt> </dl>                                                   | Comando di metadati audio spaziali standard definito da Microsoft che rappresenta la posizione del listener nel modello standard usato da [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in cui la testa del listener è posizionata in corrispondenza delle coordinate (0,0,0), definite in metri.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**SPAZIALE \_ AUDIO \_ POSITION \_ BYTE \_ COUNT**</dt> <dt>sizeof(float) \* 3</dt> </dl> | Specifica le dimensioni del valore **SPATIAL \_ AUDIO \_ POSITION.**<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**SPAZIALE \_ COMANDI \_ STANDARD AUDIO \_ \_ START**</dt> <dt>200</dt> </dl>    | Specifica l'inizio dell'intervallo di comandi di metadati audio spaziali riservati da Microsoft. I comandi dei metadati personalizzati sono limitati agli ID dei comandi da 0 a 199. I comandi da 200 a 255 sono riservati per l'uso da parte di Microsoft.<br/>                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>SpatialAudioMetadata.h</dt> </dl> |



 

 




