---
description: La funzione PdhVbOpenLog apre il file di log specificato per la lettura e la scrittura. Questa funzione chiama PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529113"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="d7eb9-104">PdhVbOpenLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="d7eb9-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="d7eb9-105">La funzione **PdhVbOpenLog** apre il file di log specificato per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="d7eb9-106">Questa funzione chiama [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span><span class="sxs-lookup"><span data-stu-id="d7eb9-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7eb9-107">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="d7eb9-108">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d7eb9-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="d7eb9-109">Funzione PdhVbOpenLog ( \_ ByVal SzLogFileName As LPCTSTR, \_ ByVal DWACCESSFLAGS As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH \_ HQUERY, \_ ByVal DwMaxSize As DWORD, \_ ByVal SZUSERCAPTION As LPCSTR, \_ ByRef phLog As PDH \_ numero \_ ) As DWORD</span><span class="sxs-lookup"><span data-stu-id="d7eb9-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="d7eb9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7eb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7eb9-111">*szLogFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-112">Puntatore a una stringa che specifica il nome del file di log da aprire.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="d7eb9-113">Se il file di log contiene dati SQL, il formato del nome del file di log è **SQL:**_DataSourceName_*_!_* _LogFileName_.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="d7eb9-114">In questo caso, il valore del parametro *lpdwLogType* è PDH \_ log \_ Type \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="d7eb9-115">*dwAccessFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-116">Tipo di accesso da specificare quando viene aperto il file di log.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="d7eb9-117">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d7eb9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d7eb9-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="d7eb9-119">Significato</span><span class="sxs-lookup"><span data-stu-id="d7eb9-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="d7eb9-120"><dt>**\_accesso in \_ lettura \_ al log PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="d7eb9-121">Viene aperto un file di log per un'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="d7eb9-122"><dt>**\_accesso in \_ scrittura \_ log PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="d7eb9-123">Viene aperto un nuovo file di log per un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="d7eb9-124"><dt>**\_ \_ accesso aggiornamento log \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="d7eb9-125">Per un'operazione di scrittura viene aperto un file di log esistente.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="d7eb9-126">Il valore selezionato dalla tabella precedente può essere combinato usando l'operatore OR con uno dei seguenti flag di creazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="d7eb9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d7eb9-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="d7eb9-128">Significato</span><span class="sxs-lookup"><span data-stu-id="d7eb9-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="d7eb9-129"><dt>**\_creazione di \_ un \_ nuovo log PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="d7eb9-130">Viene creato un nuovo file di log con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="d7eb9-131"><dt>**PDH \_ log \_ Crea \_ sempre**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="d7eb9-132">Viene creato un nuovo file di log con il nome specificato e viene cancellato qualsiasi file di log esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="d7eb9-133"><dt>**\_Registro PDH \_ aperto \_ esistente**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="d7eb9-134">Viene aperto un file di log esistente con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="d7eb9-135">Se non esiste un file di log con il nome specificato, è uguale a PDH \_ log \_ Create \_ New.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="d7eb9-136"><dt>**PDH \_ log \_ aperto \_ sempre**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="d7eb9-137">Viene aperto un file di log esistente con il nome specificato oppure viene creato un nuovo file di log con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="d7eb9-138">*lpdwLogType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-139">Puntatore a una variabile che indica il tipo di file di log da aprire.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="d7eb9-140">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d7eb9-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d7eb9-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d7eb9-142">Significato</span><span class="sxs-lookup"><span data-stu-id="d7eb9-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="d7eb9-143"><dt>**tipo di log PDH non \_ \_ \_ definito**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="d7eb9-144">Formato del file di log non definito.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="d7eb9-145"><dt>**\_tipo di log PDH \_ \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="d7eb9-146">File di testo contenenti le intestazioni di colonna nella prima riga e singoli campioni di dati in ogni riga successiva.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="d7eb9-147"><dt>**\_tipo di log PDH \_ \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="d7eb9-148">I dati nel file di log sono in SQL.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="d7eb9-149"><dt>**\_tipo di log PDH \_ \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="d7eb9-150">Uguale al \_ tipo di log PDH \_ \_ CSV.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="d7eb9-151"><dt>**\_ \_ Binary tipo di log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="d7eb9-152">Formato binario del file di log.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-152">Binary log file format.</span></span> <span data-ttu-id="d7eb9-153">Include i file di log circolari.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="d7eb9-154"><dt>**\_tipo di log PDH \_ \_ PerfMon**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="d7eb9-155">Formato del file di log PerfMon.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="d7eb9-156">*hQuery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-157">Handle di query.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-157">Query handle.</span></span> <span data-ttu-id="d7eb9-158">Questo handle viene restituito dalla funzione [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="d7eb9-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="d7eb9-159">Questo parametro può essere **null** se il file di log deve essere aperto per la lettura.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="d7eb9-160">*dwMaxSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-161">Dimensioni massime del file di log in byte.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="d7eb9-162">Questo valore viene utilizzato solo se il file di log è un file di log di dimensioni limitate o circolari.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="d7eb9-163">*szUserCaption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-164">Puntatore a una stringa che specifica la didascalia definita dall'utente del file di log.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="d7eb9-165">Una didascalia del file di log descrive in genere il contenuto del file di log.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="d7eb9-166">Quando viene aperto un file di log esistente, il valore di questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d7eb9-167">*phLog* \[ in, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb9-168">Puntatore a un buffer che riceve un handle per il file di log aperto.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7eb9-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7eb9-169">Return value</span></span>

<span data-ttu-id="d7eb9-170">Se la funzione ha esito positivo, restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="d7eb9-171">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d7eb9-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="d7eb9-172">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-172">The following are possible values.</span></span>



| <span data-ttu-id="d7eb9-173">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d7eb9-173">Return code</span></span>                                                                                                | <span data-ttu-id="d7eb9-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7eb9-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7eb9-175"><dt>**\_buffer insufficiente PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="d7eb9-176">I dati richiesti sono maggiori del buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="d7eb9-177">Impossibile restituire i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="d7eb9-178"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="d7eb9-179">La dimensione di uno o più buffer di stringa non è corretta.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="d7eb9-180"><dt>**\_handle PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="d7eb9-181">L'handle non è un oggetto PDH valido.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="d7eb9-182"><dt>**\_errore di \_ apertura del file di registro PDH \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="d7eb9-183">Impossibile aprire il file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="d7eb9-184"><dt>**il \_ file PDH non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="d7eb9-185">Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d7eb9-186">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7eb9-186">Remarks</span></span>

<span data-ttu-id="d7eb9-187">Quando si utilizza questa funzione per scrivere i dati sulle prestazioni in un file di log, è necessario innanzitutto aprire una query utilizzando [**PdhVbOpenQuery**](pdhvbopenquery.md).</span><span class="sxs-lookup"><span data-stu-id="d7eb9-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="d7eb9-188">È necessario che sia presente una query attualmente aperta ed è necessario aggiungervi i contatori desiderati, prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="d7eb9-189">Si noti che i file di log nel formato Perfmon possono essere aperti solo per la lettura.</span><span class="sxs-lookup"><span data-stu-id="d7eb9-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7eb9-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7eb9-190">Requirements</span></span>



| <span data-ttu-id="d7eb9-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7eb9-191">Requirement</span></span> | <span data-ttu-id="d7eb9-192">Valore</span><span class="sxs-lookup"><span data-stu-id="d7eb9-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7eb9-193">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7eb9-193">Minimum supported client</span></span><br/> | <span data-ttu-id="d7eb9-194">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7eb9-195">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7eb9-195">Minimum supported server</span></span><br/> | <span data-ttu-id="d7eb9-196">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7eb9-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d7eb9-197">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7eb9-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7eb9-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7eb9-199">DLL</span><span class="sxs-lookup"><span data-stu-id="d7eb9-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7eb9-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb9-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7eb9-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7eb9-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7eb9-202">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="d7eb9-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="d7eb9-203">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="d7eb9-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="d7eb9-204">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="d7eb9-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

