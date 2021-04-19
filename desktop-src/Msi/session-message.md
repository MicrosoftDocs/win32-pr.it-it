---
description: Il Metodo Message dell'oggetto Session esegue tutte le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore. La registrazione può essere abilitata selettivamente per i vari tipi di messaggio. Vedere il metodo EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333051"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="0baa2-105">Session. Message, metodo</span><span class="sxs-lookup"><span data-stu-id="0baa2-105">Session.Message method</span></span>

<span data-ttu-id="0baa2-106">Il metodo **Message** dell'oggetto [**Session**](session-object.md) esegue tutte le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore.</span><span class="sxs-lookup"><span data-stu-id="0baa2-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="0baa2-107">La registrazione può essere abilitata selettivamente per i vari tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0baa2-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="0baa2-108">Vedere il metodo [**EnableLog**](installer-enablelog.md) .</span><span class="sxs-lookup"><span data-stu-id="0baa2-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="0baa2-109">Se il campo record 0 contiene una stringa di formattazione, viene usato per formattare i dati negli altri campi.</span><span class="sxs-lookup"><span data-stu-id="0baa2-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="0baa2-110">In caso contrario, se il messaggio è un errore, un avviso o un messaggio utente, viene effettuato un tentativo di trovare un modello di messaggio nella tabella degli errori per il database corrente utilizzando il numero di errore trovato nel campo 1 del record per i tipi di messaggio e i valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="0baa2-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0baa2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0baa2-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="0baa2-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0baa2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0baa2-113">*tipo*</span><span class="sxs-lookup"><span data-stu-id="0baa2-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="0baa2-114">Il parametro *Kind* è obbligatorio per uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0baa2-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="0baa2-115">Per visualizzare una finestra di messaggio con pulsanti e icone di push, calcolare il valore di *Kind* aggiungendo gli stili standard della finestra di messaggio utilizzati da [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) e [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiMessageTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="0baa2-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="0baa2-116">Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="0baa2-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="0baa2-117">Costante</span><span class="sxs-lookup"><span data-stu-id="0baa2-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0baa2-118">Significato</span><span class="sxs-lookup"><span data-stu-id="0baa2-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="0baa2-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="0baa2-120">Terminazione prematura, probabilmente insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0baa2-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="0baa2-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="0baa2-122">Messaggio di errore formattato, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="0baa2-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="0baa2-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="0baa2-124">Messaggio di avviso formattato, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="0baa2-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="0baa2-125"><dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="0baa2-126">Messaggio di richiesta dell'utente, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="0baa2-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="0baa2-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="0baa2-128">Messaggio informativo per il log, che non deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="0baa2-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="0baa2-130">Elenco di file in uso che devono essere sostituiti.</span><span class="sxs-lookup"><span data-stu-id="0baa2-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="0baa2-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="0baa2-132">Richiesta per determinare un percorso di origine valido.</span><span class="sxs-lookup"><span data-stu-id="0baa2-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="0baa2-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="0baa2-134">Messaggio di spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0baa2-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="0baa2-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="0baa2-136">Inizio dell'azione, \[ 1 \] nome azione, \[ 2 \] Descrizione, \[ 3 \] modello per i messaggi ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="0baa2-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="0baa2-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="0baa2-138">Dati dell'azione.</span><span class="sxs-lookup"><span data-stu-id="0baa2-138">Action data.</span></span> <span data-ttu-id="0baa2-139">I campi dei record corrispondono al modello del messaggio ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="0baa2-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="0baa2-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="0baa2-141">Informazioni sull'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-141">Progress bar information.</span></span> <span data-ttu-id="0baa2-142">Vedere la descrizione dei campi di record riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="0baa2-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="0baa2-143"><dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="0baa2-144">Per abilitare il pulsante Annulla \[ , impostare 1 \] su 2 e \[ 2 \] su 1.</span><span class="sxs-lookup"><span data-stu-id="0baa2-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="0baa2-145">Per disabilitare il pulsante Annulla \[ , impostare 1 \] su 2 e \[ 2 \] su 0</span><span class="sxs-lookup"><span data-stu-id="0baa2-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0baa2-146">*record*</span><span class="sxs-lookup"><span data-stu-id="0baa2-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="0baa2-147">Oggetto [**record**](record-object.md) obbligatorio contenente un campo specifico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0baa2-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0baa2-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0baa2-148">Return value</span></span>



