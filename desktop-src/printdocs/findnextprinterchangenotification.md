---
description: La funzione FindNextPrinterChangeNotification recupera le informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Funzione FindNextPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882825"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="cf69b-103">FindNextPrinterChangeNotification (funzione)</span><span class="sxs-lookup"><span data-stu-id="cf69b-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="cf69b-104">La funzione **FindNextPrinterChangeNotification** recupera le informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf69b-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="cf69b-105">Chiamare questa funzione quando viene soddisfatta un'operazione di attesa sull'oggetto notifica di modifica.</span><span class="sxs-lookup"><span data-stu-id="cf69b-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="cf69b-106">La funzione Reimposta anche l'oggetto notifica di modifica sullo stato non segnalato.</span><span class="sxs-lookup"><span data-stu-id="cf69b-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="cf69b-107">È quindi possibile usare l'oggetto in un'altra operazione di attesa per continuare a monitorare la stampante o il server di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf69b-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="cf69b-108">Il sistema operativo imposterà l'oggetto sullo stato segnalato la volta successiva in cui si verificherà un set di modifiche specificato per la stampante o il server di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf69b-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="cf69b-109">La funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea l'oggetto notifica di modifica e specifica il set di modifiche da monitorare.</span><span class="sxs-lookup"><span data-stu-id="cf69b-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf69b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf69b-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cf69b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf69b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf69b-112">*hChange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf69b-113">Handle per un oggetto notifica di modifica associato a una stampante o a un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf69b-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="cf69b-114">È possibile ottenere tale handle chiamando la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="cf69b-115">Il sistema operativo imposta questo oggetto notifica di modifica sullo stato segnalato quando rileva una delle modifiche specificate nel filtro delle notifiche di modifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cf69b-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="cf69b-116">*pdwChange* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf69b-117">Puntatore a una variabile i cui bit sono impostati per indicare le modifiche che hanno causato la notifica più recente.</span><span class="sxs-lookup"><span data-stu-id="cf69b-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="cf69b-118">I flag di bit che possono essere impostati corrispondono a quelli specificati nel parametro *fdwFilter* della chiamata [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="cf69b-119">Il sistema imposta uno o più dei seguenti flag di bit.</span><span class="sxs-lookup"><span data-stu-id="cf69b-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="cf69b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cf69b-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="cf69b-121">Significato</span><span class="sxs-lookup"><span data-stu-id="cf69b-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="cf69b-122"><dt>**\_modulo di \_ aggiunta della modifica della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="cf69b-123">Un modulo è stato aggiunto al server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="cf69b-124"><dt>**modifica della stampante \_ \_ Aggiungi \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="cf69b-125">Un processo di stampa è stato inviato alla stampante.</span><span class="sxs-lookup"><span data-stu-id="cf69b-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="cf69b-126"><dt>**modifica della stampante \_ \_ Aggiungi \_ porta**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="cf69b-127">Una porta o un monitoraggio è stato aggiunto al server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="cf69b-128"><dt>**\_modifica stampante \_ Aggiungi \_ processore di stampa \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="cf69b-129">Un processore di stampa è stato aggiunto al server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="cf69b-130"><dt>**\_modifica stampante \_ Aggiungi \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="cf69b-131">È stata aggiunta una stampante al server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="cf69b-132"><dt>**\_modifica stampante \_ Aggiungi \_ driver della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="cf69b-133">Un driver della stampante è stato aggiunto al server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="cf69b-134"><dt>**modifica della stampante \_ \_ configurare la \_ porta**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="cf69b-135">Una porta è stata configurata nel server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="cf69b-136"><dt>**\_modulo di \_ eliminazione della modifica della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="cf69b-137">Un modulo è stato eliminato dal server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="cf69b-138"><dt>**\_processo di \_ eliminazione della modifica della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="cf69b-139">Un processo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="cf69b-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="cf69b-140"><dt>**\_porta di \_ eliminazione delle modifiche della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="cf69b-141">Una porta o un monitoraggio è stato eliminato dal server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="cf69b-142"><dt>**\_modifica stampante \_ Elimina \_ processore di stampa \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="cf69b-143">Un processore di stampa è stato eliminato dal server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="cf69b-144"><dt>**\_modifica stampante \_ Elimina \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="cf69b-145">Una stampante è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="cf69b-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="cf69b-146"><dt>**modifica stampante- \_ \_ Elimina \_ driver della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="cf69b-147">Un driver della stampante è stato eliminato dal server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="cf69b-148"><dt>**\_modifica stampante \_ non \_ riuscita \_ stampante di connessione**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="cf69b-149">Errore di connessione alla stampante.</span><span class="sxs-lookup"><span data-stu-id="cf69b-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="cf69b-150"><dt>**\_modulo del \_ set di modifiche della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="cf69b-151">Un modulo è stato impostato sul server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="cf69b-152"><dt>**\_processo del \_ set di modifiche della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="cf69b-153">Un processo è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="cf69b-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="cf69b-154"><dt>**\_ \_ stampante set di modifiche stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="cf69b-155">È stata impostata una stampante.</span><span class="sxs-lookup"><span data-stu-id="cf69b-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="cf69b-156"><dt>**\_ \_ \_ driver della stampante del set di modifiche della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="cf69b-157">È stato impostato un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="cf69b-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="cf69b-158"><dt>**\_processo di \_ scrittura \_ modifica stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="cf69b-159">I dati del processo sono stati scritti.</span><span class="sxs-lookup"><span data-stu-id="cf69b-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="cf69b-160"><dt>**\_timeout modifica \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="cf69b-161">Timeout del processo.</span><span class="sxs-lookup"><span data-stu-id="cf69b-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="cf69b-162"><dt>**\_server di modifica della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="cf69b-163">Windows 7: è stata apportata una modifica nel server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="cf69b-164">*pPrinterNotifyOptions* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf69b-165">Puntatore a una struttura [**di \_ \_ Opzioni di notifica della stampante**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="cf69b-166">Impostare il membro **Flags** di questa struttura su **Printer \_ Notify \_ Options \_ Refresh** per fare in modo che la funzione restituisca i dati correnti per tutti i campi di informazioni sulla stampante monitorata.</span><span class="sxs-lookup"><span data-stu-id="cf69b-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="cf69b-167">La funzione ignora tutti gli altri membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="cf69b-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="cf69b-168">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cf69b-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cf69b-169">*ppPrinterNotifyInfo* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf69b-170">Puntatore a una variabile puntatore che riceve un puntatore a un buffer di sola lettura allocato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cf69b-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="cf69b-171">Chiamare la funzione [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) per liberare il buffer al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cf69b-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="cf69b-172">Questo parametro può essere **null** se non è richiesta alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="cf69b-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="cf69b-173">Il buffer contiene una struttura di [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , che contiene una matrice di strutture di [**\_ \_ \_ dati di notifica della stampante**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="cf69b-174">Ogni elemento della matrice contiene informazioni su uno dei campi specificati nel parametro *pPrinterNotifyOptions* della chiamata [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="cf69b-175">In genere, la funzione fornisce dati solo per i campi modificati in modo da generare la notifica più recente.</span><span class="sxs-lookup"><span data-stu-id="cf69b-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="cf69b-176">Tuttavia, se la struttura a cui punta il parametro *pPrinterNotifyOptions* specifica **l' \_ \_ \_ aggiornamento delle opzioni di notifica della stampante**, la funzione fornisce dati per tutti i campi monitorati.</span><span class="sxs-lookup"><span data-stu-id="cf69b-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="cf69b-177">Se il bit delle **\_ \_ informazioni \_ di notifica della stampante** è impostato nel membro **flag** della struttura delle [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , si è verificato un overflow o si è verificato un errore e le notifiche potrebbero andare perse.</span><span class="sxs-lookup"><span data-stu-id="cf69b-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="cf69b-178">In questo caso, non verranno inviate notifiche aggiuntive fino a quando non si effettua una seconda chiamata **FindNextPrinterChangeNotification** che specifica l' **aggiornamento delle \_ Opzioni di notifica \_ \_ della stampante**.</span><span class="sxs-lookup"><span data-stu-id="cf69b-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf69b-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf69b-179">Return value</span></span>

<span data-ttu-id="cf69b-180">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cf69b-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cf69b-181">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="cf69b-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf69b-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf69b-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf69b-183">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="cf69b-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cf69b-184">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf69b-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cf69b-185">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="cf69b-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cf69b-186">Chiamare la funzione **FindNextPrinterChangeNotification** dopo che un'operazione di attesa su un oggetto notifica creato da [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) è stata soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="cf69b-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="cf69b-187">La chiamata a **FindNextPrinterChangeNotification** consente di ottenere informazioni sulla modifica che ha soddisfatto l'operazione di attesa e di reimpostare l'oggetto notifica in modo che possa essere segnalato quando si verifica la modifica successiva.</span><span class="sxs-lookup"><span data-stu-id="cf69b-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="cf69b-188">Con un'eccezione, non chiamare la funzione **FindNextPrinterChangeNotification** se l'oggetto notifica di modifica non è nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="cf69b-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="cf69b-189">Se una funzione wait restituisce il **\_ timeout di attesa** del valore, l'oggetto Change non è nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="cf69b-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="cf69b-190">Chiamare la funzione **FindNextPrinterChangeNotification** solo se la funzione wait riesce senza scadere. L'eccezione si verifica quando viene chiamato **FindNextPrinterChangeNotification** con il bit di **aggiornamento delle \_ Opzioni di notifica \_ \_ della stampante** impostato nel parametro *pPrinterNotifyOptions* .</span><span class="sxs-lookup"><span data-stu-id="cf69b-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="cf69b-191">Si noti che anche quando questo flag è impostato, è comunque possibile che il flag per le **\_ \_ informazioni \_ di notifica della stampante** non sia impostato nel parametro *ppPrinterNotifyInfo* .</span><span class="sxs-lookup"><span data-stu-id="cf69b-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="cf69b-192">Per continuare a monitorare la stampante o il server di stampa per le modifiche, ripetere il ciclo di chiamata a una delle [funzioni di attesa](/windows/desktop/Sync/wait-functions) e quindi chiamare la funzione **FindNextPrinterChangeNotification** per esaminare la modifica e reimpostare l'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="cf69b-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="cf69b-193">**FindNextPrinterChangeNotification** può combinare più modifiche allo stesso campo di informazioni della stampante in una singola notifica.</span><span class="sxs-lookup"><span data-stu-id="cf69b-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="cf69b-194">Quando si verifica questa situazione, la funzione comprime in genere tutte le modifiche per il campo in una singola voce della matrice delle strutture di [**dati di \_ notifica delle \_ informazioni \_ di stampa**](printer-notify-info-data.md) in *ppPrinterNotifyInfo*. la singola voce riporta solo le informazioni più aggiornate.</span><span class="sxs-lookup"><span data-stu-id="cf69b-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="cf69b-195">Tuttavia, per alcuni campi di informazioni su processi e stampanti, la funzione può restituire più voci di matrice per lo stesso campo.</span><span class="sxs-lookup"><span data-stu-id="cf69b-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="cf69b-196">In questo caso, l'ultima voce di matrice per il campo indica i dati correnti e le voci precedenti contengono i dati per le fasi intermedie.</span><span class="sxs-lookup"><span data-stu-id="cf69b-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="cf69b-197">Quando l'oggetto notifica di modifica non è più necessario, chiuderlo chiamando la funzione [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="cf69b-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="cf69b-198">In Windows XP con Service Pack 2 (SP2) e versioni successive, il firewall connessione Internet (ICF) blocca le porte della stampante per impostazione predefinita, ma è possibile abilitare un'eccezione per la condivisione di file e stampanti.</span><span class="sxs-lookup"><span data-stu-id="cf69b-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="cf69b-199">Se un utente esegue una connessione alla stampante a un altro computer e l'eccezione non è abilitata, l'utente non riceverà le notifiche di modifica della stampante dal server.</span><span class="sxs-lookup"><span data-stu-id="cf69b-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="cf69b-200">Un amministratore del computer dovrà abilitare l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="cf69b-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cf69b-201">Esempio</span><span class="sxs-lookup"><span data-stu-id="cf69b-201">Examples</span></span>

<span data-ttu-id="cf69b-202">Nell'esempio di codice riportato di seguito viene illustrato come è possibile monitorare lo stato della stampante utilizzando queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="cf69b-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="cf69b-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf69b-203">Requirements</span></span>



| <span data-ttu-id="cf69b-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf69b-204">Requirement</span></span> | <span data-ttu-id="cf69b-205">Valore</span><span class="sxs-lookup"><span data-stu-id="cf69b-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf69b-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf69b-206">Minimum supported client</span></span><br/> | <span data-ttu-id="cf69b-207">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf69b-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf69b-208">Minimum supported server</span></span><br/> | <span data-ttu-id="cf69b-209">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf69b-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf69b-210">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf69b-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf69b-211"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cf69b-212">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf69b-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf69b-213"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cf69b-214">DLL</span><span class="sxs-lookup"><span data-stu-id="cf69b-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf69b-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf69b-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cf69b-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf69b-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf69b-217">Stampa</span><span class="sxs-lookup"><span data-stu-id="cf69b-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cf69b-218">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="cf69b-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cf69b-219">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="cf69b-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="cf69b-220">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="cf69b-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="cf69b-221">**\_informazioni notifica \_ stampante**</span><span class="sxs-lookup"><span data-stu-id="cf69b-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="cf69b-222">**\_dati delle \_ informazioni di notifica della stampante \_**</span><span class="sxs-lookup"><span data-stu-id="cf69b-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="cf69b-223">**\_Opzioni di notifica stampanti \_**</span><span class="sxs-lookup"><span data-stu-id="cf69b-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

