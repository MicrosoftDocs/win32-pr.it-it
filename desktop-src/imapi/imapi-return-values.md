---
title: Valori restituiti IMAPi (Imapi2error. h)
description: I metodi IMAPi restituiscono valori non negativi, in genere S \_ OK, se il metodo ha avuto esito positivo. In caso di errore, i metodi IMAP restituiscono codici di errore o di esito positivo da Winerror. h, Imapi2error. h o Imapi2fserror. h.
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
ms.openlocfilehash: c6bc4b99bb5ac123ea26ca1deb755fa29598811b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477159"
---
# <a name="imapi-return-values"></a><span data-ttu-id="b7491-104">Valori restituiti da IMAPi</span><span class="sxs-lookup"><span data-stu-id="b7491-104">IMAPI Return Values</span></span>

<span data-ttu-id="b7491-105">I metodi IMAPi restituiscono valori non negativi, in genere S \_ OK, se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b7491-105">The IMAPI methods return non-negative values, (typically S\_OK) if the method was successful.</span></span> <span data-ttu-id="b7491-106">In caso di errore, i metodi IMAP restituiscono codici di errore o di esito positivo da Winerror. h, Imapi2error. h o Imapi2fserror. h.</span><span class="sxs-lookup"><span data-stu-id="b7491-106">The IMAPI methods return success or error codes from Winerror.h, Imapi2error.h, or Imapi2fserror.h, on failure.</span></span>

