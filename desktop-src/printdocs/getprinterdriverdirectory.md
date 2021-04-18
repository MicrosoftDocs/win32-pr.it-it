---
description: La funzione GetPrinterDriverDirectory Recupera il percorso della directory del driver della stampante.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Funzione GetPrinterDriverDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318381"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="d98ec-103">GetPrinterDriverDirectory (funzione)</span><span class="sxs-lookup"><span data-stu-id="d98ec-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="d98ec-104">La funzione **GetPrinterDriverDirectory** Recupera il percorso della directory del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="d98ec-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d98ec-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="d98ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d98ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98ec-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui si trova il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="d98ec-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="d98ec-109">Se questo parametro è **null**, viene recuperato il percorso della directory del driver locale.</span><span class="sxs-lookup"><span data-stu-id="d98ec-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="d98ec-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-111">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="d98ec-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="d98ec-112">Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="d98ec-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ec-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-114">Livello della struttura.</span><span class="sxs-lookup"><span data-stu-id="d98ec-114">The structure level.</span></span> <span data-ttu-id="d98ec-115">Questo valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="d98ec-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="d98ec-116">*pDriverDirectory* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-117">Puntatore a un buffer che riceve il percorso.</span><span class="sxs-lookup"><span data-stu-id="d98ec-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="d98ec-118">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-119">Dimensione del buffer a cui punta *pDriverDirectory* .</span><span class="sxs-lookup"><span data-stu-id="d98ec-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="d98ec-120">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d98ec-121">Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="d98ec-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98ec-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d98ec-122">Return value</span></span>

<span data-ttu-id="d98ec-123">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d98ec-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d98ec-124">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="d98ec-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98ec-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d98ec-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d98ec-126">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="d98ec-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d98ec-127">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d98ec-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d98ec-128">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="d98ec-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d98ec-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d98ec-129">Requirements</span></span>



| <span data-ttu-id="d98ec-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98ec-130">Requirement</span></span> | <span data-ttu-id="d98ec-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d98ec-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98ec-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98ec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d98ec-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d98ec-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98ec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d98ec-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d98ec-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d98ec-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d98ec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d98ec-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d98ec-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d98ec-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="d98ec-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="d98ec-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d98ec-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d98ec-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d98ec-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d98ec-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d98ec-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d98ec-142">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d98ec-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d98ec-143">**GetPrinterDriverDirectoryW** (Unicode) e **GetPrinterDriverDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d98ec-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d98ec-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d98ec-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98ec-145">Stampa</span><span class="sxs-lookup"><span data-stu-id="d98ec-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d98ec-146">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="d98ec-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d98ec-147">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="d98ec-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




