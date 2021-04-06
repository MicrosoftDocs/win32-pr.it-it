---
title: Strutture XAudio2
description: Questa sezione contiene informazioni sulle strutture fornite dall'API Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759476"
---
# <a name="xaudio2-structures"></a>Strutture XAudio2

Questa sezione contiene informazioni sulle strutture fornite dall'API Microsoft XAudio2.



| Struttura                                                                                 | Descrizione                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Rappresenta un buffer di dati audio.<br/>                                                                                                    |
| [**\_Buffer XAUDIO2 \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Rappresenta un buffer di dati audio WMA.<br/>                                                                                                 |
| [**\_Configurazione di debug XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Imposta una nuova configurazione di debug globale per XAudio2 se utilizzata dalla funzione SetDebugConfiguration.                                             |
| [**\_Catena di effetti XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Definisce una catena di effetti.<br/>                                                                                                            |
| [**\_Descrittore dell'effetto XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Definisce un effetto.<br/>                                                                                                                  |
| [**\_Parametri del filtro XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Definisce i parametri di filtro per una voce di origine.<br/>                                                                                       |
| [**\_Dati sulle prestazioni di XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera le informazioni sulle prestazioni.<br/>                                                                                                  |
| [**\_Descrittore di trasmissione XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Descrive una destinazione di trasmissione vocale.<br/>                                                                                                 |
| [**\_Dettagli voce \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contiene informazioni sui flag di creazione, i canali di input e la frequenza di campionamento di una voce.<br/>                                          |
| [**XAUDIO2 \_ \_ invio vocale**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Definisce un set di voci per la ricezione di dati da una singola voce di output.<br/>                                                                 |
| [**\_Stato XAUDIO2 Voice \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Restituisce i dati relativi allo stato corrente e alla posizione del cursore della voce.<br/>                                                                         |
| [**Parametri di I3DL2 per XAUDIO2FX \_ Reverb \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Descrive i parametri I3DL2 (Interactive 3D audio rendering Guidelines Level 2,0) da usare nella funzione ReverbConvertI3DL2ToNative.           |
| [**XAUDIO2FX \_ parametri del riverbero \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Vengono descritti i parametri per l'utilizzo nel Reverb APO.                                                                                                |
| [**\_Livelli di VOLUMEMETER XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Descrive i parametri da usare con il contatore del volume APO.                                                                                        |
| [**\_parametri del \_ buffer \_ LOCKFORPROCESS XAPO**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Definisce i parametri del buffer che rimangono costanti mentre un XAPO è bloccato.<br/>                                                             |
| [**\_parametri del \_ buffer del processo XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Definisce i parametri del buffer che possono cambiare da una chiamata a quella successiva.<br/>                                                                |
| [**\_Proprietà registrazione \_ XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Descrive le caratteristiche generali di un XAPO.<br/>                                                                                       |
| [**\_INITDATA FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parametri di inizializzazione da utilizzare con FXECHO XAPO.<br/>                                                                             |
| [**\_parametri FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parametri da usare con il XAPO FXECHO.<br/>                                                                                            |
| [**\_parametri FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parametri da usare con il XAPO FXEQ.<br/>                                                                                              |
| [**\_parametri FXMASTERINGLIMITER**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parametri da usare con il XAPO FXMasteringLimiter.<br/>                                                                                |
| [**\_parametri FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parametri da usare con il XAPO FXReverb.<br/>                                                                                          |
| [**\_Cono X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Specifica la direzionalità per un emettitore non LFE a canale singolo scalando il comportamento di DSP rispetto all'orientamento dell'emittente.<br/>    |
| [**\_Curva distanza \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Definisce una curva a tratti esplicita costituita da segmenti lineari, definendo direttamente il comportamento di DSP rispetto alla distanza normalizzata.<br/> |
| [**\_ \_ Punto curva distanza \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Definisce un'impostazione DSP a una distanza normalizzata specificata.<br/>                                                                               |
| [**\_Impostazioni DSP \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Riceve i risultati da una chiamata a X3DAudioCalculate.<br/>                                                                              |
| [**X3DAUDIO \_ emettitore**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Definisce un'origine audio 3D singola o multipunto utilizzata con un numero arbitrario di canali audio.<br/>                                    |
| [**\_Listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Definisce un punto di ricezione audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




