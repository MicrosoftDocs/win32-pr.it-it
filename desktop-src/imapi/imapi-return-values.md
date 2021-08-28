---
title: Valori restituiti IMAPI (Imapi2error.h)
description: I metodi IMAPI restituiscono valori non negativi, in genere S \_ OK, se il metodo ha avuto esito positivo. I metodi IMAPI restituiscono codici di esito positivo o di errore da Winerror.h, Imapi2error.h o Imapi2fserror.h in caso di errore.
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857f9c018fc34a16a0dc431714aacc1fcdf6a5b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474797"
---
# <a name="imapi-return-values"></a>Valori restituiti IMAPI

I metodi IMAPI restituiscono valori non negativi, in genere S \_ OK, se il metodo ha avuto esito positivo. I metodi IMAPI restituiscono codici di esito positivo o di errore da Winerror.h, Imapi2error.h o Imapi2fserror.h in caso di errore.

Vengono definiti i codici di esito positivo e di errore seguenti.




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt><dt>(HRESULT)0xC0AA0007L</dt></dl> | Il disco non ha superato la verifica della masterizzazione e può contenere dati danneggiati o essere inutilizzabile.<br /> | 
| <span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt><dt>(HRESULT)0xC0AA0002</dt></dl> | La richiesta è stata annullata.<br /> | 
| <span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt><dt>(HRESULT)0xC0AA0003</dt></dl> | La richiesta richiede la selezione di un registratore di dischi corrente.<br /> | 
| <span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0x00AA0302L</dt></dl> | Non è attualmente in corso alcuna operazione di scrittura.<br /> | 
| <span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt><dt>(HRESULT)0x00AA0004</dt></dl> | La velocità di scrittura richiesta non è supportata dall'unità e la velocità è stata regolata.<br /> | 
| <span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt><dt>(HRESULT)0x00AA0005</dt></dl> | Il tipo di rotazione richiesto non è supportato dall'unità e il tipo di rotazione è stato regolato.<br /> | 
| <span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt><dt>(HRESULT)0x00AA0006</dt></dl> | La velocità di scrittura richiesta e il tipo di rotazione non sono supportati dall'unità ed entrambi sono stati modificati.<br /> | 
| <span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt><dt>(HRESULT)0x00AA0200</dt></dl> | Il dispositivo ha accettato il comando, ma ha restituito dati di senso, che indicano un errore.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt><dt>(HRESULT)0x80AA0A00L</dt></dl> | L'immagine è diventata di sola lettura a causa di una chiamata a <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage.</strong></a> Di conseguenza, l'oggetto non può più essere modificato.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt><dt>(HRESULT)0x80AA0A01L</dt></dl> | Non è possibile aggiungere altre tracce. I supporti CD sono limitati a un intervallo di 1-99 tracce.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt><dt>(HRESULT)0x80AA0A03L</dt></dl> | È necessario aggiungere tracce all'immagine prima di usare questa funzione.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0x80AA0A02L</dt></dl> | Il tipo di settore richiesto non è supportato.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt><dt>(HRESULT)0x80AA0A04L</dt></dl> | Le tracce non possono essere aggiunte all'immagine prima dell'uso di questa funzione.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt><dt>(HRESULT)0x80AA0A05L</dt></dl> | L'aggiunta di questa traccia supererebbe le limitazioni dell'inizio del leadout.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt><dt>(HRESULT)0x80AA0A06L</dt></dl> | L'aggiunta di questa traccia supererebbe il limite di 99 indici.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt><dt>(HRESULT)0x80AA0A07L</dt></dl> | L'offset LBA specificato non è presente nell'elenco degli indici di traccia.<br /> | 
| <span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt><dt>(HRESULT)0x00AA0A08L</dt></dl> | L'offset LBA specificato è già presente nell'elenco degli indici di traccia.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt><dt>(HRESULT)0x80AA0A09L</dt></dl> | Impossibile cancellare l'indice 1 (offset LBA zero).<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt><dt>(HRESULT)0x80AA0A0AL</dt></dl> | Ogni indice deve avere una dimensione minima di dieci settori.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt><dt>(HRESULT)0xC0AA0201</dt></dl> | Il dispositivo ha segnalato che la pagina della modalità richiesta (e il tipo) non è presente.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt><dt>(HRESULT)0xC0AA0202</dt></dl> | Non sono presenti supporti nel dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt><dt>(HRESULT)0xC0AA0203</dt></dl> | Il supporto non è compatibile o di formato fisico sconosciuto.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt><dt>(HRESULT)0xC0AA0204</dt></dl> | Il supporto viene inserito capovolto.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt><dt>(HRESULT)0xC0AA0205</dt></dl> | L'unità ha segnalato che sta per essere pronta. Ripetere la richiesta in un secondo momento.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0206</dt></dl> | Il supporto è attualmente in fase di formattazione. Attendere il completamento del formato prima di provare a usare il supporto.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt><dt>(HRESULT)0xC0AA0207</dt></dl> | L'unità ha segnalato che sta eseguendo un'operazione di lunga durata, ad esempio il completamento di una scrittura. L'unità può essere inutilizzabile per un lungo periodo di tempo.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt><dt>(HRESULT)0xC0AA0208</dt></dl> | L'unità ha segnalato che la combinazione di parametri specificata nella pagina della modalità per un comando MODE SELECT non è supportata.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt><dt>(HRESULT)0xC0AA0209</dt></dl> | L'unità ha segnalato che il supporto è protetto da scrittura.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt><dt>(HRESULT)0xC0AA020A</dt></dl> | La pagina delle funzionalità richiesta non è supportata dal dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt><dt>(HRESULT)0xC0AA020B</dt></dl> | La pagina delle funzionalità richiesta è supportata, ma non è contrassegnata come corrente.<br /> | 
| <span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA020C</dt></dl> | L'unità non supporta il comando GET CONFIGURATION.<br /> | 
| <span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt><dt>(HRESULT)0xC0AA020D</dt></dl> | Il dispositivo non è riuscito ad accettare il comando entro il periodo di timeout. Questo problema può essere causato dal fatto che il dispositivo è in uno stato incoerente o potrebbe essere necessario aumentare il valore di timeout per il comando.<br /> | 
| <span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt><dt>(HRESULT)0xC0AA020E</dt></dl> | La struttura del DVD non è presente. Questo problema può essere causato dall'unità o dal supporto incompatibile utilizzato.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt><dt>(HRESULT)0xC0AA020F</dt></dl> | La velocità del supporto non è compatibile con il dispositivo. Questo problema può essere causato dall'uso di supporti con velocità superiore o inferiore rispetto all'intervallo di velocità supportato dal dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt><dt>(HRESULT)0xC0AA0210</dt></dl> | Il dispositivo associato a questo registratore durante l'ultima operazione è stato bloccato in modo esclusivo, causando l'esito negativo dell'operazione.<br /> | 
| <span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0211</dt></dl> | Il nome client non è valido.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA02FF</dt></dl> | Il dispositivo ha segnalato dati imprevisti o non validi per un comando.<br /> | 
| <span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt><dt>(HRESULT)0xC0AA0300</dt></dl> | La scrittura non è riuscita perché l'unità non ha ricevuto dati abbastanza rapidamente da continuare a scrivere. Lo spostamento dei dati di origine nel computer locale, la riduzione della velocità di scrittura o l'abilitazione di un'impostazione "buffer non in esecuzione" possono risolvere il problema.<br /> | 
| <span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA0301</dt></dl> | La scrittura non è riuscita perché l'unità ha restituito informazioni sull'errore da cui non è stato possibile eseguire il ripristino.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0400</dt></dl> | È attualmente in corso un'operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0401</dt></dl> | Non è attualmente in corso alcuna operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt><dt>(HRESULT)0xC0AA0402</dt></dl> | L'operazione richiesta è valida solo con supporti supportati.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0403</dt></dl> | Il flusso fornito da scrivere non è supportato.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt><dt>(HRESULT)0xC0AA0404</dt></dl> | Il flusso fornito da scrivere è troppo grande per il supporto attualmente inserito.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0405</dt></dl> | La sovrascrittura di supporti non vuoti non è consentita senza la proprietà ForceOverwrite impostata su VARIANT_TRUE.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0406</dt></dl> | Il tipo di supporto corrente non è supportato.<br /> | 
| <span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0407</dt></dl> | Questo dispositivo non supporta le operazioni richieste da questo formato di disco.<br /> | 
| <span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0408</dt></dl> | Il nome client non è valido.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0500</dt></dl> | È attualmente in corso un'operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0501</dt></dl> | Non è attualmente in corso alcuna operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0502</dt></dl> | L'operazione richiesta è valida solo quando il supporto è stato "preparato".<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0503</dt></dl> | L'operazione richiesta non è valida quando il supporto è stato "preparato" ma non rilasciato.<br /> | 
| <span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt><dt>(HRESULT)0xC0AA0504</dt></dl> | La proprietà non può essere modificata dopo che il supporto è stato scritto.<br /> | 
| <span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt><dt>(HRESULT)0xC0AA0505</dt></dl> | Il sommario non può essere recuperato da un disco vuoto.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0506</dt></dl> | Sono supportati solo supporti CD-R/RW vuoti.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0507</dt></dl> | Sono supportati solo supporti CD-R/RW vuoti.<br /> | 
| <span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt><dt>(HRESULT)0xC0AA0508</dt></dl> | I supporti CD-R e CD-RW supportano un massimo di 99 tracce audio.<br /> | 
| <span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT)0xC0AA0509</dt></dl> | Lo spazio disponibile sul supporto non è sufficiente per aggiungere la traccia audio specificata.<br /> | 
| <span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT)0xC0AA050A</dt></dl> | Non è possibile preparare il supporto fino a quando non si sceglie un registratore da usare.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt><dt>(HRESULT)0xC0AA050B</dt></dl> | L'ISRC specificato non è valido.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt><dt>(HRESULT)0xC0AA050C</dt></dl> | Il numero di Catalogo multimediale specificato non è valido.<br /> | 
| <span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA050D</dt></dl> | Il flusso audio specificato non è valido.<br /> | 
| <span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA050E</dt></dl> | Questo dispositivo non supporta le operazioni richieste da questo formato di disco.<br /> | 
| <span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA050F</dt></dl> | Il nome client non è valido.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0600</dt></dl> | È attualmente in corso un'operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0601</dt></dl> | Non è attualmente in corso alcuna operazione di scrittura.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0602</dt></dl> | L'operazione richiesta è valida solo quando il supporto è stato "preparato".<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0603</dt></dl> | L'operazione richiesta non è valida quando il supporto è stato "preparato" ma non rilasciato.<br /> | 
| <span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0604</dt></dl> | Il nome client non è valido.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0606</dt></dl> | Sono supportati solo supporti CD-R/RW vuoti.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0607</dt></dl> | Sono supportati solo supporti CD-R/RW vuoti.<br /> | 
| <span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT)0xC0AA0609</dt></dl> | Lo spazio sul supporto non è sufficiente per aggiungere la sessione specificata.<br /> | 
| <span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT)0xC0AA060A</dt></dl> | Non è possibile preparare il supporto fino a quando non si sceglie un registratore da usare.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA060D</dt></dl> | Il flusso audio specificato non è valido.<br /> | 
| <span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA060E</dt></dl> | Il tipo di blocco di dati richiesto non è supportato dal dispositivo corrente.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt><dt>(HRESULT)0xC0AA060F</dt></dl> | Il flusso non contiene un numero sufficiente di settori nel leadin per i supporti correnti.<br /> | 
| <span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0610</dt></dl> | Questo dispositivo non supporta le operazioni richieste da questo formato di disco.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt><dt>(HRESULT)0x80AA0900</dt></dl> | Il formato usa attualmente il registratore del disco per un'operazione di cancellazione. Attendere il completamento della cancellazione prima di provare a impostare o cancellare il registratore di dischi corrente.<br /> | 
| <span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt><dt>(HRESULT)0x80AA0901</dt></dl> | Il formato di cancellazione supporta solo un registratore. È necessario cancellare il registratore corrente prima di impostarne uno nuovo.<br /> | 
| <span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt><dt>(HRESULT)0x80AA0902</dt></dl> | L'unità non ha riportato dati sufficienti per un comando READ DISC INFORMATION. L'unità potrebbe non essere supportata o il supporto potrebbe non essere corretto.<br /> | 
| <span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt><dt>(HRESULT)0x80AA0903</dt></dl> | L'unità non ha riportato dati sufficienti per un comando MODE SENSE (page 0x2A). L'unità potrebbe non essere supportata o il supporto potrebbe non essere corretto.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt><dt>(HRESULT)0x80AA0904</dt></dl> | L'unità ha segnalato che il supporto non è cancellabile.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt><dt>(HRESULT)0x80AA0905</dt></dl> | L'unità non è riuscita con il comando di cancellazione.<br /> | 
| <span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt><dt>(HRESULT)0x80AA0906</dt></dl> | L'unità non ha completato la cancellazione in un'ora. L'unità può richiedere un ciclo di alimentazione, la rimozione dei supporti o un altro intervento manuale per riprendere il corretto funzionamento.<br /><blockquote>[!Note]<br />Attualmente, questo valore verrà restituito anche se un tentativo di eseguire una cancellazione su supporti CD-RW o DVD-RW tramite <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>l'interfaccia IDiscFormat2Erase</strong></a> ha esito negativo a causa di un supporto non valido.</blockquote><br /> | 
| <span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt><dt>(HRESULT)0x80AA0907</dt></dl> | L'unità ha restituito un errore imprevisto durante la cancellazione. Il supporto potrebbe non essere utilizzabile, la cancellazione potrebbe essere completa o l'unità potrebbe essere ancora in corso di cancellazione del disco.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt><dt>(HRESULT)0x80AA0908</dt></dl> | L'unità ha restituito un errore per un comando START UNIT (spinup). Potrebbe essere necessario un intervento manuale.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0909</dt></dl> | Il tipo di supporto corrente non è supportato.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA090A</dt></dl> | Questo dispositivo non supporta le operazioni richieste da questo formato di disco.<br /> | 
| <span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA090B</dt></dl> | Il nome client non è valido.<br /> | 




