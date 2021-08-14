---
title: Strutture XAudio2
description: Questa sezione contiene informazioni sulle strutture fornite dall'API Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcbdf454f282ca696a040aa7c1a3fe84c372ca4e0607c0a60f18b59d5f5e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962590"
---
# <a name="xaudio2-structures"></a>Strutture XAudio2

Questa sezione contiene informazioni sulle strutture fornite dall'API Microsoft XAudio2.



| Struttura                                                                                 | Descrizione                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Rappresenta un buffer di dati audio.<br/>                                                                                                    |
| [**XAUDIO2 \_ BUFFER \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Rappresenta un buffer di dati audio WMA.<br/>                                                                                                 |
| [**CONFIGURAZIONE DI DEBUG XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Imposta una nuova configurazione di debug globale per XAudio2 se usata dalla funzione SetDebugConfiguration.                                             |
| [**CATENA DI EFFETTI XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Definisce una catena di effetti.<br/>                                                                                                            |
| [**DESCRITTORE DELL'EFFETTO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Definisce un effetto.<br/>                                                                                                                  |
| [**PARAMETRI DI FILTRO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Definisce i parametri di filtro per una voce di origine.<br/>                                                                                       |
| [**DATI SULLE PRESTAZIONI DI XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera informazioni sulle prestazioni.<br/>                                                                                                  |
| [**DESCRITTORE DI INVIO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Descrive una destinazione di invio vocale.<br/>                                                                                                 |
| [**DETTAGLI DELLA VOCE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contiene informazioni sui flag di creazione, i canali di input e la frequenza di campionamento di una voce.<br/>                                          |
| [**XAUDIO2 \_ VOICE \_ SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Definisce un set di voci per ricevere dati da una singola voce di output.<br/>                                                                 |
| [**STATO VOCE \_ XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Restituisce i dati relativi allo stato corrente e alla posizione del cursore della voce.<br/>                                                                         |
| [**PARAMETRI \_ \_ I3DL2 DI XAUDIO2FX REVERB \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Descrive i parametri I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) da usare nella funzione ReverbConvertI3DL2ToNative.           |
| [**PARAMETRI REVERB XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Descrive i parametri da usare nell'APO di riverbero.                                                                                                |
| [**LIVELLI VOLUMEMETRI XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Descrive i parametri da usare con il contatore del volume APO.                                                                                        |
| [**PARAMETRI DEL \_ BUFFER LOCKFORPROCESS XAPO \_ \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Definisce i parametri del buffer che rimangono costanti mentre un oggetto XAPO è bloccato.<br/>                                                             |
| [**PARAMETRI DEL \_ BUFFER DEL PROCESSO XAPO \_ \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Definisce i parametri del buffer che possono cambiare da una chiamata a quella successiva.<br/>                                                                |
| [**PROPRIETÀ DI REGISTRAZIONE \_ \_ XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Descrive le caratteristiche generali di un XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parametri di inizializzazione da usare con FXECHO XAPO.<br/>                                                                             |
| [**PARAMETRI \_ FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parametri da usare con FXECHO XAPO.<br/>                                                                                            |
| [**PARAMETRI \_ FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parametri da usare con FXEQ XAPO.<br/>                                                                                              |
| [**PARAMETRI FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parametri da usare con FXMasteringLimiter XAPO.<br/>                                                                                |
| [**PARAMETRI \_ FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parametri da usare con FXReverb XAPO.<br/>                                                                                          |
| [**CONO X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Specifica la direzionalità per un emettitore non LFE a canale singolo ridimensionando il comportamento DSP rispetto all'orientamento dell'emettitore.<br/>    |
| [**CURVA DI DISTANZA X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Definisce una curva esplicita a senso orizzontale costituito da segmenti lineari, definendo direttamente il comportamento DSP rispetto alla distanza normalizzata.<br/> |
| [**PUNTO CURVA DI DISTANZA X3DAUDIO \_ \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Definisce un'impostazione DSP a una determinata distanza normalizzata.<br/>                                                                               |
| [**IMPOSTAZIONI \_ DSP X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Riceve i risultati da una chiamata a X3DAudioCalculate.<br/>                                                                              |
| [**EMETTITORE X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Definisce un'origine audio 3D singola o multi-punto usata con un numero arbitrario di canali audio.<br/>                                    |
| [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Definisce un punto di ricezione audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




