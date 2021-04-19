---
description: La funzione AddPrintProcessor installa un processore di stampa sul server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Funzione AddPrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317299"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="cd635-103">AddPrintProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd635-103">AddPrintProcessor function</span></span>

<span data-ttu-id="cd635-104">La funzione **AddPrintProcessor** installa un processore di stampa sul server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.</span><span class="sxs-lookup"><span data-stu-id="cd635-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd635-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd635-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="cd635-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd635-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd635-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd635-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="cd635-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="cd635-109">Se questo parametro è **null**, il processore di stampa viene installato localmente.</span><span class="sxs-lookup"><span data-stu-id="cd635-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="cd635-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd635-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd635-111">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="cd635-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="cd635-112">Se questo parametro è **null**, viene utilizzato l'ambiente corrente del chiamante/client (non di destinazione/Server).</span><span class="sxs-lookup"><span data-stu-id="cd635-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="cd635-113">*pPathName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd635-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd635-114">Puntatore a una stringa con terminazione null che specifica il nome del file che contiene il processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="cd635-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="cd635-115">Questo file deve trovarsi nella directory di sistema del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="cd635-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="cd635-116">*pPrintProcessorName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd635-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd635-117">Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="cd635-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd635-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd635-118">Return value</span></span>

<span data-ttu-id="cd635-119">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cd635-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cd635-120">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="cd635-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd635-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd635-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cd635-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="cd635-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cd635-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd635-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cd635-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="cd635-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cd635-125">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="cd635-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="cd635-126">Prima di chiamare la funzione **AddPrintProcessor** , un'applicazione deve verificare che il file contenente il processore di stampa sia archiviato nella directory del processore di stampa di sistema.</span><span class="sxs-lookup"><span data-stu-id="cd635-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="cd635-127">Un'applicazione può recuperare il nome della directory del processore di stampa di sistema chiamando la funzione [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="cd635-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="cd635-128">Un'applicazione può determinare il nome dei processori di stampa esistenti chiamando la funzione [**EnumPrintProcessors**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="cd635-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd635-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd635-129">Requirements</span></span>



| <span data-ttu-id="cd635-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd635-130">Requirement</span></span> | <span data-ttu-id="cd635-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cd635-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd635-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd635-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cd635-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd635-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd635-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd635-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cd635-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd635-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd635-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd635-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd635-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd635-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cd635-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd635-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd635-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd635-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cd635-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cd635-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd635-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cd635-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cd635-142">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cd635-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cd635-143">**AddPrintProcessorW** (Unicode) e **AddPrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cd635-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="cd635-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd635-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd635-145">Stampa</span><span class="sxs-lookup"><span data-stu-id="cd635-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cd635-146">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="cd635-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cd635-147">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="cd635-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="cd635-148">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="cd635-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

