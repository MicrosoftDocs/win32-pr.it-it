---
description: La funzione FindClosePrinterChangeNotification chiude un oggetto notifica di modifica creato chiamando la funzione FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Funzione FindClosePrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049970"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="8b3e2-103">FindClosePrinterChangeNotification (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b3e2-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="8b3e2-104">La funzione **FindClosePrinterChangeNotification** chiude un oggetto notifica di modifica creato chiamando la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="8b3e2-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="8b3e2-105">La stampante o il server di stampa associato all'oggetto notifica delle modifiche non verrà più monitorato da tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3e2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b3e2-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="8b3e2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b3e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3e2-108">*hChange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b3e2-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3e2-109">Handle per l'oggetto notifica di modifica da chiudere.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="8b3e2-110">Si tratta di un handle creato chiamando la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="8b3e2-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b3e2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b3e2-111">Return value</span></span>

<span data-ttu-id="8b3e2-112">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8b3e2-113">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b3e2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b3e2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b3e2-115">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8b3e2-116">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8b3e2-117">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="8b3e2-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8b3e2-118">Dopo aver chiamato la funzione **FindClosePrinterChangeNotification** , non è possibile usare l'handle *hChange* nelle chiamate successive a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) o [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="8b3e2-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3e2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b3e2-119">Requirements</span></span>



| <span data-ttu-id="8b3e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b3e2-120">Requirement</span></span> | <span data-ttu-id="8b3e2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8b3e2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3e2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b3e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b3e2-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8b3e2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b3e2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b3e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b3e2-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8b3e2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b3e2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b3e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b3e2-127"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b3e2-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8b3e2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b3e2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b3e2-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b3e2-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8b3e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8b3e2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b3e2-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b3e2-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8b3e2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b3e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3e2-133">Stampa</span><span class="sxs-lookup"><span data-stu-id="8b3e2-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8b3e2-134">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="8b3e2-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8b3e2-135">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="8b3e2-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="8b3e2-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="8b3e2-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




