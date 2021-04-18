---
description: La funzione seprinter imposta i dati per una stampante specificata o imposta lo stato della stampante specificata sospendendo la stampa, riprendendo la stampa o cancellando tutti i processi di stampa.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Funzione seprinter (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314977"
---
# <a name="setprinter-function"></a><span data-ttu-id="3e520-103">Funzione seprinter</span><span class="sxs-lookup"><span data-stu-id="3e520-103">SetPrinter function</span></span>

<span data-ttu-id="3e520-104">La funzione **Seprinter** imposta i dati per una stampante specificata o imposta lo stato della stampante specificata sospendendo la stampa, riprendendo la stampa o cancellando tutti i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="3e520-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e520-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e520-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="3e520-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e520-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e520-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e520-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e520-108">Handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-108">A handle to the printer.</span></span> <span data-ttu-id="3e520-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3e520-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3e520-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e520-111">Tipo di dati che la funzione archivia nel buffer a cui punta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="3e520-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="3e520-112">Se il parametro del *comando* non è uguale a zero, il parametro del *livello* deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e520-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="3e520-113">Questo valore può essere 0, 2, 3, 4, 5, 6, 7, 8 o 9.</span><span class="sxs-lookup"><span data-stu-id="3e520-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="3e520-114">*pPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e520-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e520-115">Puntatore a un buffer contenente i dati da impostare per la stampante o che contengono informazioni per il comando specificato dal parametro *Command* .</span><span class="sxs-lookup"><span data-stu-id="3e520-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="3e520-116">Il tipo di dati nel buffer è determinato dal valore di *Level*.</span><span class="sxs-lookup"><span data-stu-id="3e520-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="3e520-117">Level</span><span class="sxs-lookup"><span data-stu-id="3e520-117">Level</span></span>                                                                                                | <span data-ttu-id="3e520-118">Struttura</span><span class="sxs-lookup"><span data-stu-id="3e520-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3e520-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3e520-120">Se il parametro *Command* è **\_ \_ \_ Status set di controllo Printer**, *pPrinter* deve contenere un valore **DWORD** che specifica il nuovo stato della stampante da impostare.</span><span class="sxs-lookup"><span data-stu-id="3e520-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="3e520-121">Per un elenco dei valori di stato possibili, vedere il membro **status** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="3e520-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="3e520-122">Si noti che **lo stato della stampante è \_ \_ sospeso** e **\_ lo stato della stampante \_ \_ eliminazione in sospeso** non sono valori di stato validi da impostare.</span><span class="sxs-lookup"><span data-stu-id="3e520-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="3e520-123">Se *Level* è 0, ma il parametro *Command* non è **\_ \_ impostato \_ sullo stato del controllo Printer**, *pPrinter* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3e520-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="3e520-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3e520-125">Struttura [**di \_ info \_ 2 della stampante**](printer-info-2.md) che contiene informazioni dettagliate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="3e520-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3e520-127">Struttura [**di \_ informazioni \_ sulla stampante 3**](printer-info-3.md) contenente le informazioni di sicurezza della stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="3e520-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3e520-129">Struttura [**di \_ informazioni \_ di stampa 4**](printer-info-4.md) contenente informazioni minime sulla stampante, tra cui il nome della stampante, il nome del server e l'eventuale presenza di una stampante remota o locale.</span><span class="sxs-lookup"><span data-stu-id="3e520-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="3e520-130"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="3e520-131">Struttura [**di \_ informazioni \_ sulla stampante 5**](printer-info-5.md) che contiene informazioni sulla stampante, ad esempio attributi della stampante e impostazioni di timeout.</span><span class="sxs-lookup"><span data-stu-id="3e520-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="3e520-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="3e520-133">Struttura della [**stampante \_ info \_ 6**](printer-info-6.md) che specifica il valore di stato di una stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="3e520-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="3e520-135">Struttura [**di \_ info \_ 7 della stampante**](printer-info-7.md) .</span><span class="sxs-lookup"><span data-stu-id="3e520-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="3e520-136">Il membro *dwAction* di questa struttura **indica se il** selettore deve pubblicare, annullare la pubblicazione, pubblicare di nuovo o aggiornare i dati della stampante nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="3e520-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="3e520-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="3e520-138">Una struttura di [**\_ Info stampa \_ 8**](printer-info-8.md) che specifica le impostazioni della stampante predefinite globali.</span><span class="sxs-lookup"><span data-stu-id="3e520-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="3e520-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="3e520-140">Struttura [**Printer \_ info \_ 9**](printer-info-9.md) che specifica le impostazioni della stampante predefinite per utente.</span><span class="sxs-lookup"><span data-stu-id="3e520-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="3e520-141">*Comando* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e520-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e520-142">l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3e520-142">The action to perform.</span></span>

<span data-ttu-id="3e520-143">Se il parametro *Level* è diverso da zero, impostare il valore di questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="3e520-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="3e520-144">In questo caso, la stampante mantiene lo stato corrente e la funzione riconfigura i dati della stampante come specificato dai parametri *Level* e *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="3e520-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="3e520-145">Se il parametro *Level* è zero, impostare il valore di questo parametro su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e520-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="3e520-146">Valore</span><span class="sxs-lookup"><span data-stu-id="3e520-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="3e520-147">Significato</span><span class="sxs-lookup"><span data-stu-id="3e520-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="3e520-148"><dt>**\_sospensione controllo \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="3e520-149">Sospendere la stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="3e520-150"><dt>**\_ripulitura controllo stampanti \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="3e520-151">Elimina tutti i processi di stampa nella stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="3e520-152"><dt>**\_ripresa del controllo della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="3e520-153">Riprendere una stampante sospesa.</span><span class="sxs-lookup"><span data-stu-id="3e520-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="3e520-154"><dt>**\_stato del \_ set di controlli della stampante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="3e520-155">Impostare lo stato della stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-155">Set the printer status.</span></span><br/> <span data-ttu-id="3e520-156">Impostare il parametro *pPrinter* su un puntatore a un valore **DWORD** che specifica il nuovo stato della stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e520-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e520-157">Return value</span></span>

<span data-ttu-id="3e520-158">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3e520-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3e520-159">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3e520-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="3e520-160">Se il *livello* è 7 e l'azione di pubblicazione non è riuscita, **viene restituito l'** errore i/o in **\_ \_ sospeso** e i tentativi di completare l'azione in background.</span><span class="sxs-lookup"><span data-stu-id="3e520-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="3e520-161">Se il *livello* è 7 e l'azione di aggiornamento non è riuscita, il **seprinter** restituisce il **file di errore \_ \_ non \_ trovato**.</span><span class="sxs-lookup"><span data-stu-id="3e520-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e520-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e520-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e520-163">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3e520-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3e520-164">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e520-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3e520-165">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="3e520-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3e520-166">Non è possibile utilizzare l'utilità di **stampa** per modificare la stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="3e520-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="3e520-167">Per modificare le impostazioni della stampante correnti, chiamare la funzione [**GetPrinter**](getprinter.md) per recuperare le impostazioni correnti in una struttura [**Printer \_ info \_ 2**](printer-info-2.md) , modificare i membri della struttura in modo che siano necessari, quindi chiamare **seprinter**.</span><span class="sxs-lookup"><span data-stu-id="3e520-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="3e520-168">La funzione **Seprinter** ignora i membri **pServerName**, **AveragePPM**, **status** e **cJobs** di una struttura [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="3e520-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="3e520-169">Con la sospensione di una stampante viene sospesa la pianificazione di tutti i processi di stampa per tale stampante, ad eccezione di un processo di stampa che può essere attualmente stampato.</span><span class="sxs-lookup"><span data-stu-id="3e520-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="3e520-170">I processi di stampa possono essere inviati a una stampante sospesa, ma non verrà pianificato alcun processo di stampa su tale stampante fino a quando la stampa non viene ripresa.</span><span class="sxs-lookup"><span data-stu-id="3e520-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="3e520-171">Se una stampante viene deselezionata, tutti i processi di stampa per tale stampante vengono eliminati, ad eccezione del processo di stampa corrente.</span><span class="sxs-lookup"><span data-stu-id="3e520-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="3e520-172">Se si utilizza **Seprinter** per modificare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predefinita per una stampante (impostando globalmente le impostazioni predefinite della stampante), è necessario chiamare prima la funzione [**DocumentProperties**](documentproperties.md) per convalidare la struttura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="3e520-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="3e520-173">Per le strutture [**Printer \_ info \_ 2**](printer-info-2.md) e [**Printer \_ info \_ 3**](printer-info-3.md) contenenti un puntatore a un descrittore di sicurezza, la funzione può impostare solo i componenti del descrittore di sicurezza che il chiamante dispone delle autorizzazioni per la modifica.</span><span class="sxs-lookup"><span data-stu-id="3e520-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="3e520-174">Per impostare particolari componenti del descrittore di sicurezza, è necessario specificare i diritti di accesso necessari quando si chiama la funzione [**OpenPrinter**](openprinter.md) o [**OpenPrinter2**](openprinter2.md) per recuperare un handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="3e520-175">La tabella seguente illustra i diritti di accesso necessari per modificare i vari componenti del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3e520-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="3e520-176">Autorizzazione di accesso</span><span class="sxs-lookup"><span data-stu-id="3e520-176">Access permission</span></span>            | <span data-ttu-id="3e520-177">Componente del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3e520-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="3e520-178">**Scrivi \_ proprietario**</span><span class="sxs-lookup"><span data-stu-id="3e520-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="3e520-179">Proprietario</span><span class="sxs-lookup"><span data-stu-id="3e520-179">Owner</span></span><br/> <span data-ttu-id="3e520-180">Gruppo primario</span><span class="sxs-lookup"><span data-stu-id="3e520-180">Primary group</span></span><br/> |
| <span data-ttu-id="3e520-181">**Scrivi \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="3e520-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="3e520-182">Elenco di controllo di accesso discrezionale (DACL)</span><span class="sxs-lookup"><span data-stu-id="3e520-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="3e520-183">**ACCESSO \_ alla \_ sicurezza del sistema**</span><span class="sxs-lookup"><span data-stu-id="3e520-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="3e520-184">Elenco di controllo di accesso di sistema (SACL)</span><span class="sxs-lookup"><span data-stu-id="3e520-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="3e520-185">Se il descrittore di sicurezza contiene un componente per il quale il chiamante non dispone del diritto di accesso da modificare, il **Seprinter** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e520-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="3e520-186">I componenti di un descrittore di sicurezza che non si desidera modificare devono essere **null** o non essere presenti, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="3e520-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="3e520-187">Se non si desidera modificare il descrittore di sicurezza e si chiama l'oggetto di **stampa** con una struttura di [**\_ info \_ 2 della stampante**](printer-info-2.md) , impostare il membro **pSecurityDescriptor** della struttura su **null**.</span><span class="sxs-lookup"><span data-stu-id="3e520-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="3e520-188">Per impostazione predefinita, il firewall connessione Internet (ICF) blocca le porte della stampante, ma è possibile abilitare un'eccezione per la condivisione di file e stampanti.</span><span class="sxs-lookup"><span data-stu-id="3e520-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="3e520-189">Se il **Seprinter** viene chiamato da un amministratore del computer, l'eccezione viene abilitata.</span><span class="sxs-lookup"><span data-stu-id="3e520-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="3e520-190">Se viene chiamato da un non amministratore e l'eccezione non è già stata abilitata, la chiamata ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e520-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="3e520-191">È possibile utilizzare il livello 7 con la struttura [**Printer \_ info \_ 7**](printer-info-7.md) per pubblicare, annullare la pubblicazione o aggiornare i dati del servizio directory per la stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="3e520-192">I dati del servizio directory per una stampante includono tutti i dati archiviati con le \_ \* chiavi di SPLDS tramite chiamate alla funzione [**SetPrinterDataEx**](setprinterdataex.md) per la stampante.</span><span class="sxs-lookup"><span data-stu-id="3e520-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="3e520-193">Prima di chiamare l'agente di **stampa**, impostare il membro **pszObjectGUID** di **Printer \_ info \_ 7** su **null** e impostare il membro *dwAction* su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e520-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="3e520-194">Valore</span><span class="sxs-lookup"><span data-stu-id="3e520-194">Value</span></span>                             | <span data-ttu-id="3e520-195">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e520-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e520-196">**\_pubblicazione DSPRINT**</span><span class="sxs-lookup"><span data-stu-id="3e520-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="3e520-197">Pubblica i dati del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="3e520-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3e520-198">**\_ripubblicazione DSPRINT**</span><span class="sxs-lookup"><span data-stu-id="3e520-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="3e520-199">I dati del servizio directory per la stampante non vengono pubblicati e quindi pubblicati nuovamente, aggiornando tutte le proprietà della stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="3e520-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="3e520-200">La ripubblicazione modifica anche il GUID della stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="3e520-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="3e520-201">Utilizzare questo valore se si ritiene che i dati pubblicati della stampante siano danneggiati.</span><span class="sxs-lookup"><span data-stu-id="3e520-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="3e520-202">**DSPRINT \_ annullare la pubblicazione**</span><span class="sxs-lookup"><span data-stu-id="3e520-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="3e520-203">Annulla la pubblicazione dei dati del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="3e520-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e520-204">**aggiornamento di DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="3e520-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="3e520-205">Aggiorna i dati del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="3e520-205">Updates the directory service data.</span></span> <span data-ttu-id="3e520-206">Questa operazione è identica a quella di **DSPRINT \_ Publish**, **con la differenza che il** file di errore non viene trovato se la stampante non è già **\_ \_ \_ stata** pubblicata.</span><span class="sxs-lookup"><span data-stu-id="3e520-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="3e520-207">Usare **l' \_ aggiornamento di DSPRINT** per aggiornare le proprietà pubblicate ma non forzare la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="3e520-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="3e520-208">I driver della stampante devono sempre usare l' **\_ aggiornamento DSPRINT** anziché **DSPRINT \_ Publish**.</span><span class="sxs-lookup"><span data-stu-id="3e520-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="3e520-209">**DSPRINT \_ PENDING** non è un valore *dwAction* valido per **seprinter**.</span><span class="sxs-lookup"><span data-stu-id="3e520-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e520-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e520-210">Requirements</span></span>



| <span data-ttu-id="3e520-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e520-211">Requirement</span></span> | <span data-ttu-id="3e520-212">Valore</span><span class="sxs-lookup"><span data-stu-id="3e520-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e520-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e520-213">Minimum supported client</span></span><br/> | <span data-ttu-id="3e520-214">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e520-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3e520-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e520-215">Minimum supported server</span></span><br/> | <span data-ttu-id="3e520-216">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e520-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3e520-217">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e520-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e520-218"><dt>WinSpool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3e520-219">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e520-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e520-220"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3e520-221">DLL</span><span class="sxs-lookup"><span data-stu-id="3e520-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e520-222"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3e520-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3e520-223">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3e520-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3e520-224">**SetPrinterW** (Unicode) e **seprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3e520-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="3e520-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e520-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e520-226">Stampa</span><span class="sxs-lookup"><span data-stu-id="3e520-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3e520-227">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="3e520-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3e520-228">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e520-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="3e520-229">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e520-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="3e520-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e520-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3e520-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="3e520-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="3e520-232">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3e520-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="3e520-233">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="3e520-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="3e520-234">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="3e520-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="3e520-235">**\_Informazioni stampante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="3e520-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="3e520-236">**\_Informazioni stampante \_ 6**</span><span class="sxs-lookup"><span data-stu-id="3e520-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="3e520-237">**Informazioni sulla stampante \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="3e520-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="3e520-238">**\_Informazioni stampante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="3e520-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="3e520-239">**Informazioni sulla stampante \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="3e520-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="3e520-240">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3e520-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




