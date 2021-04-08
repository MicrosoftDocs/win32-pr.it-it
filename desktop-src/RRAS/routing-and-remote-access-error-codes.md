---
title: Codici di errore di routing e accesso remoto
description: I codici di errore API RRAS (routing e accesso remoto) seguenti sono definiti in raserror. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048045"
---
# <a name="routing-and-remote-access-error-codes"></a><span data-ttu-id="89aa1-103">Codici di errore di routing e accesso remoto</span><span class="sxs-lookup"><span data-stu-id="89aa1-103">Routing and Remote Access Error Codes</span></span>

<span data-ttu-id="89aa1-104">I codici di errore API RRAS (routing e accesso remoto) seguenti sono definiti in raserror. h.</span><span class="sxs-lookup"><span data-stu-id="89aa1-104">The following Routing and Remote Access (RRAS) API error codes are defined in raserror.h.</span></span> <span data-ttu-id="89aa1-105">Tutti i codici di errore sono supportati in Windows 2000 o versioni successive di Windows, a meno che non sia specificato diversamente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-105">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89aa1-106">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="89aa1-106">Return code/value</span></span></th>
<th><span data-ttu-id="89aa1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89aa1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <span data-ttu-id="89aa1-108"><dt><strong>In sospeso</strong></dt> <dt>600</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-108"><dt><strong>PENDING</strong></dt> <dt>600</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-109">Un'operazione è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-109">An operation is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <span data-ttu-id="89aa1-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-111">L'handle di porta specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-111">The port handle supplied is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <span data-ttu-id="89aa1-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-113">La porta specificata è già aperta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-113">The specified port is already open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <span data-ttu-id="89aa1-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-115">Il buffer fornito è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-115">The buffer supplied is too small.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <span data-ttu-id="89aa1-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-117">Le informazioni sulla porta specificate non sono corrette.</span><span class="sxs-lookup"><span data-stu-id="89aa1-117">The port information specified is incorrect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <span data-ttu-id="89aa1-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-119">Impossibile impostare le informazioni sulla porta specificate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-119">The port information specified cannot be set.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-120">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-120">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <span data-ttu-id="89aa1-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-122">La porta specificata non è connessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-122">The port specified is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <span data-ttu-id="89aa1-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-124">Rilevato un evento non valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-124">An event that is not valid was detected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-125">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-125">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <span data-ttu-id="89aa1-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-127">Il dispositivo specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="89aa1-127">The specified device does not exist.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <span data-ttu-id="89aa1-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-129">Il tipo di dispositivo specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="89aa1-129">The specified device type does not exist.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <span data-ttu-id="89aa1-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-131">Il buffer specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-131">The buffer supplied is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <span data-ttu-id="89aa1-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-133">È stata specificata una route non disponibile.</span><span class="sxs-lookup"><span data-stu-id="89aa1-133">A route was specified that is not available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-134">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-134">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <span data-ttu-id="89aa1-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-136">La route specificata non è allocata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-136">The specified route is not allocated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <span data-ttu-id="89aa1-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-138">La compressione specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-138">The specified compression is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-139">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-139">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <span data-ttu-id="89aa1-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-141">Buffer insufficienti disponibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-141">There were insufficient buffers available.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <span data-ttu-id="89aa1-142"><dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-142"><dt><strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-143">La porta specificata non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-143">The specified port was not found.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <span data-ttu-id="89aa1-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-145">Richiesta asincrona in sospeso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-145">An asynchronous request is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <span data-ttu-id="89aa1-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-147">La porta o il dispositivo specificato è già in stato di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-147">The specified port or device is already disconnecting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <span data-ttu-id="89aa1-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-149">La porta specificata non è aperta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-149">The specified port is not open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <span data-ttu-id="89aa1-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-151">La porta specificata è disconnessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-151">The specified port is disconnected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <span data-ttu-id="89aa1-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-153">Non è stato possibile determinare alcun endpoint.</span><span class="sxs-lookup"><span data-stu-id="89aa1-153">No endpoints could be determined.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-154">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-154">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <span data-ttu-id="89aa1-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-156">Impossibile aprire il file della rubrica specificata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-156">Cannot open the specified phone book file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <span data-ttu-id="89aa1-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-158">Impossibile caricare il file della rubrica telefonica specificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-158">Cannot load the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <span data-ttu-id="89aa1-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-160">Impossibile trovare la voce della rubrica telefonica specificata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-160">Cannot find the specified phone book entry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <span data-ttu-id="89aa1-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-162">Impossibile scrivere nel file della rubrica telefonica specificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-162">Cannot write to the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <span data-ttu-id="89aa1-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-164">Le informazioni contenute nella rubrica specificata non sono valide.</span><span class="sxs-lookup"><span data-stu-id="89aa1-164">Information found in the specified phone book is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <span data-ttu-id="89aa1-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-166">Non è stato possibile caricare una stringa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-166">A string could not be loaded.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-167">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-167">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <span data-ttu-id="89aa1-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-169">Impossibile trovare la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-169">Cannot find the specified key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <span data-ttu-id="89aa1-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-171">La porta specificata è stata disconnessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-171">The specified port was disconnected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <span data-ttu-id="89aa1-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-173">La porta specificata è stata disconnessa dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-173">The specified port was disconnected by the remote computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <span data-ttu-id="89aa1-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-175">La porta specificata è stata disconnessa a causa di un errore hardware.</span><span class="sxs-lookup"><span data-stu-id="89aa1-175">The specified port was disconnected due to hardware failure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <span data-ttu-id="89aa1-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-177">La porta specificata è stata disconnessa dall'utente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-177">The specified port was disconnected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <span data-ttu-id="89aa1-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-179">Dimensione della struttura non corretta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-179">Incorrect structure size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <span data-ttu-id="89aa1-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-181">La porta specificata è già in uso o non è configurata per la connessione remota di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-181">The specified port is already in use or is not configured for remote access dial-out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <span data-ttu-id="89aa1-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-183">Non è stato possibile registrare il computer nella rete remota.</span><span class="sxs-lookup"><span data-stu-id="89aa1-183">Your computer could not be registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-184">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-184">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <span data-ttu-id="89aa1-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-186">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-186">An unknown error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <span data-ttu-id="89aa1-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-188">Il dispositivo errato è collegato alla porta specificata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-188">The wrong device is attached to the specified port.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <span data-ttu-id="89aa1-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-190">È stata rilevata una stringa che non è stato possibile convertire.</span><span class="sxs-lookup"><span data-stu-id="89aa1-190">A string was detected that could not be converted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-191">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-191">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <span data-ttu-id="89aa1-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-193">Timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-193">The request has timed out.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <span data-ttu-id="89aa1-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-195">Nessuna rete asincrona disponibile.</span><span class="sxs-lookup"><span data-stu-id="89aa1-195">No asynchronous net is available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-196">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-196">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <span data-ttu-id="89aa1-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-198">Si è verificato un errore relativo a NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="89aa1-198">An error has occurred involving NetBIOS.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-199">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-199">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <span data-ttu-id="89aa1-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-201">il server non è in grado di allocare le risorse NetBIOS necessarie per supportare il client.</span><span class="sxs-lookup"><span data-stu-id="89aa1-201">he server cannot allocate NetBIOS resources needed to support the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-202">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-202">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <span data-ttu-id="89aa1-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-204">Uno dei nomi NetBIOS del computer è già registrato nella rete remota.</span><span class="sxs-lookup"><span data-stu-id="89aa1-204">One of your computer's NetBIOS names is already registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-205">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-205">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <span data-ttu-id="89aa1-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-207">Una scheda di rete nel server non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-207">A network adapter at the server failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-208">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-208">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <span data-ttu-id="89aa1-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-210">Non si riceveranno popup del messaggio di rete.</span><span class="sxs-lookup"><span data-stu-id="89aa1-210">You will not receive network message popups.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-211">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-211">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <span data-ttu-id="89aa1-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-213">Si è verificato un errore di autenticazione interno.</span><span class="sxs-lookup"><span data-stu-id="89aa1-213">An internal authentication error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <span data-ttu-id="89aa1-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-215">L'account specificato non è autorizzato ad accedere a questa ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="89aa1-215">The specified account is not permitted to log in at this time of day.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <span data-ttu-id="89aa1-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-217">L'account specificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-217">The specified account is disabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <span data-ttu-id="89aa1-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-219">La password specificata è scaduta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-219">The specified password has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <span data-ttu-id="89aa1-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-221">L'account specificato non dispone delle autorizzazioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-221">The specified account does not have remote access permissions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <span data-ttu-id="89aa1-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-223">Il server di accesso remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="89aa1-223">The remote access server is not responding.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-224">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-224">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <span data-ttu-id="89aa1-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-226">Il modem o un altro dispositivo di connessione ha segnalato un errore.</span><span class="sxs-lookup"><span data-stu-id="89aa1-226">Your modem or other connection device has reported an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <span data-ttu-id="89aa1-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-228">Una risposta non riconosciuta è stata restituita dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-228">An unrecognized response was returned by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <span data-ttu-id="89aa1-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-230">Una macro richiesta dal dispositivo non è stata trovata nel dispositivo. Sezione del file INF.</span><span class="sxs-lookup"><span data-stu-id="89aa1-230">A macro required by the device was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <span data-ttu-id="89aa1-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-232">Comando o risposta nel dispositivo. La sezione del file INF fa riferimento a una macro non definita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-232">A command or response in the device .INF file section refers to an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <span data-ttu-id="89aa1-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-234">La <message> macro non è stata trovata nel dispositivo. Sezione del file INF.</span><span class="sxs-lookup"><span data-stu-id="89aa1-234">The <message> macro was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <span data-ttu-id="89aa1-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-236">La <defaultoff> macro nel dispositivo. La sezione del file INF contiene una macro non definita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-236">The <defaultoff> macro in the device .INF file section contains an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <span data-ttu-id="89aa1-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-238">Il dispositivo. Non è stato possibile aprire il file INF.</span><span class="sxs-lookup"><span data-stu-id="89aa1-238">The device .INF file could not be opened.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <span data-ttu-id="89aa1-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-240">Nome del dispositivo nel dispositivo. INF o supporti. Il file INI è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-240">The device name in the device .INF or media .INI file is too long.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <span data-ttu-id="89aa1-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-242">Supporti. Il file INI fa riferimento a un nome di dispositivo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-242">The media .INI file refers to an unknown device name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <span data-ttu-id="89aa1-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-244">Il dispositivo. Il file INF non contiene risposte per il comando.</span><span class="sxs-lookup"><span data-stu-id="89aa1-244">The device .INF file contains no responses for the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <span data-ttu-id="89aa1-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-246">Il dispositivo. Nel file INF manca un comando.</span><span class="sxs-lookup"><span data-stu-id="89aa1-246">The device .INF file is missing a command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <span data-ttu-id="89aa1-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-248">Si è tentato di impostare una macro non elencata nel dispositivo. Sezione del file INF.</span><span class="sxs-lookup"><span data-stu-id="89aa1-248">Attempted to set a macro not listed in device .INF file section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <span data-ttu-id="89aa1-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-250">Supporti. Il file INI fa riferimento a un tipo di dispositivo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-250">The media .INI file refers to an unknown device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <span data-ttu-id="89aa1-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-252">Impossibile allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="89aa1-252">Cannot allocate memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <span data-ttu-id="89aa1-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-254">La porta non è configurata per l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-254">The port is not configured for remote access.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <span data-ttu-id="89aa1-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-256">Il modem o un altro dispositivo di connessione non funziona.</span><span class="sxs-lookup"><span data-stu-id="89aa1-256">Your modem or other connection device is not functioning.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <span data-ttu-id="89aa1-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-258">Impossibile leggere i supporti. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-258">Cannot read the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <span data-ttu-id="89aa1-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-260">La connessione è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-260">The connection was dropped.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <span data-ttu-id="89aa1-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-262">Il parametro Usage nel file media. ini non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-262">The usage parameter in the media .ini file is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <span data-ttu-id="89aa1-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-264">Impossibile leggere il nome della sezione dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-264">Cannot read the section name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <span data-ttu-id="89aa1-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-266">Impossibile leggere il tipo di dispositivo dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-266">Cannot read the device type from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <span data-ttu-id="89aa1-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-268">Impossibile leggere il nome del dispositivo dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-268">Cannot read the device name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <span data-ttu-id="89aa1-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-270">Impossibile leggere l'utilizzo dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-270">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <span data-ttu-id="89aa1-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-272">Il sistema non è riuscito a leggere la velocità massima di connessione del vettore dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-272">The system was unable to read the maximum carrier connection speed from the media .INI file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-273">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-273">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <span data-ttu-id="89aa1-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-275">Impossibile leggere l'utilizzo dal supporto. File INI.</span><span class="sxs-lookup"><span data-stu-id="89aa1-275">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <span data-ttu-id="89aa1-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-277">La riga è occupata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-277">The line is busy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <span data-ttu-id="89aa1-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-279">Persona che ha risposto anziché modem.</span><span class="sxs-lookup"><span data-stu-id="89aa1-279">A person answered instead of a modem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <span data-ttu-id="89aa1-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-281">Non esiste alcuna risposta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-281">There is no answer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <span data-ttu-id="89aa1-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-283">Non è possibile rilevare un segnale del vettore.</span><span class="sxs-lookup"><span data-stu-id="89aa1-283">Cannot detect a carrier signal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <span data-ttu-id="89aa1-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-285">Nessun segnale di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-285">There is no dial tone.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <span data-ttu-id="89aa1-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-287">Il modem (o un altro dispositivo di connessione) ha segnalato un errore generale.</span><span class="sxs-lookup"><span data-stu-id="89aa1-287">The modem (or other connecting device) reported a general error.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-288">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-288">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <span data-ttu-id="89aa1-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-290">Si è verificato un errore durante la scrittura del nome della sezione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-290">There was an error in writing the section name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <span data-ttu-id="89aa1-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-292">Si è verificato un errore durante la scrittura del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-292">There was an error in writing the device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <span data-ttu-id="89aa1-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-294">Si è verificato un errore durante la scrittura del nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-294">There was an error in writing the device name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <span data-ttu-id="89aa1-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-296">Si è verificato un errore durante la scrittura della velocità massima della connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-296">There was an error in writing the maximum connection speed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <span data-ttu-id="89aa1-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-298">Si è verificato un errore durante la scrittura della velocità massima del vettore.</span><span class="sxs-lookup"><span data-stu-id="89aa1-298">There was an error in writing the maximum carrier speed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <span data-ttu-id="89aa1-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-300">Si è verificato un errore durante la scrittura dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-300">There was an error in writing the usage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <span data-ttu-id="89aa1-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-302">Si è verificato un errore durante la scrittura del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="89aa1-302">There was an error in writing the default-off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <span data-ttu-id="89aa1-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span></span></dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <span data-ttu-id="89aa1-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-305">Supporti. Il file INI è vuoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-305">The media .INI file is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <span data-ttu-id="89aa1-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-307">Accesso negato perché il nome utente, la password o entrambi non sono validi per il dominio.</span><span class="sxs-lookup"><span data-stu-id="89aa1-307">Access denied because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <span data-ttu-id="89aa1-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-309">Si è verificato un errore hardware nella porta o nel dispositivo collegato</span><span class="sxs-lookup"><span data-stu-id="89aa1-309">A hardware failure has occurred in the port or attached device</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <span data-ttu-id="89aa1-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-311">La macro non è una macro binaria.</span><span class="sxs-lookup"><span data-stu-id="89aa1-311">The macro is not a binary macro.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <span data-ttu-id="89aa1-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-313">DCB non trovato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-313">DCB not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <span data-ttu-id="89aa1-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-315">Le macchine a Stati non sono avviate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-315">State machines are not started.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <span data-ttu-id="89aa1-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-317">Le macchine a Stati sono già avviate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-317">State machines are already started.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <span data-ttu-id="89aa1-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-319">Ciclo di risposta parziale.</span><span class="sxs-lookup"><span data-stu-id="89aa1-319">Partial response looping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <span data-ttu-id="89aa1-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-321">Nome della chiave di risposta nel dispositivo. Il file INF non è nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-321">A response key name in the device .INF file is not in the expected format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <span data-ttu-id="89aa1-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-323">La risposta del dispositivo ha causato un overflow del buffer.</span><span class="sxs-lookup"><span data-stu-id="89aa1-323">The device response caused a buffer overflow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <span data-ttu-id="89aa1-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-325">Comando espanso nel dispositivo. Il file INF è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-325">The expanded command in the device .INF file is too long.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <span data-ttu-id="89aa1-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-327">Il dispositivo è stato spostato in una velocità di connessione non supportata dal driver COM.</span><span class="sxs-lookup"><span data-stu-id="89aa1-327">The device moved to a connection speed that is not supported by the COM driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <span data-ttu-id="89aa1-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-329">Risposta del dispositivo ricevuta quando non è previsto alcun valore.</span><span class="sxs-lookup"><span data-stu-id="89aa1-329">Device response received when none expected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <span data-ttu-id="89aa1-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-331">Si è verificato un errore perché è abilitata la modalità interattiva.</span><span class="sxs-lookup"><span data-stu-id="89aa1-331">An error occurred because the interactive mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <span data-ttu-id="89aa1-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-333">È stato specificato un numero di callback non valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-333">A bad callback number was specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <span data-ttu-id="89aa1-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-335">Lo stato di autenticazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-335">The specified authentication state is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <span data-ttu-id="89aa1-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-337">Si è verificato un errore durante la scrittura della velocità di connessione iniziale.</span><span class="sxs-lookup"><span data-stu-id="89aa1-337">An error occurred when writing the initial connection speed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-338">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-338">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <span data-ttu-id="89aa1-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-340">È stata ricevuta un'indicazione di diagnostica X. 25.</span><span class="sxs-lookup"><span data-stu-id="89aa1-340">An X.25 diagnostic indication was received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <span data-ttu-id="89aa1-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-342">L'account specificato è scaduto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-342">The specified account has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <span data-ttu-id="89aa1-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-344">Si è verificato un errore durante il tentativo di modificare la password nel dominio.</span><span class="sxs-lookup"><span data-stu-id="89aa1-344">An error occurred while attempting to change the password on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <span data-ttu-id="89aa1-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-346">Sono stati rilevati errori di sovraccarico seriale durante la comunicazione con il modem.</span><span class="sxs-lookup"><span data-stu-id="89aa1-346">Serial overrun errors were detected while communicating with your modem.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <span data-ttu-id="89aa1-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-348">Errore di inizializzazione di RasMan.</span><span class="sxs-lookup"><span data-stu-id="89aa1-348">RasMan initialization failure.</span></span> <span data-ttu-id="89aa1-349">Controllare il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="89aa1-349">Check the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <span data-ttu-id="89aa1-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-351">Inizializzazione della porta bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="89aa1-351">The two-way port is initializing.</span></span> <span data-ttu-id="89aa1-352">Attendere alcuni secondi e ricomporre.</span><span class="sxs-lookup"><span data-stu-id="89aa1-352">Wait a few seconds and redial.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-353">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-353">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <span data-ttu-id="89aa1-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-355">Non sono disponibili linee ISDN attive.</span><span class="sxs-lookup"><span data-stu-id="89aa1-355">No active ISDN lines are available.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <span data-ttu-id="89aa1-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-357">Nessun canale ISDN disponibile per effettuare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-357">No ISDN channels are available to make the call.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-358">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-358">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <span data-ttu-id="89aa1-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-360">Si sono verificati troppi errori a causa della scarsa qualità della linea telefonica.</span><span class="sxs-lookup"><span data-stu-id="89aa1-360">Too many errors occurred because of poor phone line quality.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-361">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-361">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <span data-ttu-id="89aa1-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-363">La configurazione IP di accesso remoto è inutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="89aa1-363">The remote access IP configuration is unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <span data-ttu-id="89aa1-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-365">Non sono disponibili indirizzi IP nel pool statico di indirizzi IP di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-365">No IP addresses are available in the static pool of remote access IP addresses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <span data-ttu-id="89aa1-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-367">Si è verificato un timeout di PPP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-367">A PPP timeout occurred.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <span data-ttu-id="89aa1-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-369">La connessione è stata interrotta dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-369">The connection was terminated by the remote computer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-370">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-370">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <span data-ttu-id="89aa1-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-372">Non sono configurati protocolli di controllo PPP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-372">No PPP control protocols are configured.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <span data-ttu-id="89aa1-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-374">Il peer PPP remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="89aa1-374">The remote PPP peer is not responding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <span data-ttu-id="89aa1-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-376">Il pacchetto PPP non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-376">The PPP packet is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <span data-ttu-id="89aa1-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-378">Il numero di telefono, inclusi il prefisso e il suffisso, è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-378">The phone number, including the prefix and suffix, is too long.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <span data-ttu-id="89aa1-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-380">Il protocollo IPX non può comparire sul modem (o su un altro dispositivo di connessione) perché il computer non è configurato per la connessione (si tratta di un router IPX).</span><span class="sxs-lookup"><span data-stu-id="89aa1-380">The IPX protocol cannot dial out on the modem (or other connecting device) because this computer is not configured for dialing out (it is an IPX router).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-381">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-381">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <span data-ttu-id="89aa1-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-383">Il protocollo IPX non è in grado di connettersi al modem (o a un altro dispositivo di connessione) perché il computer non è configurato per la connessione (il router IPX non è installato).</span><span class="sxs-lookup"><span data-stu-id="89aa1-383">The IPX protocol cannot dial in on the modem (or other connecting device) because this computer is not configured for dialing in (the IPX router is not installed).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-384">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-384">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <span data-ttu-id="89aa1-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-386">Il protocollo IPX non può essere utilizzato per la connessione remota su più di una porta alla volta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-386">The IPX protocol cannot be used for dial-out on more than one port at a time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <span data-ttu-id="89aa1-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-388">Impossibile accedere TCPCFG.DLL.</span><span class="sxs-lookup"><span data-stu-id="89aa1-388">Cannot access TCPCFG.DLL.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-389">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-389">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <span data-ttu-id="89aa1-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-391">Impossibile trovare una scheda IP associata all'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-391">Cannot find an IP adapter bound to remote access.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <span data-ttu-id="89aa1-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-393">Non è possibile utilizzare SLIP a meno che non sia installato il protocollo IP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-393">SLIP cannot be used unless the IP protocol is installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <span data-ttu-id="89aa1-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-395">La registrazione del computer non è completa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-395">Computer registration is not complete.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-396">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-396">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <span data-ttu-id="89aa1-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-398">Il protocollo specificato non è configurato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-398">The specified protocol is not configured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <span data-ttu-id="89aa1-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-400">La negoziazione PPP non è convergente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-400">The PPP negotiation is not converging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <span data-ttu-id="89aa1-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-402">il protocollo di controllo PPP per il protocollo di rete specificato non è disponibile nel server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-402">the PPP control protocol for the specified network protocol is not available on the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <span data-ttu-id="89aa1-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-404">Il protocollo di controllo dei collegamenti PPP è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-404">The PPP link control protocol was terminated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <span data-ttu-id="89aa1-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-406">L'indirizzo richiesto è stato rifiutato dal server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-406">The requested address was rejected by the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <span data-ttu-id="89aa1-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-408">Il protocollo di controllo è stato terminato dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-408">The remote computer terminated the control protocol.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <span data-ttu-id="89aa1-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-410">Loopback rilevato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-410">Loopback detected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <span data-ttu-id="89aa1-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-412">Il server non ha assegnato un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-412">The server did not assign an address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <span data-ttu-id="89aa1-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-414">Il server remoto non è in grado di utilizzare la password crittografata di Windows NT.</span><span class="sxs-lookup"><span data-stu-id="89aa1-414">The remote server cannot use the Windows NT encrypted password.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <span data-ttu-id="89aa1-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-416">Impossibile inizializzare o non installare correttamente i dispositivi TAPI configurati per l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-416">The TAPI devices configured for remote access failed to initialize or were not installed correctly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <span data-ttu-id="89aa1-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-418">Il computer locale non supporta la crittografia.</span><span class="sxs-lookup"><span data-stu-id="89aa1-418">The local computer does not support encryption.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <span data-ttu-id="89aa1-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-420">Il server remoto non supporta la crittografia.</span><span class="sxs-lookup"><span data-stu-id="89aa1-420">The remote server does not support encryption.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <span data-ttu-id="89aa1-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-422">Il computer remoto richiede la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="89aa1-422">The remote computer requires data encryption.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-423">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-423">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <span data-ttu-id="89aa1-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-425">Il sistema non è in grado di utilizzare il numero di rete IPX assegnato dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-425">The system cannot use the IPX network number assigned by the remote computer.</span></span> <span data-ttu-id="89aa1-426">Nel registro eventi vengono fornite informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89aa1-426">Additional information is provided in the event log.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-427">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-427">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <span data-ttu-id="89aa1-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-429">Il modulo di gestione della sessione (SMM) non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-429">The Session Management Module (SMM) is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-430">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-430">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <span data-ttu-id="89aa1-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-432">Il SMM non è inizializzato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-432">The SMM is uninitialized.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-433">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-433">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <span data-ttu-id="89aa1-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-435">Nessun MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-435">No MAC for port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-436">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-436">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <span data-ttu-id="89aa1-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-438">Timeout di SMM.</span><span class="sxs-lookup"><span data-stu-id="89aa1-438">The SMM timed out.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-439">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-439">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <span data-ttu-id="89aa1-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-441">È stato specificato un numero di telefono non valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-441">A bad phone number was specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <span data-ttu-id="89aa1-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-443">Il SMM errato è stato specificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-443">The wrong SMM was specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-444">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-444">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <span data-ttu-id="89aa1-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-446">Il numero di callback contiene un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-446">The callback number contains a character that is not valid.</span></span> <span data-ttu-id="89aa1-447">Sono consentiti solo i 18 caratteri seguenti: da 0 a 9, T, P, W, (,),-, @ e spazio.</span><span class="sxs-lookup"><span data-stu-id="89aa1-447">Only the following 18 characters are allowed: 0 to 9, T, P, W, (, ), -, @, and space.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-448">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-448">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <span data-ttu-id="89aa1-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-450">Si è verificato un errore di sintassi durante l'elaborazione di uno script.</span><span class="sxs-lookup"><span data-stu-id="89aa1-450">A syntax error was encountered while processing a script.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <span data-ttu-id="89aa1-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-452">Non è stato possibile disconnettere la connessione perché è stata creata dal router multiprotocollo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-452">The connection could not be disconnected because it was created by the multi-protocol router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <span data-ttu-id="89aa1-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-454">Il sistema non è riuscito a trovare il bundle a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="89aa1-454">The system could not find the multi-link bundle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <span data-ttu-id="89aa1-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-456">Il sistema non è in grado di eseguire la connessione automatica perché per questa connessione è stato specificato un dialer personalizzato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-456">The system cannot perform automated dial because this connection has a custom dialer specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <span data-ttu-id="89aa1-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-458">Questa connessione è già in corso di composizione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-458">This connection is already being dialed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <span data-ttu-id="89aa1-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-460">Non è stato possibile avviare automaticamente RAS.</span><span class="sxs-lookup"><span data-stu-id="89aa1-460">RAS could not be started automatically.</span></span> <span data-ttu-id="89aa1-461">Nel registro eventi vengono fornite informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89aa1-461">Additional information is provided in the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <span data-ttu-id="89aa1-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-463">Condivisione connessione Internet (ICS) è già abilitata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-463">Internet Connection Sharing (ICS) is already enabled on the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-464">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-464">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <span data-ttu-id="89aa1-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-466">Si è verificato un errore durante la modifica delle impostazioni di condivisione della connessione Internet esistenti.</span><span class="sxs-lookup"><span data-stu-id="89aa1-466">An error occurred while the existing Internet Connection Sharing settings were being changed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-467">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-467">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <span data-ttu-id="89aa1-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-469">Si è verificato un errore durante l'abilitazione delle funzionalità di routing.</span><span class="sxs-lookup"><span data-stu-id="89aa1-469">An error occurred while routing capabilities were being enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-470">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-470">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <span data-ttu-id="89aa1-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-472">Si è verificato un errore durante l'abilitazione della condivisione della connessione Internet per la connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-472">An error occurred while Internet Connection Sharing was being enabled for the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-473">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-473">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <span data-ttu-id="89aa1-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-475">Si è verificato un errore durante la configurazione della rete locale per la condivisione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-475">An error occurred while the local network was being configured for sharing.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-476">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-476">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <span data-ttu-id="89aa1-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-478">Non è possibile abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-478">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="89aa1-479">È presente più di una connessione LAN diversa dalla connessione da condividere.</span><span class="sxs-lookup"><span data-stu-id="89aa1-479">There is more than one LAN connection other than the connection to be shared.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-480">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-480">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <span data-ttu-id="89aa1-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-482">Nessun lettore di smart card installato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-482">No smart card reader is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <span data-ttu-id="89aa1-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-484">Non è possibile abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-484">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="89aa1-485">Una connessione LAN è già configurata con l'indirizzo IP richiesto per l'indirizzamento automatico degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-485">A LAN connection is already configured with the IP address that is required for automatic IP addressing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <span data-ttu-id="89aa1-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-487">Impossibile trovare un certificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-487">A certificate could not be found.</span></span> <span data-ttu-id="89aa1-488">Per le connessioni che utilizzano il protocollo L2TP su IPSec è richiesta l'installazione di un certificato del computer, noto anche come certificato del computer.</span><span class="sxs-lookup"><span data-stu-id="89aa1-488">Connections that use the L2TP protocol over IPSec require the installation of a machine certificate, also known as a computer certificate.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <span data-ttu-id="89aa1-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-490">Non è possibile abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-490">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="89aa1-491">Per la connessione LAN selezionata come rete privata è stato configurato più di un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-491">The LAN connection selected as the private network has more than one IP address configured.</span></span> <span data-ttu-id="89aa1-492">Riconfigurare la connessione LAN con un singolo indirizzo IP prima di abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-492">Please reconfigure the LAN connection with a single IP address before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <span data-ttu-id="89aa1-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-494">Tentativo di connessione non riuscito a causa dell'impossibilità di crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="89aa1-494">The connection attempt failed because of failure to encrypt data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <span data-ttu-id="89aa1-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-496">La destinazione specificata non è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="89aa1-496">The specified destination is not reachable.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <span data-ttu-id="89aa1-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-498">Il computer remoto ha rifiutato il tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-498">The remote computer rejected the connection attempt.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <span data-ttu-id="89aa1-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-500">Il tentativo di connessione non è riuscito perché la rete è occupata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-500">The connection attempt failed because the network is busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <span data-ttu-id="89aa1-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-502">L'hardware di rete del computer remoto non è compatibile con il tipo di chiamata richiesta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-502">The remote computer's network hardware is incompatible with the type of call requested.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <span data-ttu-id="89aa1-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-504">Il tentativo di connessione non è riuscito perché il numero di destinazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-504">The connection attempt failed because the destination number has changed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <span data-ttu-id="89aa1-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-506">Il tentativo di connessione non è riuscito a causa di un errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="89aa1-506">The connection attempt failed because of a temporary failure.</span></span> <span data-ttu-id="89aa1-507">Provare a eseguire di nuovo la connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-507">Try connecting again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <span data-ttu-id="89aa1-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-509">La chiamata è stata bloccata dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-509">The call was blocked by the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <span data-ttu-id="89aa1-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-511">Non è stato possibile connettere la chiamata perché il computer remoto ha richiamato la funzionalità non disturbare.</span><span class="sxs-lookup"><span data-stu-id="89aa1-511">The call could not be connected because the remote computer has invoked the Do Not Disturb feature.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <span data-ttu-id="89aa1-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-513">Il tentativo di connessione non è riuscito perché il modem o un altro dispositivo di connessione nel computer remoto non è in ordine.</span><span class="sxs-lookup"><span data-stu-id="89aa1-513">The connection attempt failed because the modem or other connection device on the remote computer is out of order.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <span data-ttu-id="89aa1-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-515">Non è stato possibile verificare l'identità del server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-515">It was not possible to verify the identity of the server.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <span data-ttu-id="89aa1-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-517">Per eseguire la connessione utilizzando questa connessione, è necessario utilizzare una smart card.</span><span class="sxs-lookup"><span data-stu-id="89aa1-517">To dial out using this connection you must use a smart card.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-518">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-518">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <span data-ttu-id="89aa1-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-520">Una funzione tentata non è valida per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-520">An attempted function is not valid for this connection.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <span data-ttu-id="89aa1-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-522">Il tentativo di crittografia non è riuscito perché non è stato trovato alcun certificato valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-522">The encryption attempt failed because no valid certificate was found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-523">Deprecato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-523">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <span data-ttu-id="89aa1-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-525">La condivisione della connessione (NAT) è attualmente installata come protocollo di routing e deve essere rimossa prima di abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-525">Connection Sharing (NAT) is currently installed as a routing protocol, and must be removed before enabling Internet Connection Sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <span data-ttu-id="89aa1-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-527">Non è possibile abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-527">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="89aa1-528">La connessione LAN selezionata come rete privata non è presente o è disconnessa dalla rete.</span><span class="sxs-lookup"><span data-stu-id="89aa1-528">The LAN connection selected as the private network is either not present, or is disconnected from the network.</span></span> <span data-ttu-id="89aa1-529">Verificare che la scheda LAN sia connessa prima di abilitare la condivisione della connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="89aa1-529">Please ensure that the LAN adapter is connected before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <span data-ttu-id="89aa1-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-531">Non è possibile comporre utilizzando questa connessione al momento dell'accesso perché è configurata per l'utilizzo di un nome utente diverso da quello della smart card.</span><span class="sxs-lookup"><span data-stu-id="89aa1-531">You cannot dial using this connection at login time because it is configured to use a user name different than the one on the smart card.</span></span> <span data-ttu-id="89aa1-532">Se si desidera utilizzare questa connessione al momento dell'accesso, è necessario configurarla in modo che utilizzi il nome utente nella smart card.</span><span class="sxs-lookup"><span data-stu-id="89aa1-532">If you want to use this connection at login time, you must configure it to use the user name on the smart card.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <span data-ttu-id="89aa1-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-534">Non è possibile comporre utilizzando questa connessione al momento dell'accesso perché non è configurata per l'utilizzo di una smart card.</span><span class="sxs-lookup"><span data-stu-id="89aa1-534">You cannot dial using this connection at login time because it is not configured to use a smart card.</span></span> <span data-ttu-id="89aa1-535">Se si desidera utilizzarlo al momento dell'accesso, è necessario modificare le proprietà della connessione in modo che utilizzi una smart card.</span><span class="sxs-lookup"><span data-stu-id="89aa1-535">If you want to use it at login time, you must edit the properties of this connection so that it uses a smart card.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <span data-ttu-id="89aa1-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-537">Il tentativo di connessione L2TP non è riuscito perché non è presente alcun certificato computer valido per l'autenticazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="89aa1-537">The L2TP connection attempt failed because there is no valid machine certificate on your computer for security authentication.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <span data-ttu-id="89aa1-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-539">Il tentativo di connessione L2TP non è riuscito perché il livello di protezione non è stato in grado di autenticare il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-539">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <span data-ttu-id="89aa1-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-541">Il tentativo di connessione L2TP non è riuscito perché il livello di sicurezza non è riuscito a negoziare i parametri compatibili con il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-541">The L2TP connection attempt failed because the security layer could not negotiate compatible parameters with the remote computer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <span data-ttu-id="89aa1-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-543">Il tentativo di connessione L2TP non è riuscito perché si è verificato un errore di elaborazione durante le negoziazioni iniziali con il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-543">The L2TP connection attempt failed because the security layer encountered a processing error during initial negotiations with the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <span data-ttu-id="89aa1-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-545">Il tentativo di connessione L2TP non è riuscito perché la convalida del certificato nel computer remoto non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-545">The L2TP connection attempt failed because certificate validation on the remote computer failed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <span data-ttu-id="89aa1-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-547">Tentativo di connessione L2TP non riuscito. Impossibile trovare i criteri di sicurezza per la connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-547">The L2TP connection attempt failed because security policy for the connection was not found.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <span data-ttu-id="89aa1-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-549">Tentativo di connessione L2TP non riuscito perché si è verificato il timeout della negoziazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="89aa1-549">The L2TP connection attempt failed because security negotiation timed out.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <span data-ttu-id="89aa1-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-551">Il tentativo di connessione L2TP non è riuscito perché si è verificato un errore durante la negoziazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="89aa1-551">The L2TP connection attempt failed because an error occurred while negotiating security.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <span data-ttu-id="89aa1-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-553">L'attributo RADIUS del protocollo con frame per questo utente non è PPP.</span><span class="sxs-lookup"><span data-stu-id="89aa1-553">The Framed Protocol RADIUS attribute for this user is not PPP.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <span data-ttu-id="89aa1-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-555">L'attributo RADIUS del tipo di tunnel per questo utente non è corretto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-555">The Tunnel Type RADIUS attribute for this user is not correct.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <span data-ttu-id="89aa1-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-557">L'attributo RADIUS del tipo di servizio per questo utente non è Framed né un callback con frame.</span><span class="sxs-lookup"><span data-stu-id="89aa1-557">The Service Type RADIUS attribute for this user is neither Framed nor Callback Framed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <span data-ttu-id="89aa1-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-559">Impossibile stabilire una connessione al computer remoto perché il modem non è stato trovato o è occupato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-559">A connection to the remote computer could not be established because the modem was not found or was busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <span data-ttu-id="89aa1-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-561">Impossibile trovare un certificato che può essere utilizzato con il protocollo EAP (Extensible Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="89aa1-561">A certificate could not be found that can be used with the Extensible Authentication Protocol (EAP).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <span data-ttu-id="89aa1-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-563">Non è possibile abilitare la condivisione della connessione Internet (ICS) a causa di un conflitto di indirizzi IP nella rete.</span><span class="sxs-lookup"><span data-stu-id="89aa1-563">Internet Connection Sharing (ICS) cannot be enabled due to an IP address conflict on the network.</span></span> <span data-ttu-id="89aa1-564">ICS richiede che l'host sia configurato per l'uso di <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="89aa1-564">ICS requires the host be configured to use <strong>192.168.0.1</strong>.</span></span> <span data-ttu-id="89aa1-565">Assicurarsi che nessun altro client nella rete sia configurato per l'uso di <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="89aa1-565">Ensure that no other client on the network is configured to use <strong>192.168.0.1</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-566">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-566">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-567">Windows 7 e versioni successive: l'host deve essere configurato per l'uso di <strong>192.168.137.1</strong>
</span><span class="sxs-lookup"><span data-stu-id="89aa1-567">Windows 7 and later: The host must be configured to use <strong>192.168.137.1</strong>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <span data-ttu-id="89aa1-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-569">Non è possibile stabilire la connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-569">Unable to establish the VPN connection.</span></span> <span data-ttu-id="89aa1-570">Il server VPN potrebbe non essere raggiungibile oppure è possibile che i parametri di sicurezza non siano configurati correttamente per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-570">The VPN server may be unreachable, or security parameters may not be configured properly for this connection.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-571">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-571">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <span data-ttu-id="89aa1-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-573">Questa connessione è configurata in modo da convalidare l'identità del server di accesso, ma Windows non è in grado di verificare il certificato digitale inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-573">This connection is configured to validate the identity of the access server, but Windows cannot verify the digital certificate sent by the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-574">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-574">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <span data-ttu-id="89aa1-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-576">La scheda specificata non è stata riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-576">The card supplied was not recognized.</span></span> <span data-ttu-id="89aa1-577">Verificare che la scheda sia inserita correttamente e che si trovi in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="89aa1-577">Please check that the card is inserted correctly, and fits securely.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-578">Supportato in Windows XP con SP1 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-578">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <span data-ttu-id="89aa1-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-580">La configurazione PEAP archiviata nel cookie di sessione non corrisponde alla configurazione della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-580">The PEAP configuration stored in the session cookie does not match the current session configuration.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-581">Supportato in Windows XP con SP1 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-581">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <span data-ttu-id="89aa1-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-583">L'identità PEAP archiviata nel cookie di sessione non corrisponde all'identità corrente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-583">The PEAP identity stored in the session cookie does not match the current identity.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-584">Supportato in Windows XP con SP1 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-584">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <span data-ttu-id="89aa1-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-586">Non è possibile comporre utilizzando questa connessione al momento dell'accesso perché è configurata per l'utilizzo delle credenziali dell'utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-586">You cannot dial using this connection at login time because it is configured to use the currently-logged-in user's credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-587">Supportato in Windows XP con SP1 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-587">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <span data-ttu-id="89aa1-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-589">Una connessione tra il computer e il server VPN è stata avviata, ma non è possibile completare la connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-589">A connection between your computer and the VPN server has been started, but the VPN connection cannot be completed.</span></span> <span data-ttu-id="89aa1-590">La ragione più comune è che almeno un dispositivo Internet (ad esempio un firewall o un router) tra il computer e il server VPN non è configurato per consentire i pacchetti di protocollo GRE (Generic Routing Encapsulation).</span><span class="sxs-lookup"><span data-stu-id="89aa1-590">The most common cause for this is that at least one Internet device (for example, a firewall or a router) between your computer and the VPN server is not configured to allow Generic Routing Encapsulation (GRE) protocol packets.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-591">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-591">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <span data-ttu-id="89aa1-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-593">La connessione di rete tra il computer e il server VPN è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-593">The network connection between your computer and the VPN server was interrupted.</span></span> <span data-ttu-id="89aa1-594">Ciò può essere causato da un problema nella trasmissione VPN ed è in genere il risultato della latenza Internet o semplicemente che il server VPN ha raggiunto la capacità.</span><span class="sxs-lookup"><span data-stu-id="89aa1-594">This can be caused by a problem in the VPN transmission and is commonly the result of internet latency or simply that your VPN server has reached capacity.</span></span> <span data-ttu-id="89aa1-595">Provare a riconnettersi al server VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-595">Try to reconnect to the VPN server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-596">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-596">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <span data-ttu-id="89aa1-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-598">Non è stato possibile stabilire la connessione di rete tra il computer e il server VPN perché il server remoto ha rifiutato la connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-598">The network connection between your computer and the VPN server could not be established because the remote server refused the connection.</span></span> <span data-ttu-id="89aa1-599">Ciò è in genere causato da una mancata corrispondenza tra la configurazione del server e le impostazioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-599">This is typically caused by a mismatch between the server's configuration and your connection settings.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-600">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-600">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <span data-ttu-id="89aa1-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-602">Non è stato possibile stabilire la connessione di rete tra il computer e il server VPN perché il server remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="89aa1-602">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="89aa1-603">Il problema potrebbe essere dovuto al fatto che uno dei dispositivi di rete (ad esempio, firewall, NAT, router) tra il computer e il server remoto non è configurato per consentire le connessioni VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-603">This could be because one of the network devices (for example, firewalls, NAT, routers) between your computer and the remote server is not configured to allow VPN connections.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-604">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-604">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <span data-ttu-id="89aa1-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-606">Una connessione di rete tra il computer e il server VPN è stata avviata, ma la connessione VPN non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-606">A network connection between your computer and the VPN server was started, but the VPN connection was not completed.</span></span> <span data-ttu-id="89aa1-607">Questo è in genere causato dall'utilizzo di un certificato non corretto o scaduto per l'autenticazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-607">This is typically caused by the use of an incorrect or expired certificate for authentication between the client and the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-608">Supportato in Windows Vista e nelle versioni successive di Windows</span><span class="sxs-lookup"><span data-stu-id="89aa1-608">Supported in Windows Vista and later versions of Windows</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <span data-ttu-id="89aa1-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-610">Non è stato possibile stabilire la connessione di rete tra il computer e il server VPN perché il server remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="89aa1-610">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="89aa1-611">Questa situazione è in genere causata da un problema di chiave precondivisa tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-611">This is typically caused by a pre-shared key problem between the client and server.</span></span> <span data-ttu-id="89aa1-612">Viene usata una chiave precondivisa per garantire che l'utente si trovi in un ciclo di comunicazione di protezione IP (IPSec).</span><span class="sxs-lookup"><span data-stu-id="89aa1-612">A pre-shared key is used to guarantee you are who you say you are in an IP Security (IPSec) communication cycle.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-613">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-613">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <span data-ttu-id="89aa1-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-615">impossibile stabilire la connessione a causa di un criterio configurato nel server RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-615">The connection was prevented because of a policy configured on your RAS/VPN server.</span></span> <span data-ttu-id="89aa1-616">In particolare, il metodo di autenticazione utilizzato dal server per verificare il nome utente e la password potrebbe non corrispondere al metodo di autenticazione configurato nel profilo di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-616">Specifically, the authentication method used by the server to verify your username and password may not match the authentication method configured in your connection profile.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-617">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-617">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <span data-ttu-id="89aa1-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-619">Si è provato a stabilire una seconda connessione a banda larga mentre è già stata stabilita una connessione a banda larga precedente con lo stesso dispositivo o la stessa porta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-619">You have attempted to establish a second broadband connection while a previous broadband connection is already established using the same device or port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-620">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-620">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <span data-ttu-id="89aa1-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-622">La connettività Ethernet sottostante necessaria per la connessione a banda larga non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-622">The underlying Ethernet connectivity required for the broadband connection was not found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-623">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-623">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <span data-ttu-id="89aa1-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-625">Non è stato possibile stabilire la connessione di rete a banda larga nel computer perché il server remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="89aa1-625">The broadband network connection could not be established on your computer because the remote server is not responding.</span></span> <span data-ttu-id="89aa1-626">Il problema potrebbe essere causato da un valore non valido per il campo ' nome servizio ' della connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-626">This could be caused by a value that is not valid for the 'Service Name' field for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-627">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-627">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <span data-ttu-id="89aa1-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-629">Una funzionalità o un'impostazione che si è tentato di abilitare non è più supportata dal servizio di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-629">A feature or setting you have tried to enable is no longer supported by the remote access service.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-630">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-630">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <span data-ttu-id="89aa1-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-632">Non è possibile eliminare una connessione mentre è connessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-632">Cannot delete a connection while it is connected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-633">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-633">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <span data-ttu-id="89aa1-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-635">Il client di imposizione Protezione accesso alla rete non è stato in grado di creare risorse di sistema per le connessioni di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-635">The Network Access Protection (NAP) enforcement client could not create system resources for remote access connections.</span></span> <span data-ttu-id="89aa1-636">Alcuni servizi o risorse di rete potrebbero non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-636">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-637">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-637">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <span data-ttu-id="89aa1-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-639">Il servizio agente protezione accesso alla rete (agente NAP) è stato disabilitato o non è installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="89aa1-639">The Network Access Protection Agent (NAP Agent) service has been disabled or is not installed on this computer.</span></span> <span data-ttu-id="89aa1-640">Alcuni servizi o risorse di rete potrebbero non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-640">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-641">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-641">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <span data-ttu-id="89aa1-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-643">Il client di imposizione Protezione accesso alla rete non è riuscito a eseguire la registrazione con il servizio agente protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="89aa1-643">The Network Access Protection (NAP) enforcement client failed to register with the Network Access Protection Agent (NAP Agent) service.</span></span> <span data-ttu-id="89aa1-644">Alcuni servizi o risorse di rete potrebbero non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-644">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-645">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-645">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <span data-ttu-id="89aa1-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-647">Il client di imposizione di protezione accesso alla rete non è stato in grado di elaborare la richiesta perché la connessione di accesso remoto non esiste.</span><span class="sxs-lookup"><span data-stu-id="89aa1-647">The Network Access Protection (NAP) enforcement client was unable to process the request because the remote access connection does not exist.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-648">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-648">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <span data-ttu-id="89aa1-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-650">Il client di imposizione di protezione accesso alla rete (NAP) non ha risposto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-650">The Network Access Protection (NAP) enforcement client did not respond.</span></span> <span data-ttu-id="89aa1-651">Alcuni servizi o risorse di rete potrebbero non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-651">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-652">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-652">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <span data-ttu-id="89aa1-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-654">Il Crypto-Binding tipo-lunghezza-valore (TLV) ricevuto non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-654">The Crypto-Binding type-length-value (TLV) received is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-655">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-655">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <span data-ttu-id="89aa1-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-657">Crypto-Binding TLV non è stato ricevuto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-657">Crypto-Binding TLV was not received.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-658">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-658">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <span data-ttu-id="89aa1-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-660">Il protocollo PPTP (Point-to-Point Tunneling Protocol) non è compatibile con IPv6.</span><span class="sxs-lookup"><span data-stu-id="89aa1-660">Point-to-Point Tunneling Protocol (PPTP) is incompatible with IPv6.</span></span> <span data-ttu-id="89aa1-661">Modificare il tipo di rete privata virtuale in L2TP (Layer Two Tunneling Protocol).</span><span class="sxs-lookup"><span data-stu-id="89aa1-661">Change the type of virtual private network to Layer Two Tunneling Protocol (L2TP).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-662">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-662">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <span data-ttu-id="89aa1-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-664">Convalida EAPTLS delle credenziali memorizzate nella cache non riuscita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-664">EAPTLS validation of the cached credentials failed.</span></span> <span data-ttu-id="89aa1-665">Rimuovere le credenziali memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="89aa1-665">Discard cached credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-666">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-666">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <span data-ttu-id="89aa1-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-668">Impossibile completare la connessione L2TP/IPsec perché il servizio moduli di chiavi IPSec IKE e AuthIP e/o il servizio motore di filtro di base non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-668">The L2TP/IPsec connection cannot be completed because the IKE and AuthIP IPSec Keying Modules service and/or the Base Filtering Engine service is not running.</span></span> <span data-ttu-id="89aa1-669">Questi servizi sono necessari per stabilire una connessione L2TP/IPSec.</span><span class="sxs-lookup"><span data-stu-id="89aa1-669">These services are required to establish an L2TP/IPSec connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-670">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-670">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <span data-ttu-id="89aa1-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-672">Connessione terminata a causa di un timeout di inattività.</span><span class="sxs-lookup"><span data-stu-id="89aa1-672">The connection was terminated because of idle timeout.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-673">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-673">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <span data-ttu-id="89aa1-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-675">Il modem (o un altro dispositivo di connessione) è stato disconnesso a causa di un errore di collegamento.</span><span class="sxs-lookup"><span data-stu-id="89aa1-675">The modem (or other connecting device) was disconnected due to link failure.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-676">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-676">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <span data-ttu-id="89aa1-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-678">La connessione è stata interrotta perché l'utente si è disconnesso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-678">The connection was terminated because user logged off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-679">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-679">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <span data-ttu-id="89aa1-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-681">La connessione è stata interrotta perché si è verificato un cambio utente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-681">The connection was terminated because user switch happened.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-682">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-682">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <span data-ttu-id="89aa1-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-684">La connessione è stata terminata a causa della sospensione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-684">The connection was terminated because of hibernation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-685">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-685">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <span data-ttu-id="89aa1-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-687">La connessione è stata interrotta perché il sistema è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-687">The connection was terminated because the system got suspended.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-688">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-688">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <span data-ttu-id="89aa1-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-690">Connessione terminata perché la gestione connessione di accesso remoto è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-690">The connection was terminated because Remote Access Connection manager stopped.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-691">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-691">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <span data-ttu-id="89aa1-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-693">Il tentativo di connessione L2TP non è riuscito perché il livello di protezione non è stato in grado di autenticare il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-693">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <span data-ttu-id="89aa1-694">Questo potrebbe essere dovuto al fatto che uno o più campi del certificato presentato dal server remoto non possono essere convalidati come appartenenti alla destinazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-694">This could be because one or more fields of the certificate presented by the remote server could not be validated as belonging to the target destination.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-695">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-695">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <span data-ttu-id="89aa1-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-697">Il computer non supporta protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="89aa1-697">The machine is not NAP capable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-698">Supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-698">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <span data-ttu-id="89aa1-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-700">ID tunnel non valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-700">Invalid Tunnel ID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-701">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-701">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <span data-ttu-id="89aa1-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-703">È in corso un'altra richiesta di aggiornamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-703">Another update connection request is in progress.</span></span> <span data-ttu-id="89aa1-704">RAS consente solo una richiesta di aggiornamento della connessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-704">RAS allows only one update connection request at a time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-705">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-705">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <span data-ttu-id="89aa1-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-707">La negoziazione con il protocollo configurato è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-707">Negotiating using configured protocol is disable.</span></span> <span data-ttu-id="89aa1-708">Modificare le proprietà di connessione e selezionare un protocollo diverso per la negoziazione, quindi riprovare.</span><span class="sxs-lookup"><span data-stu-id="89aa1-708">Edit connection properties and select different protocol for negotiation and try again.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-709">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-709">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <span data-ttu-id="89aa1-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-711">Negoziazione di indirizzi interni non riuscita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-711">Internal address negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-712">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-712">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <span data-ttu-id="89aa1-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-714">Il client deve richiedere un indirizzo IPv4 o IPv6 interno.</span><span class="sxs-lookup"><span data-stu-id="89aa1-714">Client has to request an Internal IPv4 or IPv6 address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-715">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-715">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <span data-ttu-id="89aa1-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-717">Negoziazione di selettori di traffico non riuscita.</span><span class="sxs-lookup"><span data-stu-id="89aa1-717">Traffic Selectors negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-718">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-718">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <span data-ttu-id="89aa1-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-720">La mobilità è disabilitata per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-720">Mobility is disabled for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-721">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-721">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <span data-ttu-id="89aa1-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-723">La connessione VPN sta ancora eseguendo la connessione o la ripetizione dell'autenticazione a causa della modifica dello stato di quarantena.</span><span class="sxs-lookup"><span data-stu-id="89aa1-723">The VPN Connection is still connecting or re-authenticating because of Quarantine state change.</span></span> <span data-ttu-id="89aa1-724">Avviare l'aggiornamento per dispositivi mobili solo quando lo stato della connessione è "connesso".</span><span class="sxs-lookup"><span data-stu-id="89aa1-724">Initiate mobile update only when connection state is 'Connected'.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-725">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-725">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <span data-ttu-id="89aa1-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-727">Il server ha rifiutato l'autenticazione client, a causa di un TLV imprevisto o di un valore non corrispondente per un TLV.</span><span class="sxs-lookup"><span data-stu-id="89aa1-727">Server rejected client authentication, due to unexpected TLV or value mismatch for a TLV.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-728">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-728">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <span data-ttu-id="89aa1-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-730">La preferenza di destinazione VPN non è selezionata dall'utente o non è più valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-730">Either VPN destination preference is not selected by the user or it is no longer valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-731">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-731">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <span data-ttu-id="89aa1-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-733">Credenziale smart card memorizzata nella cache non valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-733">Cached smart card credential is invalid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-734">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-734">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <span data-ttu-id="89aa1-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-736">Il tentativo di connessione VPN non è riuscito a causa di un errore interno durante l'aggiunta di cookie al protocollo SSTP (Secure Socket Tunneling Protocol).</span><span class="sxs-lookup"><span data-stu-id="89aa1-736">VPN connection attempt failed due to internal error occurred while adding cookies to the Secure Socket Tunneling Protocol (SSTP).</span></span> <span data-ttu-id="89aa1-737">Per informazioni dettagliate, vedere il registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="89aa1-737">Please see the System Event Log for the detailed information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <span data-ttu-id="89aa1-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-739">Gli attributi del metodo interno PEAP archiviati nel cookie non sono validi.</span><span class="sxs-lookup"><span data-stu-id="89aa1-739">The PEAP inner method attribute(s) stored in the cookie is/are invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <span data-ttu-id="89aa1-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-741">Il tipo di protocollo di autenticazione estendibile richiesto per l'autenticazione della connessione di accesso remoto non è installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="89aa1-741">The Extensible Authentication Protocol type required for authentication of the remote access connection is not installed on your computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <span data-ttu-id="89aa1-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-743">Il tipo di protocollo di autenticazione estendibile configurato nella connessione di accesso remoto non supporta Single Sign-On.</span><span class="sxs-lookup"><span data-stu-id="89aa1-743">The Extensible Authentication Protocol type configured on the remote access connection does not support single sign-on.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <span data-ttu-id="89aa1-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-745">Il tipo di protocollo di autenticazione estendibile configurato nella connessione di accesso remoto non supporta l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="89aa1-745">The Extensible Authentication Protocol type configured on the remote access connection does not support the requested operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <span data-ttu-id="89aa1-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-747">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato che autentica il client nel server non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-747">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid.</span></span> <span data-ttu-id="89aa1-748">Verificare che il certificato utilizzato per l'autenticazione sia valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-748">Ensure that the certificate used for authentication is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <span data-ttu-id="89aa1-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-750">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato che autentica il client sul server è scaduto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-750">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is expired.</span></span> <span data-ttu-id="89aa1-751">Rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-751">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <span data-ttu-id="89aa1-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-753">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato che autentica il client sul server viene revocato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-753">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is revoked.</span></span> <span data-ttu-id="89aa1-754">Usare un certificato che non è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-754">Use a certificate that has not been revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <span data-ttu-id="89aa1-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-756">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita a causa di un errore nel certificato che autentica il client nel server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-756">The remote access connection completed, but authentication failed because of an error in the certificate that authenticates the client to the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <span data-ttu-id="89aa1-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-758">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato usato dal client per autenticare il server non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-758">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <span data-ttu-id="89aa1-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-760">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato usato dal client per autenticare il server è scaduto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-760">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <span data-ttu-id="89aa1-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-762">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato usato dal client per autenticare il server è revocato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-762">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <span data-ttu-id="89aa1-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-764">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita a causa di un errore nel certificato utilizzato dal client per autenticare il server.</span><span class="sxs-lookup"><span data-stu-id="89aa1-764">The remote access connection completed, but authentication failed because of an error in the certificate that the client uses to authenticate the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <span data-ttu-id="89aa1-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-766">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché un certificato radice attendibile che convalida il certificato utente non è stato trovato nell'archivio certificati delle autorità di certificazione radice attendibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-766">The remote access connection completed, but authentication failed because a trusted root certificate that validates the user certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <span data-ttu-id="89aa1-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-768">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato radice attendibile usato per convalidare il certificato utente non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-768">The remote access connection completed, but authentication failed because the trusted root certificate that is used to validate the user certificate is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <span data-ttu-id="89aa1-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-770">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato nell'archivio certificati delle autorità di certificazione radice attendibili che autentica il certificato utente è scaduto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-770">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that authenticates the user certificate is expired.</span></span> <span data-ttu-id="89aa1-771">Rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-771">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <span data-ttu-id="89aa1-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-773">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché un certificato che convalida il certificato del server non è stato trovato nell'archivio certificati delle autorità di certificazione radice attendibili.</span><span class="sxs-lookup"><span data-stu-id="89aa1-773">The remote access connection completed, but authentication failed because a certificate that validates the server certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <span data-ttu-id="89aa1-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-775">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato nell'archivio certificati delle autorità di certificazione radice attendibili che convalida il certificato del server non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-775">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that validates the server certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <span data-ttu-id="89aa1-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-777">La connessione di accesso remoto è stata completata, ma l'autenticazione non è riuscita perché il certificato nel computer server non ha un nome di server specificato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-777">The remote access connection completed, but authentication failed because the certificate on the server computer does not have a server name specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <span data-ttu-id="89aa1-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-779">L'identità esterna PEAP non corrisponde all'identità interna quando la privacy delle identità è disattivata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-779">The PEAP outer identity is not same as the inner identity when identity privacy is turned OFF.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <span data-ttu-id="89aa1-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-781">La connessione remota non è stata eseguita perché il nome del server di accesso remoto non è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-781">The remote connection was not made because the name of the remote access server did not resolve.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <span data-ttu-id="89aa1-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-783">La password specificata per il certificato non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-783">The password provided for the certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <span data-ttu-id="89aa1-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-785">Non è stato possibile abilitare l'interfaccia perché è stata creata più di un'interfaccia con la stessa destinazione con il metodo di autenticazione della chiave già condivisa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-785">The interface could not be enabled because more than one interface with the same destination has been created with the pre-shared key authentication method.</span></span> <span data-ttu-id="89aa1-786">Modificare il metodo di destinazione/autenticazione e abilitare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="89aa1-786">Change the destination/auth method and enable the interface.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="89aa1-787">I codici di errore API RRAS (routing e accesso remoto) seguenti sono definiti in mprerror. h.</span><span class="sxs-lookup"><span data-stu-id="89aa1-787">The following Routing and Remote Access (RRAS) API error codes are defined in mprerror.h.</span></span> <span data-ttu-id="89aa1-788">Tutti i codici di errore sono supportati in Windows 2000 o versioni successive di Windows, a meno che non sia specificato diversamente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-788">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89aa1-789">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="89aa1-789">Return code/value</span></span></th>
<th><span data-ttu-id="89aa1-790">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89aa1-790">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <span data-ttu-id="89aa1-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-792">Il router non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-792">The router is not running.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <span data-ttu-id="89aa1-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-794">L'interfaccia è già connessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-794">The interface is already connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <span data-ttu-id="89aa1-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-796">L'identificatore di protocollo specificato non è noto al router.</span><span class="sxs-lookup"><span data-stu-id="89aa1-796">The specified protocol identifier is not known to the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <span data-ttu-id="89aa1-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-798">DDM (Demand-Dial Interface Manager) non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-798">The Demand-dial Interface Manager (DDM) is not running.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <span data-ttu-id="89aa1-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-800">Un'interfaccia con questo nome è già registrata con il router.</span><span class="sxs-lookup"><span data-stu-id="89aa1-800">An interface with this name is already registered with the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <span data-ttu-id="89aa1-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-802">Un'interfaccia con questo nome non è registrata con il router.</span><span class="sxs-lookup"><span data-stu-id="89aa1-802">An interface with this name is not registered with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <span data-ttu-id="89aa1-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-804">L'interfaccia non è connessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-804">The interface is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <span data-ttu-id="89aa1-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-806">Il protocollo specificato viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-806">The specified protocol is stopping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <span data-ttu-id="89aa1-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-808">L'interfaccia è connessa e pertanto non può essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="89aa1-808">The interface is connected and hence cannot be deleted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <span data-ttu-id="89aa1-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-810">Le credenziali dell'interfaccia non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-810">The interface credentials have not been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <span data-ttu-id="89aa1-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-812">Questa interfaccia è già in fase di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-812">This interface is already in the process of connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <span data-ttu-id="89aa1-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-814">È già in corso un aggiornamento delle informazioni di routing su questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="89aa1-814">An update of routing information on this interface is already in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <span data-ttu-id="89aa1-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-816">L'interfaccia configurazione non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-816">The interface configration is not valid.</span></span> <span data-ttu-id="89aa1-817">Esiste già un'altra interfaccia connessa alla stessa interfaccia sul router remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-817">There is already another interface that is connected to the same interface on the remote router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <span data-ttu-id="89aa1-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-819">Un client di accesso remoto ha tentato di connettersi tramite una porta riservata solo ai router.</span><span class="sxs-lookup"><span data-stu-id="89aa1-819">A Remote Access Client attempted to connect over a port that was reserved for routers only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <span data-ttu-id="89aa1-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-821">Un router di connessione a richiesta ha tentato di connettersi su una porta riservata solo ai client di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-821">A Demand Dial Router attempted to connect over a port that was reserved for Remote Access Clients only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <span data-ttu-id="89aa1-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-823">L'interfaccia client con questo nome esiste già ed è attualmente connessa.</span><span class="sxs-lookup"><span data-stu-id="89aa1-823">The client interface with this name already exists and is currently connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <span data-ttu-id="89aa1-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-825">L'interfaccia si trova in uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-825">The interface is in a disabled state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <span data-ttu-id="89aa1-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-827">Il protocollo di autenticazione è stato rifiutato dal peer remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-827">The authentication protocol was rejected by the remote peer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <span data-ttu-id="89aa1-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-829">Non sono disponibili protocolli di autenticazione per l'uso.</span><span class="sxs-lookup"><span data-stu-id="89aa1-829">There are no authentication protocols available for use.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <span data-ttu-id="89aa1-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-831">Impossibile stabilire la connessione. il protocollo di autenticazione utilizzato dal server RAS/VPN per verificare il nome utente e la password non è stato in grado di trovare la corrispondenza con le impostazioni nel profilo di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-831">The connection could not be established because the authentication protocol used by the RAS/VPN server to verify your username and password could not be matched with the settings in your connection profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <span data-ttu-id="89aa1-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-833">L'account remoto non dispone dell'autorizzazione di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-833">The remote account does not have Remote Access permission.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <span data-ttu-id="89aa1-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-835">L'account remoto è scaduto.</span><span class="sxs-lookup"><span data-stu-id="89aa1-835">The remote account has expired.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <span data-ttu-id="89aa1-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-837">L'account remoto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="89aa1-837">The remote account is disabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <span data-ttu-id="89aa1-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-839">L'account remoto non è autorizzato ad accedere a questa ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="89aa1-839">The remote account is not permitted to logon at this time of day.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <span data-ttu-id="89aa1-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-841">Accesso negato al peer remoto perché il nome utente, la password o entrambi non sono validi per il dominio.</span><span class="sxs-lookup"><span data-stu-id="89aa1-841">Access was denied to the remote peer because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <span data-ttu-id="89aa1-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-843">Non sono disponibili porte abilitate per il routing per l'uso da questa interfaccia della richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-843">There are no routing enabled ports available for use by this demand dial interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <span data-ttu-id="89aa1-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-845">La porta è stata disconnessa a causa di inattività.</span><span class="sxs-lookup"><span data-stu-id="89aa1-845">The port has been disconnected due to inactivity.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <span data-ttu-id="89aa1-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-847">L'interfaccia non è attualmente raggiungibile in questo momento.</span><span class="sxs-lookup"><span data-stu-id="89aa1-847">The interface is not reachable at this time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <span data-ttu-id="89aa1-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-849">Il servizio Demand Dial è in uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-849">The Demand Dial service is in a paused state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <span data-ttu-id="89aa1-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-851">L'interfaccia è stata disconnessa dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="89aa1-851">The interface has been disconnected by the administrator.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <span data-ttu-id="89aa1-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-853">Il server di autenticazione non ha risposto tempestivamente alle richieste di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-853">The authentication server did not respond to authentication requests in a timely fashion.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <span data-ttu-id="89aa1-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-855">È stato raggiunto il numero massimo di porte consentite per l'uso nella connessione a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="89aa1-855">The maximum number of ports allowed for use in the multi-linked connection has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <span data-ttu-id="89aa1-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-857">È stato raggiunto il limite di tempo di connessione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-857">The connection time limit for the user has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <span data-ttu-id="89aa1-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-859">È stato raggiunto il limite massimo per il numero di interfacce LAN supportate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-859">The maximum limit on the number of LAN interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <span data-ttu-id="89aa1-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-861">È stato raggiunto il limite massimo per il numero di interfacce di connessione a richiesta supportate.</span><span class="sxs-lookup"><span data-stu-id="89aa1-861">The maximum limit on the number of Demand Dial interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <span data-ttu-id="89aa1-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-863">È stato raggiunto il limite massimo per il numero di client di accesso remoto supportati.</span><span class="sxs-lookup"><span data-stu-id="89aa1-863">The maximum limit on the number of Remote Access Clients supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <span data-ttu-id="89aa1-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-865">La porta è stata disconnessa a causa del criterio BAP (Bandwidth Allocation Protocol).</span><span class="sxs-lookup"><span data-stu-id="89aa1-865">The port has been disconnected due to the Bandwidth Allocation Protocol (BAP) policy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <span data-ttu-id="89aa1-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-867">Poiché è in uso un'altra connessione del tipo, la connessione in ingresso non può accettare la richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-867">Because another connection of your type is in use, the incoming connection cannot accept your connection request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <span data-ttu-id="89aa1-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-869">Nessun server RADIUS presente nella rete.</span><span class="sxs-lookup"><span data-stu-id="89aa1-869">No RADIUS servers were located on the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <span data-ttu-id="89aa1-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-871">La risposta ricevuta dal server di autenticazione RADIUS non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-871">The response received from the RADIUS authentication server was not valid.</span></span> <span data-ttu-id="89aa1-872">Assicurarsi che la password del segreto con distinzione tra maiuscole e minuscole per il server RADIUS sia impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-872">Make sure that the case sensitive secret password for the RADIUS server is set correctly.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <span data-ttu-id="89aa1-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-874">Non si è autorizzati a connettersi in questo momento.</span><span class="sxs-lookup"><span data-stu-id="89aa1-874">You do not have permission to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <span data-ttu-id="89aa1-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-876">Non si è autorizzati a connettersi usando il tipo di dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-876">You do not have permission to connect using the current device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <span data-ttu-id="89aa1-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-878">Impossibile stabilire la connessione perché il metodo di autenticazione utilizzato dal profilo di connessione non è consentito per l'utilizzo da parte di criteri di accesso configurati nel server RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="89aa1-878">The connection could not be established because the authentication method used by your connection profile is not permitted for use by an access policy configured on the RAS/VPN server.</span></span> <span data-ttu-id="89aa1-879">In particolare, ciò può essere dovuto a differenze di configurazione tra il metodo di autenticazione selezionato nel server RAS/VPN e i criteri di accesso configurati.</span><span class="sxs-lookup"><span data-stu-id="89aa1-879">Specifically, this could be due to configuration differences between the authentication method selected on the RAS/VPN server and the access policy configured for it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <span data-ttu-id="89aa1-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-881">BAP è necessario per questo utente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-881">BAP is required for this user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <span data-ttu-id="89aa1-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-883">Al momento non è consentito connettersi all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="89aa1-883">The interface is not allowed to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <span data-ttu-id="89aa1-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-885">La configurazione del router salvato non è compatibile con il router corrente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-885">The saved router configuration is incompatible with the current router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <span data-ttu-id="89aa1-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-887">Accesso remoto ha rilevato gli account utente di formato precedenti che non verranno migrati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="89aa1-887">Remote Access has detected older format user accounts that will not be migrated automatically.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <span data-ttu-id="89aa1-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-889">Il trasporto è già installato con il router.</span><span class="sxs-lookup"><span data-stu-id="89aa1-889">The transport is already installed with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <span data-ttu-id="89aa1-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-891">La lunghezza della firma ricevuta in un pacchetto dal server RADIUS non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-891">The signature length received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-892">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-892">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <span data-ttu-id="89aa1-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-894">La firma ricevuta in un pacchetto dal server RADIUS non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-894">The signature received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-895">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-895">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <span data-ttu-id="89aa1-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-897">Non ha ricevuto la firma insieme a EAPMessage dal server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="89aa1-897">Did not receive signature along with EAPMessage from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-898">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-898">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <span data-ttu-id="89aa1-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-900">La lunghezza o l'ID ricevuto in un pacchetto dal server RADIUS non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-900">The length or Id received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-901">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-901">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <span data-ttu-id="89aa1-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-903">La lunghezza ricevuta in un pacchetto con attributo dal server RADIUS non è valida.</span><span class="sxs-lookup"><span data-stu-id="89aa1-903">The length received in a packet with attribute from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-904">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-904">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <span data-ttu-id="89aa1-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-906">Il pacchetto ricevuto dal server RADIUS non è valido.</span><span class="sxs-lookup"><span data-stu-id="89aa1-906">The packet received from RADIUS server in not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-907">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-907">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <span data-ttu-id="89aa1-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-909">L'autenticatore non corrisponde al pacchetto dal server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="89aa1-909">Authenticator does not match in packet from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-910">Supportato in Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-910">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <span data-ttu-id="89aa1-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span><span class="sxs-lookup"><span data-stu-id="89aa1-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span></span></dl></td>
<td><span data-ttu-id="89aa1-912">Il server di routing e accesso remoto non è configurato o non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="89aa1-912">Routing and Remote access server is either not configured or not running.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89aa1-913">Supportato in Windows 7 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="89aa1-913">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="89aa1-914">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89aa1-914">Requirements</span></span>



| <span data-ttu-id="89aa1-915">Requisito</span><span class="sxs-lookup"><span data-stu-id="89aa1-915">Requirement</span></span> | <span data-ttu-id="89aa1-916">Valore</span><span class="sxs-lookup"><span data-stu-id="89aa1-916">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="89aa1-917">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89aa1-917">Minimum supported client</span></span><br/> | <span data-ttu-id="89aa1-918">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89aa1-918">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89aa1-919">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89aa1-919">Minimum supported server</span></span><br/> | <span data-ttu-id="89aa1-920">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89aa1-920">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 





