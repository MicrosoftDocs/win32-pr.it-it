---
description: La funzione DeleteForm rimuove un nome di modulo dall'elenco dei form supportati.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Funzione DeleteForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050004"
---
# <a name="deleteform-function"></a><span data-ttu-id="e2f95-103">DeleteForm (funzione)</span><span class="sxs-lookup"><span data-stu-id="e2f95-103">DeleteForm function</span></span>

<span data-ttu-id="e2f95-104">La funzione **DeleteForm** rimuove un nome di modulo dall'elenco dei form supportati.</span><span class="sxs-lookup"><span data-stu-id="e2f95-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2f95-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="e2f95-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f95-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f95-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f95-108">Indica l'handle della stampante aperta su cui deve essere eseguita questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e2f95-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="e2f95-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="e2f95-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-110">*pFormName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f95-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f95-111">Puntatore al nome del form da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e2f95-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f95-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2f95-112">Return value</span></span>

<span data-ttu-id="e2f95-113">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e2f95-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e2f95-114">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="e2f95-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f95-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2f95-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2f95-116">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e2f95-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e2f95-117">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2f95-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e2f95-118">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="e2f95-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e2f95-119">**DeleteForm** può eliminare solo i nomi di modulo aggiunti tramite la funzione [**AddForm**](addform.md) .</span><span class="sxs-lookup"><span data-stu-id="e2f95-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f95-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2f95-120">Requirements</span></span>



| <span data-ttu-id="e2f95-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f95-121">Requirement</span></span> | <span data-ttu-id="e2f95-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e2f95-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f95-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2f95-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f95-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2f95-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2f95-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2f95-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f95-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2f95-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2f95-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2f95-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f95-128"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f95-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e2f95-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2f95-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2f95-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2f95-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e2f95-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f95-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f95-132"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e2f95-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e2f95-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e2f95-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e2f95-134">**DeleteFormW** (Unicode) e **DeleteFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e2f95-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="e2f95-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2f95-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f95-136">Stampa</span><span class="sxs-lookup"><span data-stu-id="e2f95-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e2f95-137">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e2f95-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e2f95-138">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="e2f95-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="e2f95-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e2f95-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




