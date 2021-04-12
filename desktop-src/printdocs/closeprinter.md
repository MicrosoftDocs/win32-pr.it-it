---
description: La funzione ClosePrinter chiude l'oggetto stampante specificato.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Funzione ClosePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233613"
---
# <a name="closeprinter-function"></a><span data-ttu-id="a56ff-103">ClosePrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="a56ff-103">ClosePrinter function</span></span>

<span data-ttu-id="a56ff-104">La funzione **ClosePrinter** chiude l'oggetto stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="a56ff-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a56ff-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="a56ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a56ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56ff-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a56ff-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a56ff-108">Handle per l'oggetto stampante da chiudere.</span><span class="sxs-lookup"><span data-stu-id="a56ff-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="a56ff-109">Questo handle viene restituito dalla funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="a56ff-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56ff-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a56ff-110">Return value</span></span>

<span data-ttu-id="a56ff-111">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a56ff-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a56ff-112">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="a56ff-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56ff-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a56ff-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a56ff-114">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="a56ff-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a56ff-115">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a56ff-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a56ff-116">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="a56ff-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a56ff-117">Quando la funzione **ClosePrinter** restituisce, l'handle *hPrinter* non è valido, indipendentemente dal fatto che la funzione abbia avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a56ff-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="a56ff-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="a56ff-118">Examples</span></span>

<span data-ttu-id="a56ff-119">Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="a56ff-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a56ff-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a56ff-120">Requirements</span></span>



| <span data-ttu-id="a56ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56ff-121">Requirement</span></span> | <span data-ttu-id="a56ff-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a56ff-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56ff-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a56ff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a56ff-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a56ff-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a56ff-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a56ff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a56ff-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a56ff-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a56ff-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a56ff-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a56ff-128"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a56ff-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a56ff-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a56ff-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a56ff-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a56ff-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a56ff-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a56ff-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a56ff-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a56ff-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a56ff-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a56ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56ff-134">Stampa</span><span class="sxs-lookup"><span data-stu-id="a56ff-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a56ff-135">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="a56ff-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a56ff-136">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="a56ff-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="a56ff-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a56ff-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




