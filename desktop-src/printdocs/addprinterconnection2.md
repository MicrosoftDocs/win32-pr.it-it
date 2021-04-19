---
description: Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Funzione AddPrinterConnection2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311566"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="7ea8c-103">AddPrinterConnection2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ea8c-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="7ea8c-104">Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea8c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ea8c-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ea8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ea8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea8c-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ea8c-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea8c-108">Handle per la finestra padre in cui verrà visualizzata la finestra di dialogo se il sistema di stampa deve scaricare un driver della stampante dal server di stampa per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8c-109">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ea8c-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea8c-110">Puntatore a una stringa costante con terminazione null che specifica il nome della stampante a cui l'utente corrente desidera connettersi.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8c-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="7ea8c-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea8c-112">Versione della struttura a cui punta *pConnectionInfo*.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="7ea8c-113">Attualmente, viene definito solo il livello 1, pertanto il valore di *dwLevel* deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8c-114">*pConnectionInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ea8c-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea8c-115">Puntatore a una struttura [**di \_ informazioni di connessione della stampante \_ \_ 1**](printer-connection-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea8c-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="7ea8c-116">Per ulteriori informazioni su questo parametro, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea8c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ea8c-117">Return value</span></span>

<span data-ttu-id="7ea8c-118">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7ea8c-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="7ea8c-120">Per informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea8c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ea8c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ea8c-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7ea8c-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7ea8c-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="7ea8c-125">Quando Windows Vista effettua una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante dal server a cui è collegata la stampante.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="7ea8c-126">Se l'utente non dispone delle autorizzazioni per copiare i file nel percorso appropriato, la funzione **AddPrinterConnection2** ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="7ea8c-127">Se i file del driver della stampante devono essere copiati dal server di stampa ma non possono essere copiati in modo invisibile a causa dei criteri di gruppo in vigore e \_ la connessione alla stampante \_ non \_ è impostata alcuna interfaccia utente in *pConnectionInfo->dwFlags*, non verrà visualizzata alcuna finestra di dialogo e la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="7ea8c-128">Se il driver della stampante locale può essere utilizzato per eseguire il rendering dei processi di stampa per questa stampante e la versione del driver locale non deve corrispondere alla versione del driver della stampante nel server, impostare la \_ mancata corrispondenza della connessione della stampante \_ in *PConnectionInfo->dwFlags* e assegnare il puntatore a una variabile di stringa che contiene il percorso del driver della stampante locale a *pConnectionInfo->pszDriverName*.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="7ea8c-129">Una connessione stampante stabilita chiamando **AddPrinterConnection2** verrà enumerata quando viene chiamato [**EnumPrinters**](enumprinters.md) con *dwType* impostato su Printer \_ enum \_ Connection.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="7ea8c-130">La versione ANSI di questa funzione, **AddPrinterConnection2A**, non è supportata e restituisce l' **errore \_ non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea8c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ea8c-131">Requirements</span></span>



| <span data-ttu-id="7ea8c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ea8c-132">Requirement</span></span> | <span data-ttu-id="7ea8c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7ea8c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea8c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ea8c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea8c-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ea8c-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7ea8c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ea8c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea8c-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ea8c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ea8c-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ea8c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ea8c-139"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ea8c-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7ea8c-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ea8c-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ea8c-141"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ea8c-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7ea8c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ea8c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ea8c-143"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7ea8c-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7ea8c-144">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7ea8c-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ea8c-145">**AddPrinterConnection2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="7ea8c-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="7ea8c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ea8c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea8c-147">Stampa</span><span class="sxs-lookup"><span data-stu-id="7ea8c-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7ea8c-148">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7ea8c-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7ea8c-149">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="7ea8c-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="7ea8c-150">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="7ea8c-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="7ea8c-151">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="7ea8c-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

