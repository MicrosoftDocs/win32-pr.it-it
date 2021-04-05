---
description: La funzione AddPrinterConnection aggiunge una connessione alla stampante specificata per l'utente corrente.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Funzione AddPrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883209"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="dcdc0-103">AddPrinterConnection (funzione)</span><span class="sxs-lookup"><span data-stu-id="dcdc0-103">AddPrinterConnection function</span></span>

<span data-ttu-id="dcdc0-104">La funzione **AddPrinterConnection** aggiunge una connessione alla stampante specificata per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdc0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcdc0-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="dcdc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcdc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcdc0-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcdc0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcdc0-108">Puntatore a una stringa con terminazione null che specifica il nome di una stampante a cui l'utente corrente desidera stabilire una connessione.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcdc0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcdc0-109">Return value</span></span>

<span data-ttu-id="dcdc0-110">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dcdc0-111">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcdc0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcdc0-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dcdc0-113">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dcdc0-114">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dcdc0-115">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="dcdc0-116">Quando Windows crea una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante nel server a cui è collegata la stampante.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="dcdc0-117">Se l'utente non dispone delle autorizzazioni per copiare i file nel percorso appropriato, la funzione **AddPrinterConnection** ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="dcdc0-118">Una connessione stampante stabilita chiamando **AddPrinterConnection** verrà enumerata quando viene chiamato [**EnumPrinters**](enumprinters.md) con *dwType* impostato su Printer \_ enum \_ Connection.</span><span class="sxs-lookup"><span data-stu-id="dcdc0-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcdc0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcdc0-119">Requirements</span></span>



| <span data-ttu-id="dcdc0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcdc0-120">Requirement</span></span> | <span data-ttu-id="dcdc0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dcdc0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdc0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcdc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dcdc0-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcdc0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dcdc0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcdc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dcdc0-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcdc0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dcdc0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcdc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcdc0-127"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcdc0-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dcdc0-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcdc0-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcdc0-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcdc0-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dcdc0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dcdc0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcdc0-131"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="dcdc0-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="dcdc0-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dcdc0-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dcdc0-133">**AddPrinterConnectionW** (Unicode) e **AddPrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dcdc0-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="dcdc0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcdc0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdc0-135">Stampa</span><span class="sxs-lookup"><span data-stu-id="dcdc0-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dcdc0-136">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="dcdc0-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dcdc0-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="dcdc0-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="dcdc0-138">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="dcdc0-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="dcdc0-139">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="dcdc0-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