| <span data-ttu-id="0baa2-149">Costante</span><span class="sxs-lookup"><span data-stu-id="0baa2-149">Constant</span></span>                                                                                              | <span data-ttu-id="0baa2-150">Valore</span><span class="sxs-lookup"><span data-stu-id="0baa2-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="0baa2-151"><dt>**msiMessageStatusError**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="0baa2-152">-1</span><span class="sxs-lookup"><span data-stu-id="0baa2-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="0baa2-153"><dt>**msiMessageStatusNone**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="0baa2-154">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-155"><dt>**msiMessageStatusOk**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="0baa2-156">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-157"><dt>**msiMessageStatusCancel**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="0baa2-158">2</span><span class="sxs-lookup"><span data-stu-id="0baa2-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-159"><dt>**msiMessageStatusAbort**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="0baa2-160">3</span><span class="sxs-lookup"><span data-stu-id="0baa2-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-161"><dt>**msiMessageStatusRetry**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="0baa2-162">4</span><span class="sxs-lookup"><span data-stu-id="0baa2-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-163"><dt>**msiMessageStatusIgnore**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="0baa2-164">5</span><span class="sxs-lookup"><span data-stu-id="0baa2-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-165"><dt>**msiMessageStatusYes**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="0baa2-166">6</span><span class="sxs-lookup"><span data-stu-id="0baa2-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="0baa2-167"><dt>**msiMessageStatusNo**</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="0baa2-168">7</span><span class="sxs-lookup"><span data-stu-id="0baa2-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="0baa2-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="0baa2-169">Remarks</span></span>

<span data-ttu-id="0baa2-170">**Campi di record del messaggio**</span><span class="sxs-lookup"><span data-stu-id="0baa2-170">**Message Record Fields**</span></span>

