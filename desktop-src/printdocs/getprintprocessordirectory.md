---
description: La funzione GetPrintProcessorDirectory Recupera il percorso della directory del processore di stampa nel server specificato.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Funzione GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885181"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="6c4cd-103">GetPrintProcessorDirectory (funzione)</span><span class="sxs-lookup"><span data-stu-id="6c4cd-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="6c4cd-104">La funzione **GetPrintProcessorDirectory** Recupera il percorso della directory del processore di stampa nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c4cd-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="6c4cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c4cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4cd-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-108">Puntatore a una stringa con terminazione null che specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="6c4cd-109">Se questo parametro è **null**, viene restituito un percorso locale.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="6c4cd-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-111">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="6c4cd-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="6c4cd-112">Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="6c4cd-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-114">Livello della struttura.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-114">The structure level.</span></span> <span data-ttu-id="6c4cd-115">Questo valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="6c4cd-116">*pPrintProcessorInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-117">Puntatore a un buffer che riceve il percorso.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="6c4cd-118">Si noti che, per i sistemi operativi precedenti a Windows Server 2003 SP 1, il percorso è nel formato locale per il server, non nel formato remoto vero e proprio.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="6c4cd-119">Ad esempio, il percorso viene specificato come "% windir% \\ system32 \\ spool \\ prtprocs \\ % Environment%" invece di " \\ \\ servername \\ Print $ \\ prtprocs \\ % Environment%", anche quando viene chiamato per un server remoto.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="6c4cd-120">Per i sistemi operativi Windows Server 2003 SP 1 e versioni successive, viene restituito il vero percorso remoto.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="6c4cd-121">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-122">Dimensioni del buffer a cui punta *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="6c4cd-123">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4cd-124">Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4cd-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c4cd-125">Return value</span></span>

<span data-ttu-id="6c4cd-126">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6c4cd-127">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c4cd-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c4cd-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c4cd-129">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6c4cd-130">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6c4cd-131">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="6c4cd-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c4cd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c4cd-132">Requirements</span></span>



| <span data-ttu-id="6c4cd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4cd-133">Requirement</span></span> | <span data-ttu-id="6c4cd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6c4cd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4cd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c4cd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4cd-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c4cd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c4cd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4cd-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c4cd-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c4cd-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c4cd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c4cd-140"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4cd-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6c4cd-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c4cd-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c4cd-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c4cd-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6c4cd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6c4cd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c4cd-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6c4cd-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6c4cd-145">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6c4cd-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c4cd-146">**GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c4cd-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="6c4cd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c4cd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4cd-148">Stampa</span><span class="sxs-lookup"><span data-stu-id="6c4cd-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6c4cd-149">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="6c4cd-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6c4cd-150">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="6c4cd-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




