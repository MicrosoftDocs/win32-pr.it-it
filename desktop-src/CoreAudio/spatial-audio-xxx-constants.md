---
description: Le \_ \_ costanti xxx audio spaziali definiscono i valori relativi alle funzionalità audio spaziali.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Costanti SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331295"
---
# <a name="spatial_audio_xxx-constants"></a>\_ \_ Costanti xxx audio spaziali

Le \_ \_ costanti xxx audio spaziali definiscono i valori relativi alle funzionalità audio spaziali.



| Costante/valore                                                                                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**Spaziale \_ \_Posizione AUDIO**</dt> <dt>200</dt> </dl>                                                   | Comando standard di metadati audio spaziali definito da Microsoft che rappresenta la posizione del listener nel modello standard usato da [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in cui la testa del listener è posizionata in corrispondenza delle coordinate (0, 0, 0), definita in metri.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**Spaziale \_ \_ \_ \_ Conteggio byte posizione audio**</dt> <dt>sizeof (float) \* 3</dt> </dl> | Specifica la dimensione del valore **della \_ \_ posizione audio spaziale** .<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**Spaziale \_ \_Comandi audio \_ standard \_ avviati**</dt> <dt>200</dt> </dl>    | Specifica l'inizio dell'intervallo dei comandi di metadati audio spaziali riservati a Microsoft. I comandi dei metadati personalizzati sono limitati agli ID di comando 0-199. I comandi 200-255 sono riservati per l'uso da Microsoft.<br/>                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>SpatialAudioMetadata. h</dt> </dl> |



 

 