<span data-ttu-id="0baa2-171">Di seguito vengono descritte le definizioni dei campi di record quando msiMessageTypeProgress viene passato come tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0baa2-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="0baa2-172">Field 1 specifica il tipo del messaggio di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="0baa2-173">Il significato degli altri campi dipende dal valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="0baa2-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="0baa2-174">I valori possibili che è possibile impostare nel campo 1 sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="0baa2-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="0baa2-175">Nome messaggio</span><span class="sxs-lookup"><span data-stu-id="0baa2-175">Message name</span></span>     | <span data-ttu-id="0baa2-176">Valore</span><span class="sxs-lookup"><span data-stu-id="0baa2-176">Value</span></span> | <span data-ttu-id="0baa2-177">Descrizione campo 1</span><span class="sxs-lookup"><span data-stu-id="0baa2-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baa2-178">MasterReset</span><span class="sxs-lookup"><span data-stu-id="0baa2-178">MasterReset</span></span>      | <span data-ttu-id="0baa2-179">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-179">0</span></span>     | <span data-ttu-id="0baa2-180">Reimposta l'indicatore di stato e imposta il numero totale previsto di cicli sulla barra.</span><span class="sxs-lookup"><span data-stu-id="0baa2-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="0baa2-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="0baa2-181">ActionInfo</span></span>       | <span data-ttu-id="0baa2-182">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-182">1</span></span>     | <span data-ttu-id="0baa2-183">Fornisce informazioni correlate ai messaggi di stato che devono essere inviati dall'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="0baa2-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="0baa2-184">ProgressReport</span><span class="sxs-lookup"><span data-stu-id="0baa2-184">ProgressReport</span></span>   | <span data-ttu-id="0baa2-185">2</span><span class="sxs-lookup"><span data-stu-id="0baa2-185">2</span></span>     | <span data-ttu-id="0baa2-186">Incrementa l'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="0baa2-187">ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="0baa2-187">ProgressAddition</span></span> | <span data-ttu-id="0baa2-188">3</span><span class="sxs-lookup"><span data-stu-id="0baa2-188">3</span></span>     | <span data-ttu-id="0baa2-189">Abilita un'azione (ad esempio CustomAction) per aggiungere i segni di avanzamento al numero totale previsto di stato dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="0baa2-190">Il significato del campo 2 dipende dal valore nel campo 1, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0baa2-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="0baa2-191">Valore campo 1</span><span class="sxs-lookup"><span data-stu-id="0baa2-191">Field 1 value</span></span> | <span data-ttu-id="0baa2-192">Descrizione campo 2</span><span class="sxs-lookup"><span data-stu-id="0baa2-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baa2-193">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-193">0</span></span>             | <span data-ttu-id="0baa2-194">Previsto numero totale di cicli nell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="0baa2-195">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-195">1</span></span>             | <span data-ttu-id="0baa2-196">Numero di cicli di selezione dell'indicatore di stato per ogni messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="0baa2-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="0baa2-197">Questo campo viene ignorato se il campo 3 è 0.</span><span class="sxs-lookup"><span data-stu-id="0baa2-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="0baa2-198">2</span><span class="sxs-lookup"><span data-stu-id="0baa2-198">2</span></span>             | <span data-ttu-id="0baa2-199">Numero di cicli spostati nell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="0baa2-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="0baa2-200">3</span><span class="sxs-lookup"><span data-stu-id="0baa2-200">3</span></span>             | <span data-ttu-id="0baa2-201">Numero di cicli da aggiungere allo stato di avanzamento previsto totale.</span><span class="sxs-lookup"><span data-stu-id="0baa2-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="0baa2-202">Il significato del campo 3 dipende dal valore nel campo 1, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0baa2-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="0baa2-203">Valore campo 1</span><span class="sxs-lookup"><span data-stu-id="0baa2-203">Field 1 value</span></span> | <span data-ttu-id="0baa2-204">Valore campo 3</span><span class="sxs-lookup"><span data-stu-id="0baa2-204">Field 3 value</span></span> | <span data-ttu-id="0baa2-205">Descrizione campo 3</span><span class="sxs-lookup"><span data-stu-id="0baa2-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baa2-206">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-206">0</span></span>             | <span data-ttu-id="0baa2-207">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-207">0</span></span>             | <span data-ttu-id="0baa2-208">Indicatore di stato avanti (da sinistra a destra)</span><span class="sxs-lookup"><span data-stu-id="0baa2-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="0baa2-209">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-209">1</span></span>             | <span data-ttu-id="0baa2-210">Barra di avanzamento indietro (da destra a sinistra)</span><span class="sxs-lookup"><span data-stu-id="0baa2-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="0baa2-211">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-211">1</span></span>             | <span data-ttu-id="0baa2-212">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-212">0</span></span>             | <span data-ttu-id="0baa2-213">L'azione corrente invierà messaggi ProgressReport espliciti.</span><span class="sxs-lookup"><span data-stu-id="0baa2-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="0baa2-214">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-214">1</span></span>             | <span data-ttu-id="0baa2-215">Incrementare l'indicatore di stato in base al numero di cicli specificati nel campo 2 ogni volta che viene inviato un messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="0baa2-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="0baa2-216">2</span><span class="sxs-lookup"><span data-stu-id="0baa2-216">2</span></span>             | <span data-ttu-id="0baa2-217">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="0baa2-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="0baa2-218">3</span><span class="sxs-lookup"><span data-stu-id="0baa2-218">3</span></span>             | <span data-ttu-id="0baa2-219">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="0baa2-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="0baa2-220">Il significato del campo 4 dipende dal valore nel campo 1, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0baa2-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="0baa2-221">Valore campo 1</span><span class="sxs-lookup"><span data-stu-id="0baa2-221">Field 1 value</span></span> | <span data-ttu-id="0baa2-222">Valore campo 4</span><span class="sxs-lookup"><span data-stu-id="0baa2-222">Field 4 value</span></span> | <span data-ttu-id="0baa2-223">Descrizione campo 4</span><span class="sxs-lookup"><span data-stu-id="0baa2-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baa2-224">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-224">0</span></span>             | <span data-ttu-id="0baa2-225">0</span><span class="sxs-lookup"><span data-stu-id="0baa2-225">0</span></span>             | <span data-ttu-id="0baa2-226">Esecuzione in corso.</span><span class="sxs-lookup"><span data-stu-id="0baa2-226">Execution is in progress.</span></span> <span data-ttu-id="0baa2-227">In questo caso, l'interfaccia utente potrebbe calcolare e visualizzare il tempo rimanente.</span><span class="sxs-lookup"><span data-stu-id="0baa2-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="0baa2-228">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-228">1</span></span>             | <span data-ttu-id="0baa2-229">Creazione dello script di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0baa2-229">Creating the execution script.</span></span> <span data-ttu-id="0baa2-230">In questo caso, l'interfaccia utente potrebbe visualizzare un messaggio per attendere il completamento della preparazione dell'installazione da parte del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="0baa2-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="0baa2-231">1</span><span class="sxs-lookup"><span data-stu-id="0baa2-231">1</span></span>             | <span data-ttu-id="0baa2-232">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="0baa2-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="0baa2-233">2</span><span class="sxs-lookup"><span data-stu-id="0baa2-233">2</span></span>             | <span data-ttu-id="0baa2-234">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="0baa2-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="0baa2-235">3</span><span class="sxs-lookup"><span data-stu-id="0baa2-235">3</span></span>             | <span data-ttu-id="0baa2-236">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="0baa2-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="0baa2-237">**Visualizzazione di finestre di messaggio**</span><span class="sxs-lookup"><span data-stu-id="0baa2-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="0baa2-238">Per visualizzare una finestra di messaggio con pulsanti e icone di push, calcolare il valore di *Kind* aggiungendo gli stili standard della finestra di messaggio utilizzati da **MessageBox** e **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="0baa2-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="0baa2-239">Le opzioni disponibili per i pulsanti di push per VBScript sono vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ AbortRetryIgnore (), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ YesNo) e vbRetryCancel (MB \_ RETRYCANCEL).</span><span class="sxs-lookup"><span data-stu-id="0baa2-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="0baa2-240">Le opzioni delle icone disponibili per VBScript sono vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) e vbInformation (MB \_ ICONINFORMATION).</span><span class="sxs-lookup"><span data-stu-id="0baa2-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="0baa2-241">Ad esempio, la chiamata seguente invia un messaggio **msiMessageTypeError** con l'icona vbExclamation e i pulsanti vbYesNo.</span><span class="sxs-lookup"><span data-stu-id="0baa2-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="0baa2-242">Se un'azione personalizzata chiama il metodo del **messaggio** , l'azione personalizzata deve essere in grado di gestire un annullamento da parte dell'utente e deve restituire **msiDoActionStatusUserExit**.</span><span class="sxs-lookup"><span data-stu-id="0baa2-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0baa2-243">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0baa2-243">Requirements</span></span>



| <span data-ttu-id="0baa2-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="0baa2-244">Requirement</span></span> | <span data-ttu-id="0baa2-245">Valore</span><span class="sxs-lookup"><span data-stu-id="0baa2-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baa2-246">Versione</span><span class="sxs-lookup"><span data-stu-id="0baa2-246">Version</span></span><br/> | <span data-ttu-id="0baa2-247">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0baa2-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0baa2-248">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0baa2-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0baa2-249">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0baa2-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0baa2-250">DLL</span><span class="sxs-lookup"><span data-stu-id="0baa2-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="0baa2-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0baa2-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0baa2-252">IID</span><span class="sxs-lookup"><span data-stu-id="0baa2-252">IID</span></span><br/>     | <span data-ttu-id="0baa2-253">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0baa2-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
