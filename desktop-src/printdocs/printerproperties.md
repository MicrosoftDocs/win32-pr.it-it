---
description: La funzione PrinterProperties Visualizza una finestra delle proprietà Printer-Properties per la stampante specificata.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Funzione PrinterProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334303"
---
# <a name="printerproperties-function"></a><span data-ttu-id="c2216-103">PrinterProperties (funzione)</span><span class="sxs-lookup"><span data-stu-id="c2216-103">PrinterProperties function</span></span>

<span data-ttu-id="c2216-104">La funzione **PrinterProperties** Visualizza una finestra delle proprietà Printer-Properties per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="c2216-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2216-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2216-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="c2216-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2216-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2216-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2216-108">Handle per la finestra padre della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2216-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="c2216-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2216-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2216-110">Handle per un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="c2216-110">A handle to a printer object.</span></span> <span data-ttu-id="c2216-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="c2216-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2216-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2216-112">Return value</span></span>

<span data-ttu-id="c2216-113">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c2216-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c2216-114">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c2216-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2216-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2216-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2216-116">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c2216-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c2216-117">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2216-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c2216-118">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="c2216-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2216-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2216-119">Requirements</span></span>



| <span data-ttu-id="c2216-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2216-120">Requirement</span></span> | <span data-ttu-id="c2216-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c2216-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2216-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2216-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2216-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2216-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2216-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2216-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2216-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2216-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2216-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2216-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2216-127"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2216-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2216-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2216-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2216-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2216-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c2216-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c2216-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2216-131"><dt>winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c2216-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2216-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2216-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2216-133">Stampa</span><span class="sxs-lookup"><span data-stu-id="c2216-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c2216-134">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="c2216-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c2216-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="c2216-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="c2216-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c2216-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




