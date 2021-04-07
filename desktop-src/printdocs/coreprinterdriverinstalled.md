---
description: La funzione CorePrinterDriverInstalled segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Funzione CorePrinterDriverInstalled (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057906"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="e6508-103">CorePrinterDriverInstalled (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6508-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="e6508-104">La funzione **CorePrinterDriverInstalled** segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.</span><span class="sxs-lookup"><span data-stu-id="e6508-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6508-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6508-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="e6508-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6508-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6508-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6508-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="e6508-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="e6508-109">Utilizzare **null** per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="e6508-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6508-110">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6508-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-111">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86.</span><span class="sxs-lookup"><span data-stu-id="e6508-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="e6508-112">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e6508-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6508-113">*CoreDriverGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6508-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-114">GUID del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="e6508-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="e6508-115">*ftDriverDate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6508-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-116">Data del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="e6508-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="e6508-117">*dwlDriverVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6508-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-118">Versione del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="e6508-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="e6508-119">*pbDriverInstalled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e6508-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6508-120">Puntatore a **true** se il driver, o una versione più recente, è installato; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="e6508-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6508-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6508-121">Return value</span></span>

<span data-ttu-id="e6508-122">Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="e6508-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="e6508-123">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="e6508-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6508-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6508-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6508-125">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e6508-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e6508-126">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6508-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e6508-127">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="e6508-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6508-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6508-128">Requirements</span></span>



| <span data-ttu-id="e6508-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6508-129">Requirement</span></span> | <span data-ttu-id="e6508-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e6508-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6508-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6508-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e6508-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6508-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e6508-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6508-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e6508-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6508-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6508-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6508-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6508-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6508-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e6508-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6508-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6508-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6508-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e6508-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e6508-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6508-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6508-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="e6508-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e6508-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e6508-142">**CorePrinterDriverInstalledW** (Unicode) e **CorePrinterDriverInstalledA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e6508-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e6508-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6508-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6508-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="e6508-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e6508-145">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e6508-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

