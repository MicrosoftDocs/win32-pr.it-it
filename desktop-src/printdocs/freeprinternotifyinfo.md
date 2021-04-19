---
description: La funzione FreePrinterNotifyInfo libera un buffer allocato dal sistema creato dalla funzione FindNextPrinterChangeNotification.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Funzione FreePrinterNotifyInfo (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311824"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="72ba5-103">FreePrinterNotifyInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="72ba5-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="72ba5-104">La funzione **FreePrinterNotifyInfo** libera un buffer allocato dal sistema creato dalla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="72ba5-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ba5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72ba5-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="72ba5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72ba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ba5-107">*pPrinterNotifyInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72ba5-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ba5-108">Puntatore a un buffer di [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) restituito da una chiamata alla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="72ba5-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="72ba5-109">**FreePrinterNotifyInfo** dealloca il buffer.</span><span class="sxs-lookup"><span data-stu-id="72ba5-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ba5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72ba5-110">Return value</span></span>

<span data-ttu-id="72ba5-111">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="72ba5-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="72ba5-112">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="72ba5-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="72ba5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="72ba5-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72ba5-114">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="72ba5-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="72ba5-115">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72ba5-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="72ba5-116">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="72ba5-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72ba5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72ba5-117">Requirements</span></span>



| <span data-ttu-id="72ba5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ba5-118">Requirement</span></span> | <span data-ttu-id="72ba5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="72ba5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ba5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72ba5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72ba5-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="72ba5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="72ba5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72ba5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72ba5-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="72ba5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="72ba5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72ba5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72ba5-125"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72ba5-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="72ba5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="72ba5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="72ba5-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72ba5-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="72ba5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="72ba5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72ba5-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72ba5-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="72ba5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72ba5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ba5-131">Stampa</span><span class="sxs-lookup"><span data-stu-id="72ba5-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="72ba5-132">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="72ba5-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="72ba5-133">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="72ba5-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="72ba5-134">**\_informazioni notifica \_ stampante**</span><span class="sxs-lookup"><span data-stu-id="72ba5-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




