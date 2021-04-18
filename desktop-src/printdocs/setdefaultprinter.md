---
description: La funzione SetDefaultPrinter imposta il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Funzione SetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314980"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="d8761-103">SetDefaultPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="d8761-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="d8761-104">La funzione **SetDefaultPrinter** imposta il nome della stampante predefinita per l'utente corrente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d8761-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8761-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8761-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="d8761-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8761-107">*pszPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8761-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8761-108">Puntatore a una stringa con terminazione null che contiene il nome predefinito della stampante.</span><span class="sxs-lookup"><span data-stu-id="d8761-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="d8761-109">Per una connessione a una stampante remota, il formato del nome è **\\\\** _Server_ *_\\_* _PrinterName_.</span><span class="sxs-lookup"><span data-stu-id="d8761-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="d8761-110">Per una stampante locale, il formato del nome è *PrinterName*.</span><span class="sxs-lookup"><span data-stu-id="d8761-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="d8761-111">Se questo parametro è **null** o una stringa vuota, ovvero "", **SetDefaultPrinter** selezionerà una stampante predefinita da una delle stampanti installate.</span><span class="sxs-lookup"><span data-stu-id="d8761-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="d8761-112">Se è già presente una stampante predefinita, la chiamata a **SetDefaultPrinter** con una stringa **null** o vuota in questo parametro potrebbe modificare la stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="d8761-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8761-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8761-113">Return value</span></span>

<span data-ttu-id="d8761-114">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d8761-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d8761-115">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="d8761-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8761-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8761-116">Remarks</span></span>

<span data-ttu-id="d8761-117">Quando si utilizza questo metodo, è necessario specificare una stampante, un driver e una porta validi.</span><span class="sxs-lookup"><span data-stu-id="d8761-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="d8761-118">Se non sono validi, le API non hanno esito negativo, ma il risultato non è definito.</span><span class="sxs-lookup"><span data-stu-id="d8761-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="d8761-119">Questo potrebbe causare la reimpostazione della stampante da parte di altri programmi sulla stampante valida precedente.</span><span class="sxs-lookup"><span data-stu-id="d8761-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="d8761-120">È possibile utilizzare [**EnumPrinters**](enumprinters.md) per recuperare il nome della stampante, il nome del driver e il nome della porta di tutte le stampanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="d8761-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="d8761-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="d8761-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d8761-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8761-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d8761-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="d8761-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8761-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8761-124">Requirements</span></span>



| <span data-ttu-id="d8761-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8761-125">Requirement</span></span> | <span data-ttu-id="d8761-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d8761-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8761-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8761-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d8761-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8761-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8761-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8761-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d8761-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8761-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8761-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8761-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8761-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8761-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d8761-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8761-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8761-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8761-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d8761-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d8761-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8761-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d8761-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d8761-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d8761-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d8761-138">**SetDefaultPrinterW** (Unicode) e **SetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d8761-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="d8761-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8761-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8761-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="d8761-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d8761-141">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="d8761-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d8761-142">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="d8761-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="d8761-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="d8761-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