I codici di esito positivo e di errore seguenti sono definiti in Imapi2fserror.h.




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt><dt>(HRESULT)0xC0AAB100</dt></dl> | Errore interno: %1!ls!.<br /> | 
| <span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt><dt>(HRESULT)0xC0AAB101</dt></dl> | Valore specificato per il parametro '%1!ls!' non è valida.<br /> | 
| <span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl><dt><strong>IMAPI_E_READONLY</strong></dt><dt>(HRESULT)0xC0AAB102</dt></dl> | L'oggetto FileSystemImage è in modalità di sola lettura.<br /> | 
| <span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt><dt>(HRESULT)0xC0AAB103</dt></dl> | Nessun output file system specificato.<br /> | 
| <span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt><dt>(HRESULT)0xC0AAB104</dt></dl> | L'identificatore di volume specificato è troppo lungo o contiene uno o più caratteri non validi.<br /> | 
| <span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl><dt><strong>IMAPI_E_INVALID_DATE</strong></dt><dt>(HRESULT)0xC0AAB105</dt></dl> | Date di file non valide. %1!ls! l'ora è precedente a %2!ls! al tempo.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB106</dt></dl> | Il file system deve essere vuoto per questa funzione.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt><dt>(HRESULT)0xC0AAB163L</dt></dl> | Non è possibile modificare il file system specificato per la creazione, perché il file system della sessione importata e il file system nella sessione corrente non corrispondono.<br /> | 
| <span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl><dt><strong>IMAPI_E_NOT_FILE</strong></dt><dt>(HRESULT)0xC0AAB108</dt></dl> | Percorso specificato '%1!ls!' non identifica un file.<br /> | 
| <span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl><dt><strong>IMAPI_E_NOT_DIR</strong></dt><dt>(HRESULT)0xC0AAB109</dt></dl> | Percorso specificato '%1!ls!' non identifica una directory.<br /> | 
| <span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB10A</dt></dl> | La directory '%1!s!' non è vuoto.<br /> | 
| <span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt><dt>(HRESULT)0xC0AAB10B</dt></dl> | ls!' non fa parte del file system. Deve essere aggiunto per completare questa operazione.<br /> | 
| <span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl><dt><strong>IMAPI_E_INVALID_PATH</strong></dt><dt>(HRESULT)0xC0AAB110</dt></dl> | Percorso '%1!s!' formato non valido o contiene caratteri non validi.<br /> | 
| <span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt><dt>(HRESULT)0xC0AAB111</dt></dl> | Il nome '%1!ls!' specificato non è valido: il nome dell'oggetto file o directory creato mentre la proprietà UseRestrictedCharacterSet è impostata può contenere solo caratteri ANSI.<br /> | 
| <span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl><dt><strong>IMAPI_E_DUP_NAME</strong></dt><dt>(HRESULT)0xC0AAB112</dt></dl> | ls!' il nome esiste già.<br /> | 
| <span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt><dt>(HRESULT)0xC0AAB113</dt></dl> | Tentativo di aggiungere '%1!ls!' failed: impossibile creare un nome univoco specifico del file system per %2!ls! .<br /> | 
| <span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB118</dt></dl> | Impossibile trovare l'elemento '%1!ls!' nella gerarchia FileSystemImage.<br /> | 
| <span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB119</dt></dl> | Il file '%1!s!' non trovato nella gerarchia FileSystemImage.<br /> | 
| <span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB11A</dt></dl> | La directory '%1!s!' non trovato nella gerarchia FileSystemImage.<br /> | 
| <span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt><dt>(HRESULT)0xC0AAB120</dt></dl> | Aggiunta di '%1!ls!' l'immagine del risultato ha dimensioni maggiori del limite configurato corrente.<br /> | 
| <span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB121</dt></dl> | Il valore specificato per la proprietà FreeMediaBlocks è troppo piccolo per le dimensioni stimate dell'immagine in base ai dati correnti. <br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt><dt>(HRESULT)0xC0AAB200L</dt></dl> | L'immagine non è allineata su un limite di settore di 2 kb.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt><dt>(HRESULT)0xC0AAB201L)</dt></dl> | L'immagine non contiene un descrittore di volume valido.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt><dt>(HRESULT)0xC0AAB202L</dt></dl> | L'immagine non è stata impostata usando i metodi <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> o <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> prima di chiamare il metodo <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate.</strong></a><br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB203L</dt></dl> | L'immagine specificata è troppo grande per essere convalidata perché le dimensioni superano <strong>MAXLONG.</strong><br /> | 
| <span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt><dt>(HRESULT)0xC0AAB128</dt></dl> | Flusso di dati fornito per il file '%1!ls!' è incoerente: previsto %2! I64d! byte, trovati %3! I64d!. <br /> | 
| <span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB129</dt></dl> | Impossibile leggere i dati dal flusso fornito per il file '%1!ls!'.<br /> | 
| <span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12A</dt></dl> | Si è verificato l'errore seguente durante il tentativo di creare il flusso di dati per il file '%1!ls!': <br /> | 
| <span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12BL</dt></dl> | L'errore di enumerazione dei file nell'albero della directory non è accessibile a causa delle autorizzazioni.<br /> | 
| <span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt><dt>(HRESULT)0xC0AAB130</dt></dl> | Questa file system contiene troppe directory per %1!ls! .<br /> | 
| <span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt><dt>(HRESULT)0xC0AAB131</dt></dl> | ISO9660 è limitato a 8 livelli di directory.<br /> | 
| <span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB132</dt></dl> | Il file di dati è troppo grande per '%1!ls!' .<br /> | 
| <span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB138</dt></dl> | Impossibile inizializzare %1!ls! file stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB139</dt></dl> | Errore durante la ricerca in '%1!ls!' file stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB13A</dt></dl> | Errore durante la scrittura in '%1!ls!' file stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB13B</dt></dl> | Errore durante la lettura da '%1!ls!' file stash.<br /> | 
| <span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt><dt>(HRESULT)0xC0AAB140</dt></dl> | Directory di lavoro '%1!ls!' non è valida.<br /> | 
| <span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt><dt>(HRESULT)0xC0AAB141</dt></dl> | Impossibile impostare la directory di lavoro su '%1!ls!'. Lo spazio disponibile è %2! I64d! byte, circa %3! I64d! byte necessari. <br /> | 
| <span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt><dt>(HRESULT)0xC0AAB142</dt></dl> | Tentativo di spostare il file di dati stash nella directory '%1!ls!' non ha avuto esito positivo.<br /> | 
| <span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt><dt>(HRESULT)0xC0AAB148</dt></dl> | Impossibile aggiungere l'oggetto di avvio all'immagine.<br /> | 
| <span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt><dt>(HRESULT)0xC0AAB149</dt></dl> | Un oggetto di avvio può essere incluso solo in un'immagine disco iniziale.<br /> | 
| <span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt><dt>(HRESULT)0xC0AAB14A</dt></dl> | Il tipo di emulazione richiesto non corrisponde alle dimensioni dell'immagine d'avvio.<br /> | 
| <span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt><dt>(HRESULT)0xC0AAB150</dt></dl> | Il supporto ottico è vuoto.<br /> | 
| <span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt><dt>(HRESULT)0xC0AAB151</dt></dl> | Il disco specificato non contiene uno dei file system supportati.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB152</dt></dl> | Il disco specificato non contiene '%1!ls!' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt><dt>(HRESULT)0xC0AAB153</dt></dl> | Errore di coerenza durante l'importazione di '%1!ls!' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AAB154</dt></dl> | '%1!ls!' file system nel disco selezionato contiene una funzionalità non supportata per l'importazione: %2!ls!.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt><dt>(HRESULT)0xC0AAB155</dt></dl> | Impossibile importare %2!ls! file system dal disco. Il file '%1!ls!' esiste già all'interno della gerarchia delle immagini come directory.<br /> | 
| <span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB156</dt></dl> | Impossibile cercare il blocco %1! I64d! nel disco di origine. <br /> | 
| <span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB157</dt></dl> | L'importazione dalla sessione precedente non è riuscita a causa di un errore durante la lettura di un blocco nel supporto (molto probabilmente il blocco %1!u!).<br /> | 
| <span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt><dt>(HRESULT)0xC0AAB158</dt></dl> | Il disco corrente non è lo stesso da cui file system è stato importato.<br /> | 
| <span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt><dt>(HRESULT)0xC0AAB159</dt></dl> | IMAPI non consente più sessioni con il tipo di supporto corrente.<br /> | 
| <span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt><dt>(HRESULT)0xC0AAB15A</dt></dl> | IMAPI non può eseguire più sessioni con il supporto corrente perché non supporta una revisione della funzione definita dall'utente compatibile per la scrittura.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT)0xC0AAB15B</dt></dl> | IMAPI non supporta il tipo multisessione richiesto.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt><dt>(HRESULT)0xC0AAB133</dt></dl> | L'operazione non è riuscita a causa di un layout incompatibile della sessione precedente importata dal supporto.<br /> | 
| <span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT)0xC0AAB15C</dt></dl> | IMAPI non supporta nessuno dei tipi di multisessione forniti nel supporto corrente.<br /><blockquote>[!Note]<br />[<strong>Il metodo IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) restituisce questo errore se non sono presenti supporti nel dispositivo di registrazione.</blockquote><br /> | 
| <span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt><dt>(HRESULT)0xC0AAB15D</dt></dl> | La proprietà MultisessionInterfaces deve essere impostata prima di chiamare questo metodo.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt><dt>(HRESULT)0xC0AAB15E</dt></dl> | Impossibile importare %2!ls! file system dal disco. Directory '%1!ls!' esiste già all'interno della gerarchia di immagini come file.<br /> | 
| <span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt><dt>(HRESULT)0xC0AAB162</dt></dl> | Uno dei parametri multisessione non può essere recuperato o ha un valore errato.<br /> | 
| <span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0x00AAB15FL</dt></dl> | Questa funzionalità non è supportata per la revisione file system corrente. L'immagine verrà creata senza questa funzionalità.<br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                            |
| Intestazione<br/>                   | <dl> <dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt> </dl> |



 

 