<span data-ttu-id="b7491-107">Vengono definiti i codici di esito positivo e di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7491-107">The following success and error codes are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b7491-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b7491-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b7491-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7491-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <span data-ttu-id="b7491-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT) 0xC0AA0007L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT)0xC0AA0007L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-111">Il disco non ha superato la verifica dell'ustione e potrebbe contenere dati danneggiati o essere inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="b7491-111">The disc did not pass burn verification and may contain corrupt data or be unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <span data-ttu-id="b7491-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT) 0xC0AA0002</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT)0xC0AA0002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-113">La richiesta è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="b7491-113">The request was canceled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <span data-ttu-id="b7491-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT) 0xC0AA0003</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT)0xC0AA0003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-115">La richiesta richiede la selezione di una registrazione del disco corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-115">The request requires a current disc recorder to be selected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <span data-ttu-id="b7491-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0x00AA0302L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0x00AA0302L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-117">Non è attualmente in corso alcuna operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-117">No write operation is currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <span data-ttu-id="b7491-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0004</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-119">La velocità di scrittura richiesta non è supportata dall'unità e la velocità è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b7491-119">The requested write speed was not supported by the drive and the speed was adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <span data-ttu-id="b7491-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0005</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-121">Il tipo di rotazione richiesto non è supportato dall'unità e il tipo di rotazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b7491-121">The requested rotation type was not supported by the drive and the rotation type was adjusted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <span data-ttu-id="b7491-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0006</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0006</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-123">La velocità di scrittura e il tipo di rotazione richiesti non erano supportati dall'unità e sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="b7491-123">The requested write speed and rotation type were not supported by the drive and they were both adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <span data-ttu-id="b7491-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT) 0x00AA0200</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT)0x00AA0200</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-125">Il dispositivo ha accettato il comando, ma ha restituito dati di Sense, che indicano un errore.</span><span class="sxs-lookup"><span data-stu-id="b7491-125">The device accepted the command, but returned sense data, indicating an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <span data-ttu-id="b7491-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT) 0x80AA0A00L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT)0x80AA0A00L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-127">L'immagine è diventata di sola lettura a causa di una chiamata a <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator:: CreateResultImage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7491-127">The image has become read-only due to a call to <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>.</span></span> <span data-ttu-id="b7491-128">Di conseguenza, l'oggetto non può più essere modificato.</span><span class="sxs-lookup"><span data-stu-id="b7491-128">As a result the object can no longer be modified.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <span data-ttu-id="b7491-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A01L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A01L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-130">Non è possibile aggiungere altre tracce.</span><span class="sxs-lookup"><span data-stu-id="b7491-130">No more tracks may be added.</span></span> <span data-ttu-id="b7491-131">Il supporto CD è limitato a un intervallo di 1-99 tracce.</span><span class="sxs-lookup"><span data-stu-id="b7491-131">CD media is restricted to a range of 1-99 tracks.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <span data-ttu-id="b7491-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A03L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A03L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-133">Prima di utilizzare questa funzione, è necessario aggiungere tracce all'immagine.</span><span class="sxs-lookup"><span data-stu-id="b7491-133">Tracks must be added to the image before using this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <span data-ttu-id="b7491-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0A02L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0A02L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-135">Il tipo di settore richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7491-135">The requested sector type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <span data-ttu-id="b7491-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT) 0x80AA0A04L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT)0x80AA0A04L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-137">Non è possibile aggiungere tracce all'immagine prima di usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b7491-137">Tracks may not be added to the image prior to the use of this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <span data-ttu-id="b7491-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT) 0x80AA0A05L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT)0x80AA0A05L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-139">L'aggiunta di questa traccia supererà le limitazioni dell'inizio del lead out.</span><span class="sxs-lookup"><span data-stu-id="b7491-139">Adding this track would exceed the limitations of the start of the leadout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <span data-ttu-id="b7491-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT) 0x80AA0A06L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT)0x80AA0A06L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-141">L'aggiunta di questa traccia comporta il superamento del limite di 99 indice.</span><span class="sxs-lookup"><span data-stu-id="b7491-141">Adding this track would exceed the 99 index limit.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <span data-ttu-id="b7491-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT) 0x80AA0A07L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT)0x80AA0A07L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-143">L'offset LBA specificato non è presente nell'elenco degli indici di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b7491-143">The specified LBA offset is not in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <span data-ttu-id="b7491-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT) 0x00AA0A08L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT)0x00AA0A08L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-145">L'offset LBA specificato è già presente nell'elenco degli indici di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b7491-145">The specified LBA offset is already in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <span data-ttu-id="b7491-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT) 0x80AA0A09L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT)0x80AA0A09L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-147">Non è possibile cancellare l'indice 1 (valore di offset LBA zero).</span><span class="sxs-lookup"><span data-stu-id="b7491-147">Index 1 (LBA offset zero) cannot be cleared.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <span data-ttu-id="b7491-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT) 0x80AA0A0AL</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT)0x80AA0A0AL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-149">Ogni indice deve avere una dimensione minima di dieci settori.</span><span class="sxs-lookup"><span data-stu-id="b7491-149">Each index must have a minimum size of ten sectors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <span data-ttu-id="b7491-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT) 0xC0AA0201</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT)0xC0AA0201</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-151">Il dispositivo ha segnalato che la pagina della modalità richiesta (e il tipo) non è presente.</span><span class="sxs-lookup"><span data-stu-id="b7491-151">The device reported that the requested mode page (and type) is not present.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <span data-ttu-id="b7491-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0202</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0202</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-153">Nessun supporto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7491-153">There is no media in the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <span data-ttu-id="b7491-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AA0203</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AA0203</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-155">Il supporto non è compatibile o il formato fisico è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b7491-155">The media is not compatible or of unknown physical format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <span data-ttu-id="b7491-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT) 0xC0AA0204</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT)0xC0AA0204</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-157">Il supporto viene inserito verso il basso.</span><span class="sxs-lookup"><span data-stu-id="b7491-157">The media is inserted upside down.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <span data-ttu-id="b7491-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT) 0xC0AA0205</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT)0xC0AA0205</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-159">L'unità ha segnalato che è in corso la preparazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-159">The drive reported that it is in the process of becoming ready.</span></span> <span data-ttu-id="b7491-160">Ripetere la richiesta in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b7491-160">Please try the request again later.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <span data-ttu-id="b7491-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0206</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0206</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-162">Il file multimediale è attualmente in fase di formattazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-162">The media is currently being formatted.</span></span> <span data-ttu-id="b7491-163">Attendere il completamento del formato prima di provare a usare il supporto.</span><span class="sxs-lookup"><span data-stu-id="b7491-163">Please wait for the format to complete before attempting to use the media.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <span data-ttu-id="b7491-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT) 0xC0AA0207</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT)0xC0AA0207</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-165">L'unità ha segnalato che sta eseguendo un'operazione a esecuzione prolungata, ad esempio la fine di una scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-165">The drive reported that it is performing a long-running operation, such as finishing a write.</span></span> <span data-ttu-id="b7491-166">L'unità può essere inutilizzabile per un lungo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="b7491-166">The drive may be unusable for a long period of time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <span data-ttu-id="b7491-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT) 0xC0AA0208</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT)0xC0AA0208</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-168">L'unità ha segnalato che la combinazione di parametri forniti nella pagina modalità per un comando di selezione modalità non è supportata.</span><span class="sxs-lookup"><span data-stu-id="b7491-168">The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <span data-ttu-id="b7491-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT) 0xC0AA0209</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT)0xC0AA0209</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-170">L'unità ha segnalato che il supporto è protetto da scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-170">The drive reported that the media is write protected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <span data-ttu-id="b7491-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT) 0xC0AA020A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT)0xC0AA020A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-172">La pagina della funzionalità richiesta non è supportata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7491-172">The feature page requested is not supported by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <span data-ttu-id="b7491-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT) 0xC0AA020B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT)0xC0AA020B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-174">La pagina della funzionalità richiesta è supportata, ma non è contrassegnata come corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-174">The feature page requested is supported, but is not marked as current.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <span data-ttu-id="b7491-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA020C</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA020C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-176">L'unità non supporta il comando GET CONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="b7491-176">The drive does not support the GET CONFIGURATION command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <span data-ttu-id="b7491-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT) 0xC0AA020D</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT)0xC0AA020D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-178">Il dispositivo non è riuscito ad accettare il comando entro il periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="b7491-178">The device failed to accept the command within the timeout period.</span></span> <span data-ttu-id="b7491-179">Questo problema può essere dovuto al fatto che il dispositivo è in uno stato incoerente o è possibile che sia necessario aumentare il valore di timeout per il comando.</span><span class="sxs-lookup"><span data-stu-id="b7491-179">This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <span data-ttu-id="b7491-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT) 0xC0AA020E</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT)0xC0AA020E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-181">La struttura del DVD non è presente.</span><span class="sxs-lookup"><span data-stu-id="b7491-181">The DVD structure is not present.</span></span> <span data-ttu-id="b7491-182">Questo problema può essere causato da unità/supporto incompatibile.</span><span class="sxs-lookup"><span data-stu-id="b7491-182">This may be caused by incompatible drive/medium used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <span data-ttu-id="b7491-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AA020F</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AA020F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-184">La velocità del supporto non è compatibile con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7491-184">The media's speed is incompatible with the device.</span></span> <span data-ttu-id="b7491-185">Questo problema può essere causato dall'uso di supporti di velocità superiore o inferiore rispetto all'intervallo di velocità supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7491-185">This may be caused by using higher or lower speed media than the range of speeds supported by the device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <span data-ttu-id="b7491-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT) 0xC0AA0210</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT)0xC0AA0210</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-187">Il dispositivo associato a questo registratore durante l'ultima operazione è stato bloccato in modo esclusivo, causando l'esito negativo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-187">The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <span data-ttu-id="b7491-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0211</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0211</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-189">Il nome del client non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-189">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <span data-ttu-id="b7491-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA02FF</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA02FF</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-191">Il dispositivo ha segnalato dati imprevisti o non validi per un comando.</span><span class="sxs-lookup"><span data-stu-id="b7491-191">The device reported unexpected or invalid data for a command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <span data-ttu-id="b7491-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT) 0xC0AA0300</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT)0xC0AA0300</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-193">La scrittura non è riuscita perché l'unità non ha ricevuto i dati abbastanza rapidamente da continuare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-193">The write failed because the drive did not receive data quickly enough to continue writing.</span></span> <span data-ttu-id="b7491-194">Lo stato di trasferimento dei dati di origine nel computer locale, la riduzione della velocità di scrittura o l'abilitazione di un' &quot; impostazione senza buffer del buffer &quot; può risolvere questo problema.</span><span class="sxs-lookup"><span data-stu-id="b7491-194">Moving the source data to the local computer, reducing the write speed, or enabling a &quot;buffer underrun free&quot; setting may resolve this issue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <span data-ttu-id="b7491-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA0301</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA0301</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-196">La scrittura non è riuscita perché l'unità ha restituito le informazioni sull'errore che non è stato possibile recuperare.</span><span class="sxs-lookup"><span data-stu-id="b7491-196">The write failed because the drive returned error information that could not be recovered from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <span data-ttu-id="b7491-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0400</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0400</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-198">È attualmente in corso un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-198">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <span data-ttu-id="b7491-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0401</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0401</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-200">Non è attualmente in corso alcuna operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-200">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <span data-ttu-id="b7491-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT) 0xC0AA0402</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT)0xC0AA0402</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-202">L'operazione richiesta è valida solo con supporti supportati.</span><span class="sxs-lookup"><span data-stu-id="b7491-202">The requested operation is only valid with supported media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <span data-ttu-id="b7491-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0403</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0403</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-204">Il flusso specificato per la scrittura non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7491-204">The provided stream to write is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <span data-ttu-id="b7491-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0404</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0404</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-206">Il flusso specificato per la scrittura è troppo grande per il supporto attualmente inserito.</span><span class="sxs-lookup"><span data-stu-id="b7491-206">The provided stream to write is too large for the currently inserted media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <span data-ttu-id="b7491-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0405</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0405</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-208">La sovrascrittura di supporti non vuoti non è consentita se la proprietà ForceOverwrite è impostata su VARIANT_TRUE.</span><span class="sxs-lookup"><span data-stu-id="b7491-208">Overwriting non-blank media is not allowed without the ForceOverwrite property set to VARIANT_TRUE.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <span data-ttu-id="b7491-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0406</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0406</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-210">Il tipo di supporto corrente non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7491-210">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <span data-ttu-id="b7491-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0407</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0407</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-212">Questo dispositivo non supporta le operazioni richieste da questo formato di disco.</span><span class="sxs-lookup"><span data-stu-id="b7491-212">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <span data-ttu-id="b7491-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0408</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0408</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-214">Il nome del client non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-214">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <span data-ttu-id="b7491-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0500</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0500</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-216">È attualmente in corso un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-216">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <span data-ttu-id="b7491-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0501</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0501</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-218">Non è attualmente in corso alcuna operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-218">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <span data-ttu-id="b7491-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0502</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0502</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-220">L'operazione richiesta è valida solo quando è stato preparato un supporto &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="b7491-220">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <span data-ttu-id="b7491-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0503</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0503</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-222">L'operazione richiesta non è valida quando i supporti sono stati &quot; preparati &quot; ma non rilasciati.</span><span class="sxs-lookup"><span data-stu-id="b7491-222">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <span data-ttu-id="b7491-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT) 0xC0AA0504</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT)0xC0AA0504</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-224">Non è possibile modificare la proprietà dopo la scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="b7491-224">The property cannot be changed once the media has been written to.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <span data-ttu-id="b7491-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AA0505</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AA0505</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-226">Il sommario non può essere recuperato da un disco vuoto.</span><span class="sxs-lookup"><span data-stu-id="b7491-226">The table of contents cannot be retrieved from an empty disc.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <span data-ttu-id="b7491-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0506</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0506</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-228">Sono supportati solo supporti CD-R/RW vuoti.</span><span class="sxs-lookup"><span data-stu-id="b7491-228">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <span data-ttu-id="b7491-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0507</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0507</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-230">Sono supportati solo supporti CD-R/RW vuoti.</span><span class="sxs-lookup"><span data-stu-id="b7491-230">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <span data-ttu-id="b7491-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT) 0xC0AA0508</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT)0xC0AA0508</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-232">I supporti CD-R e CD-RW supportano un massimo di 99 tracce audio.</span><span class="sxs-lookup"><span data-stu-id="b7491-232">CD-R and CD-RW media support a maximum of 99 audio tracks.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <span data-ttu-id="b7491-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0509</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0509</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-234">Lo spazio rimanente sul supporto non è sufficiente per aggiungere la traccia audio specificata.</span><span class="sxs-lookup"><span data-stu-id="b7491-234">There is not enough space left on the media to add the provided audio track.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <span data-ttu-id="b7491-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA050A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA050A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-236">Non è possibile preparare i supporti fino a quando non si sceglie un registratore da usare.</span><span class="sxs-lookup"><span data-stu-id="b7491-236">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <span data-ttu-id="b7491-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT) 0xC0AA050B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT)0xC0AA050B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-238">Il ISRC specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-238">The ISRC provided is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <span data-ttu-id="b7491-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT) 0xC0AA050C</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT)0xC0AA050C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-240">Il numero di catalogo multimediale fornito non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-240">The Media Catalog Number provided is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <span data-ttu-id="b7491-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050D</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-242">Il flusso audio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-242">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <span data-ttu-id="b7491-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050E</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-244">Questo dispositivo non supporta le operazioni richieste da questo formato di disco.</span><span class="sxs-lookup"><span data-stu-id="b7491-244">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <span data-ttu-id="b7491-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA050F</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA050F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-246">Il nome del client non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-246">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <span data-ttu-id="b7491-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0600</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0600</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-248">È attualmente in corso un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-248">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <span data-ttu-id="b7491-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0601</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0601</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-250">Non è attualmente in corso alcuna operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-250">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <span data-ttu-id="b7491-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0602</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0602</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-252">L'operazione richiesta è valida solo quando è stato preparato un supporto &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="b7491-252">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <span data-ttu-id="b7491-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0603</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0603</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-254">L'operazione richiesta non è valida quando i supporti sono stati &quot; preparati &quot; ma non rilasciati.</span><span class="sxs-lookup"><span data-stu-id="b7491-254">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <span data-ttu-id="b7491-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0604</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0604</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-256">Il nome del client non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-256">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <span data-ttu-id="b7491-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0606</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0606</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-258">Sono supportati solo supporti CD-R/RW vuoti.</span><span class="sxs-lookup"><span data-stu-id="b7491-258">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <span data-ttu-id="b7491-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0607</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0607</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-260">Sono supportati solo supporti CD-R/RW vuoti.</span><span class="sxs-lookup"><span data-stu-id="b7491-260">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <span data-ttu-id="b7491-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0609</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0609</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-262">Lo spazio sul supporto non è sufficiente per aggiungere la sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="b7491-262">There is not enough space on the media to add the provided session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <span data-ttu-id="b7491-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA060A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA060A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-264">Non è possibile preparare i supporti fino a quando non si sceglie un registratore da usare.</span><span class="sxs-lookup"><span data-stu-id="b7491-264">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <span data-ttu-id="b7491-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060D</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-266">Il flusso audio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-266">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <span data-ttu-id="b7491-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060E</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-268">Il tipo di blocco di dati richiesto non è supportato dal dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-268">The requested data block type is not supported by the current device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <span data-ttu-id="b7491-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT) 0xC0AA060F</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT)0xC0AA060F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-270">Il flusso non contiene un numero sufficiente di settori nel leadin per il supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-270">The stream does not contain a sufficient number of sectors in the leadin for the current media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <span data-ttu-id="b7491-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0610</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0610</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-272">Questo dispositivo non supporta le operazioni richieste da questo formato di disco.</span><span class="sxs-lookup"><span data-stu-id="b7491-272">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <span data-ttu-id="b7491-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT) 0x80AA0900</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT)0x80AA0900</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-274">Il formato usa attualmente la registrazione del disco per un'operazione di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-274">The format is currently using the disc recorder for an erase operation.</span></span> <span data-ttu-id="b7491-275">Attendere il completamento della cancellazione prima di provare a impostare o cancellare la registrazione del disco corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-275">Please wait for the erase to complete before attempting to set or clear the current disc recorder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <span data-ttu-id="b7491-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0901</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0901</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-277">Il formato di cancellazione supporta solo un registratore.</span><span class="sxs-lookup"><span data-stu-id="b7491-277">The erase format only supports one recorder.</span></span> <span data-ttu-id="b7491-278">È necessario cancellare il registratore corrente prima di impostarne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="b7491-278">You must clear the current recorder before setting a new one.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <span data-ttu-id="b7491-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0902</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0902</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-280">L'unità non ha segnalato dati sufficienti per un comando READ disk INFORMATION.</span><span class="sxs-lookup"><span data-stu-id="b7491-280">The drive did not report sufficient data for a READ DISC INFORMATION command.</span></span> <span data-ttu-id="b7491-281">L'unità potrebbe non essere supportata o il supporto potrebbe non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="b7491-281">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <span data-ttu-id="b7491-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0903</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0903</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-283">L'unità non ha segnalato dati sufficienti per un comando MODE (page 0x2A).</span><span class="sxs-lookup"><span data-stu-id="b7491-283">The drive did not report sufficient data for a MODE SENSE (page 0x2A) command.</span></span> <span data-ttu-id="b7491-284">L'unità potrebbe non essere supportata o il supporto potrebbe non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="b7491-284">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <span data-ttu-id="b7491-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT) 0x80AA0904</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT)0x80AA0904</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-286">L'unità ha segnalato che i supporti non sono cancellabili.</span><span class="sxs-lookup"><span data-stu-id="b7491-286">The drive reported that the media is not erasable.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <span data-ttu-id="b7491-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0905</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0905</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-288">L'unità non ha superato il comando di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-288">The drive failed the erase command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <span data-ttu-id="b7491-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT) 0x80AA0906</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT)0x80AA0906</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-290">L'unità non ha completato la cancellazione in un'ora.</span><span class="sxs-lookup"><span data-stu-id="b7491-290">The drive did not complete the erase in one hour.</span></span> <span data-ttu-id="b7491-291">Per riprendere il funzionamento corretto, è possibile che l'unità richieda un ciclo di alimentazione, una rimozione dei supporti o un altro intervento manuale.</span><span class="sxs-lookup"><span data-stu-id="b7491-291">The drive may require a power cycle, media removal, or other manual intervention to resume proper operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b7491-292">Attualmente, questo valore verrà restituito anche se un tentativo di eseguire una cancellazione su un supporto CD-RW o DVD-RW tramite l'interfaccia <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> ha esito negativo a causa di un problema di supporto.</span><span class="sxs-lookup"><span data-stu-id="b7491-292">Currently, this value will also be returned if an attempt to perform an erase on CD-RW or DVD-RW media via the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> interface fails as a result of the media being bad.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <span data-ttu-id="b7491-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT) 0x80AA0907</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT)0x80AA0907</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-294">L'unità ha restituito un errore imprevisto durante la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-294">The drive returned an unexpected error during the erase.</span></span> <span data-ttu-id="b7491-295">È possibile che il supporto sia inutilizzabile, che la cancellazione venga completata o che l'unità sia ancora in corso di cancellazione del disco.</span><span class="sxs-lookup"><span data-stu-id="b7491-295">The media may be unusable, the erase may be complete, or the drive may still be in the process of erasing the disc.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <span data-ttu-id="b7491-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0908</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0908</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-297">L'unità ha restituito un errore per un comando di unità di avvio (SpinUp).</span><span class="sxs-lookup"><span data-stu-id="b7491-297">The drive returned an error for a START UNIT (spinup) command.</span></span> <span data-ttu-id="b7491-298">Potrebbe essere necessario un intervento manuale.</span><span class="sxs-lookup"><span data-stu-id="b7491-298">Manual intervention may be required.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <span data-ttu-id="b7491-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0909</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0909</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-300">Il tipo di supporto corrente non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7491-300">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <span data-ttu-id="b7491-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA090A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA090A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-302">Questo dispositivo non supporta le operazioni richieste da questo formato di disco.</span><span class="sxs-lookup"><span data-stu-id="b7491-302">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <span data-ttu-id="b7491-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA090B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA090B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-304">Il nome del client non è valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-304">The client name is not valid.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b7491-305">I codici di errore e di riuscita seguenti sono definiti in Imapi2fserror. h.</span><span class="sxs-lookup"><span data-stu-id="b7491-305">The following success and error codes are defined in Imapi2fserror.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b7491-306">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b7491-306">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b7491-307">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7491-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <span data-ttu-id="b7491-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB100</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-309">Si è verificato un errore interno: %1! ls!.</span><span class="sxs-lookup"><span data-stu-id="b7491-309">Internal error occurred: %1!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <span data-ttu-id="b7491-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT) 0xC0AAB101</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT)0xC0AAB101</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-311">Il valore specificato per il parametro ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-311">The value specified for parameter '%1!ls!'</span></span> <span data-ttu-id="b7491-312">non è valida.</span><span class="sxs-lookup"><span data-stu-id="b7491-312">is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <span data-ttu-id="b7491-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT) 0xC0AAB102</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT)0xC0AAB102</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-314">L'oggetto FileSystemImage è in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b7491-314">FileSystemImage object is in read only mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <span data-ttu-id="b7491-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT) 0xC0AAB103</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT)0xC0AAB103</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-316">Non file system specificato alcun output.</span><span class="sxs-lookup"><span data-stu-id="b7491-316">No output file system specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <span data-ttu-id="b7491-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB104</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT)0xC0AAB104</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-318">L'identificatore di volume specificato è troppo lungo o contiene uno o più caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="b7491-318">The specified Volume Identifier is either too long or contains one or more invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <span data-ttu-id="b7491-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT) 0xC0AAB105</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT)0xC0AAB105</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-320">Date file non valide.</span><span class="sxs-lookup"><span data-stu-id="b7491-320">Invalid file dates.</span></span> <span data-ttu-id="b7491-321">%1! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-321">%1!ls!</span></span> <span data-ttu-id="b7491-322">l'ora è precedente a %2! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-322">time is earlier than %2!ls!</span></span> <span data-ttu-id="b7491-323">al tempo.</span><span class="sxs-lookup"><span data-stu-id="b7491-323">time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <span data-ttu-id="b7491-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB106</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB106</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-325">Il file system deve essere vuoto per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b7491-325">The file system must be empty for this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <span data-ttu-id="b7491-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB163L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB163L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-327">Non è possibile modificare il file system specificato per la creazione perché i file system della sessione importata e il file system della sessione corrente non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="b7491-327">You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <span data-ttu-id="b7491-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB108</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT)0xC0AAB108</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-329">Percorso specificato ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-329">Specified path '%1!ls!'</span></span> <span data-ttu-id="b7491-330">non identifica un file.</span><span class="sxs-lookup"><span data-stu-id="b7491-330">does not identify a file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <span data-ttu-id="b7491-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT) 0xC0AAB109</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT)0xC0AAB109</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-332">Percorso specificato ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-332">Specified path '%1!ls!'</span></span> <span data-ttu-id="b7491-333">non identifica una directory.</span><span class="sxs-lookup"><span data-stu-id="b7491-333">does not identify a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <span data-ttu-id="b7491-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB10A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB10A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-335">La directory ' %1! s!'</span><span class="sxs-lookup"><span data-stu-id="b7491-335">The directory '%1!s!'</span></span> <span data-ttu-id="b7491-336">non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="b7491-336">is not empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <span data-ttu-id="b7491-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB10B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB10B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-338">ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-338">ls!'</span></span> <span data-ttu-id="b7491-339">non fa parte del file system.</span><span class="sxs-lookup"><span data-stu-id="b7491-339">is not part of the file system.</span></span> <span data-ttu-id="b7491-340">Per completare questa operazione, è necessario aggiungerlo.</span><span class="sxs-lookup"><span data-stu-id="b7491-340">It must be added to complete this operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <span data-ttu-id="b7491-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT) 0xC0AAB110</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT)0xC0AAB110</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-342">Percorso ' %1! s!'</span><span class="sxs-lookup"><span data-stu-id="b7491-342">Path '%1!s!'</span></span> <span data-ttu-id="b7491-343">non è formattato correttamente o contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="b7491-343">is badly formed or contains invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <span data-ttu-id="b7491-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT) 0xC0AAB111</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT)0xC0AAB111</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-345">Il nome ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-345">The name '%1!ls!'</span></span> <span data-ttu-id="b7491-346">il parametro specificato non è valido: il nome dell'oggetto file o directory creato mentre la proprietà UseRestrictedCharacterSet è impostata può contenere solo caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="b7491-346">specified is not legal: Name of file or directory object created while the UseRestrictedCharacterSet property is set may only contain ANSI characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <span data-ttu-id="b7491-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB112</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT)0xC0AAB112</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-348">ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-348">ls!'</span></span> <span data-ttu-id="b7491-349">il nome esiste già.</span><span class="sxs-lookup"><span data-stu-id="b7491-349">name already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <span data-ttu-id="b7491-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB113</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT)0xC0AAB113</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-351">Tentativo di aggiunta di ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-351">Attempt to add '%1!ls!'</span></span> <span data-ttu-id="b7491-352">non riuscito: non è possibile creare un nome univoco specifico per il file System per %2! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-352">failed: cannot create a file-system-specific unique name for the %2!ls!</span></span> <span data-ttu-id="b7491-353">.</span><span class="sxs-lookup"><span data-stu-id="b7491-353">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <span data-ttu-id="b7491-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB118</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB118</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-355">Impossibile trovare l'elemento ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-355">Cannot find item '%1!ls!'</span></span> <span data-ttu-id="b7491-356">nella gerarchia di FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="b7491-356">in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <span data-ttu-id="b7491-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB119</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB119</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-358">Il file ' %1! s!'</span><span class="sxs-lookup"><span data-stu-id="b7491-358">The file '%1!s!'</span></span> <span data-ttu-id="b7491-359">non è stato trovato nella gerarchia FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="b7491-359">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <span data-ttu-id="b7491-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB11A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB11A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-361">La directory ' %1! s!'</span><span class="sxs-lookup"><span data-stu-id="b7491-361">The directory '%1!s!'</span></span> <span data-ttu-id="b7491-362">non è stato trovato nella gerarchia FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="b7491-362">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <span data-ttu-id="b7491-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT) 0xC0AAB120</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT)0xC0AAB120</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-364">Aggiunta di ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-364">Adding '%1!ls!'</span></span> <span data-ttu-id="b7491-365">comporterebbe un'immagine di risultato con dimensioni maggiori del limite configurato corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-365">would result in a result image having a size larger than the current configured limit.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <span data-ttu-id="b7491-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB121</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB121</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-367">Il valore specificato per la proprietà FreeMediaBlocks è troppo piccolo per le dimensioni stimate dell'immagine in base ai dati correnti.</span><span class="sxs-lookup"><span data-stu-id="b7491-367">Value specified for FreeMediaBlocks property is too small for estimated image size based on current data.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <span data-ttu-id="b7491-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT) 0xC0AAB200L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT)0xC0AAB200L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-369">L'immagine non è allineata a un limite di settore 2 KB.</span><span class="sxs-lookup"><span data-stu-id="b7491-369">The image is not aligned on a 2kb sector boundary.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <span data-ttu-id="b7491-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB201L)</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB201L)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-371">L'immagine non contiene un descrittore di volume valido.</span><span class="sxs-lookup"><span data-stu-id="b7491-371">The image does not contain a valid volume descriptor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <span data-ttu-id="b7491-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT) 0xC0AAB202L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT)0xC0AAB202L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-373">L'immagine non è stata impostata con i metodi <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager:: SEPATH</strong></a> o <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::</strong></a> SetValue prima di chiamare il metodo <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager:: Validate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b7491-373">The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> methods prior to calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <span data-ttu-id="b7491-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB203L</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB203L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-375">L'immagine fornita è troppo grande per essere convalidata perché le dimensioni superano <strong>MAXLONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7491-375">The provided image is too large to be validated as the size exceeds <strong>MAXLONG</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <span data-ttu-id="b7491-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT) 0xC0AAB128</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT)0xC0AAB128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-377">Flusso di dati specificato per il file ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-377">Data stream supplied for file '%1!ls!'</span></span> <span data-ttu-id="b7491-378">è incoerente: previsto %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="b7491-378">is inconsistent: expected %2!I64d!</span></span> <span data-ttu-id="b7491-379">byte, trovati %3! I64d!.</span><span class="sxs-lookup"><span data-stu-id="b7491-379">bytes, found %3!I64d!.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <span data-ttu-id="b7491-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB129</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB129</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-381">Impossibile leggere i dati dal flusso fornito per il file ' %1! ls!'.</span><span class="sxs-lookup"><span data-stu-id="b7491-381">Cannot read data from stream supplied for file '%1!ls!'.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <span data-ttu-id="b7491-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-383">Si è verificato il seguente errore durante il tentativo di creare il flusso di dati per il file ' %1! ls!':</span><span class="sxs-lookup"><span data-stu-id="b7491-383">The following error was encountered when trying to create data stream for file '%1!ls!':</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <span data-ttu-id="b7491-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12BL</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12BL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-385">Errore durante l'enumerazione dei file nell'albero di directory è inaccessibile a causa delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="b7491-385">Failure enumerating files in the directory tree is inaccessible due to permissions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <span data-ttu-id="b7491-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT) 0xC0AAB130</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT)0xC0AAB130</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-387">Questa immagine di file system contiene troppe directory per %1! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-387">This file system image has too many directories for the %1!ls!</span></span> <span data-ttu-id="b7491-388">.</span><span class="sxs-lookup"><span data-stu-id="b7491-388">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <span data-ttu-id="b7491-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT) 0xC0AAB131</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT)0xC0AAB131</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-390">ISO9660 è limitato a 8 livelli di directory.</span><span class="sxs-lookup"><span data-stu-id="b7491-390">ISO9660 is limited to 8 levels of directories.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <span data-ttu-id="b7491-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB132</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB132</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-392">Il file di dati è troppo grande per ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-392">Data file is too large for '%1!ls!'</span></span> <span data-ttu-id="b7491-393">.</span><span class="sxs-lookup"><span data-stu-id="b7491-393">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <span data-ttu-id="b7491-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB138</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB138</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-395">Impossibile inizializzare %1! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-395">Cannot initialize %1!ls!</span></span> <span data-ttu-id="b7491-396">file stash.</span><span class="sxs-lookup"><span data-stu-id="b7491-396">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <span data-ttu-id="b7491-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB139</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB139</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-398">Errore durante la ricerca in ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-398">Error seeking in '%1!ls!'</span></span> <span data-ttu-id="b7491-399">file stash.</span><span class="sxs-lookup"><span data-stu-id="b7491-399">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <span data-ttu-id="b7491-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-401">Si è verificato un errore durante la scrittura in ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-401">Error encountered writing to '%1!ls!'</span></span> <span data-ttu-id="b7491-402">file stash.</span><span class="sxs-lookup"><span data-stu-id="b7491-402">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <span data-ttu-id="b7491-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-404">Si è verificato un errore durante la lettura da' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-404">Error encountered reading from '%1!ls!'</span></span> <span data-ttu-id="b7491-405">file stash.</span><span class="sxs-lookup"><span data-stu-id="b7491-405">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <span data-ttu-id="b7491-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB140</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB140</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-407">La directory di lavoro ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-407">The working directory '%1!ls!'</span></span> <span data-ttu-id="b7491-408">non è valida.</span><span class="sxs-lookup"><span data-stu-id="b7491-408">is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <span data-ttu-id="b7491-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT) 0xC0AAB141</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT)0xC0AAB141</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-410">Impossibile impostare la directory di lavoro su' %1! ls!'.</span><span class="sxs-lookup"><span data-stu-id="b7491-410">Cannot set working directory to '%1!ls!'.</span></span> <span data-ttu-id="b7491-411">Lo spazio disponibile è %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="b7491-411">Space available is %2!I64d!</span></span> <span data-ttu-id="b7491-412">byte, approssimativamente %3! I64d!</span><span class="sxs-lookup"><span data-stu-id="b7491-412">bytes, approximately %3!I64d!</span></span> <span data-ttu-id="b7491-413">byte richiesti.</span><span class="sxs-lookup"><span data-stu-id="b7491-413">bytes required.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <span data-ttu-id="b7491-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT) 0xC0AAB142</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT)0xC0AAB142</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-415">Tentativo di spostare il file di Stash dei dati nella directory ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-415">Attempt to move the data stash file to directory '%1!ls!'</span></span> <span data-ttu-id="b7491-416">il tentativo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b7491-416">was not successful.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <span data-ttu-id="b7491-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT) 0xC0AAB148</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT)0xC0AAB148</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-418">Non è stato possibile aggiungere l'oggetto di avvio all'immagine.</span><span class="sxs-lookup"><span data-stu-id="b7491-418">The boot object could not be added to the image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <span data-ttu-id="b7491-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT) 0xC0AAB149</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT)0xC0AAB149</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-420">Un oggetto di avvio può essere incluso solo in un'immagine del disco iniziale.</span><span class="sxs-lookup"><span data-stu-id="b7491-420">A boot object can only be included in an initial disc image.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <span data-ttu-id="b7491-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB14A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB14A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-422">Il tipo di emulazione richiesto non corrisponde alla dimensione dell'immagine d'avvio.</span><span class="sxs-lookup"><span data-stu-id="b7491-422">The emulation type requested does not match the boot image size.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <span data-ttu-id="b7491-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AAB150</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AAB150</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-424">Il supporto ottico è vuoto.</span><span class="sxs-lookup"><span data-stu-id="b7491-424">Optical media is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <span data-ttu-id="b7491-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB151</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB151</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-426">Il disco specificato non contiene uno dei file system supportati.</span><span class="sxs-lookup"><span data-stu-id="b7491-426">The specified disc does not contain one of the supported file systems.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <span data-ttu-id="b7491-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB152</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB152</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-428">Il disco specificato non contiene un'%1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-428">The specified disc does not contain a '%1!ls!'</span></span> <span data-ttu-id="b7491-429">.</span><span class="sxs-lookup"><span data-stu-id="b7491-429">file system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <span data-ttu-id="b7491-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB153</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB153</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-431">Si è verificato un errore di coerenza durante l'importazione di ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-431">Consistency error encountered while importing the '%1!ls!'</span></span> <span data-ttu-id="b7491-432">.</span><span class="sxs-lookup"><span data-stu-id="b7491-432">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <span data-ttu-id="b7491-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AAB154</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AAB154</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-434">' %1! ls!' file system nel disco selezionato contiene una funzionalità non supportata per l'importazione: %2! ls!.</span><span class="sxs-lookup"><span data-stu-id="b7491-434">The '%1!ls!'file system on the selected disc contains a feature not supported for import: %2!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <span data-ttu-id="b7491-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB155</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB155</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-436">Impossibile importare %2! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-436">Could not import %2!ls!</span></span> <span data-ttu-id="b7491-437">file system dal disco. Il file ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-437">file system from disc. The file '%1!ls!'</span></span> <span data-ttu-id="b7491-438">esiste già nella gerarchia di immagini come una directory.</span><span class="sxs-lookup"><span data-stu-id="b7491-438">already exists within the image hierarchy as a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <span data-ttu-id="b7491-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB156</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB156</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-440">Impossibile eseguire la ricerca del blocco %1! I64d!</span><span class="sxs-lookup"><span data-stu-id="b7491-440">Cannot seek to block %1!I64d!</span></span> <span data-ttu-id="b7491-441">sul disco di origine.</span><span class="sxs-lookup"><span data-stu-id="b7491-441">on source disc.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <span data-ttu-id="b7491-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB157</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB157</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-443">Importazione dalla sessione precedente non riuscita a causa di un errore durante la lettura di un blocco sul supporto (più probabile blocco %1! u!).</span><span class="sxs-lookup"><span data-stu-id="b7491-443">Import from previous session failed due to an error reading a block on the media (most likely block %1!u!).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <span data-ttu-id="b7491-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB158</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB158</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-445">Il disco corrente non è uguale a quello da cui è stato importato file system.</span><span class="sxs-lookup"><span data-stu-id="b7491-445">Current disc is not the same one from which file system was imported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <span data-ttu-id="b7491-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB159</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB159</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-447">IMAPi non consente l'uso di più sessioni con il tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-447">IMAPI does not allow multi-session with the current media type.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <span data-ttu-id="b7491-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AAB15A</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AAB15A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-449">IMAPi non è in grado di eseguire più sessioni con il supporto corrente perché non supporta una revisione UDF compatibile per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="b7491-449">IMAPI cannot do multi-session with the current media because it does not support a compatible UDF revision for write.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <span data-ttu-id="b7491-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15B</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-451">IMAPi non supporta il tipo multisessione richiesto.</span><span class="sxs-lookup"><span data-stu-id="b7491-451">IMAPI does not support the multisession type requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <span data-ttu-id="b7491-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT) 0xC0AAB133</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT)0xC0AAB133</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-453">Operazione non riuscita a causa di un layout incompatibile della sessione precedente importata dal supporto.</span><span class="sxs-lookup"><span data-stu-id="b7491-453">Operation failed due to an incompatible layout of the previous session imported from the medium.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <span data-ttu-id="b7491-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15C</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-455">IMAPi supporta nessuno dei tipi multisessione disponibili sul supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-455">IMAPI supports none of the multisession type(s) provided on the current media.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b7491-456">[<strong>IFileSystemImage:: ImportFileSystem</strong>] (/Windows/Desktop/API/imapi2fs/NF-imapi2fs-ifilesystemimage-importfilesystem) il metodo restituisce questo errore se non è presente alcun supporto nel dispositivo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b7491-456">[<strong>IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method returns this error if there is no media in the recording device.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <span data-ttu-id="b7491-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT) 0xC0AAB15D</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT)0xC0AAB15D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-458">Prima di chiamare questo metodo è necessario impostare la proprietà MultisessionInterfaces.</span><span class="sxs-lookup"><span data-stu-id="b7491-458">MultisessionInterfaces property must be set prior calling this method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <span data-ttu-id="b7491-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB15E</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT)0xC0AAB15E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-460">Impossibile importare %2! ls!</span><span class="sxs-lookup"><span data-stu-id="b7491-460">Could not import %2!ls!</span></span> <span data-ttu-id="b7491-461">file system dal disco. La directory ' %1! ls!'</span><span class="sxs-lookup"><span data-stu-id="b7491-461">file system from disc. The directory '%1!ls!'</span></span> <span data-ttu-id="b7491-462">esiste già nella gerarchia di immagini come file.</span><span class="sxs-lookup"><span data-stu-id="b7491-462">already exists within the image hierarchy as a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <span data-ttu-id="b7491-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT) 0xC0AAB162</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT)0xC0AAB162</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-464">Non è possibile recuperare uno dei parametri multisessione o il valore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="b7491-464">One of multisession parameters cannot be retrieved or has a wrong value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <span data-ttu-id="b7491-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x00AAB15FL</dt> </span><span class="sxs-lookup"><span data-stu-id="b7491-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x00AAB15FL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b7491-466">Questa funzionalità non è supportata per la revisione del file system corrente.</span><span class="sxs-lookup"><span data-stu-id="b7491-466">This feature is not supported for the current file system revision.</span></span> <span data-ttu-id="b7491-467">L'immagine verrà creata senza questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b7491-467">The image will be created without this feature.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b7491-468">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7491-468">Requirements</span></span>



| <span data-ttu-id="b7491-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7491-469">Requirement</span></span> | <span data-ttu-id="b7491-470">Valore</span><span class="sxs-lookup"><span data-stu-id="b7491-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7491-471">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7491-471">Minimum supported client</span></span><br/> | <span data-ttu-id="b7491-472">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b7491-472">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="b7491-473">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7491-473">Minimum supported server</span></span><br/> | <span data-ttu-id="b7491-474">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7491-474">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                            |
| <span data-ttu-id="b7491-475">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7491-475">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7491-476"><dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7491-476"><dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt></span></span> </dl> |



 

 





