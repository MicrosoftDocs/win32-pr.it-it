---
description: Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Funzione GetCorePrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345286"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="28e7d-103">GetCorePrinterDrivers (funzione)</span><span class="sxs-lookup"><span data-stu-id="28e7d-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="28e7d-104">Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="28e7d-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28e7d-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="28e7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28e7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e7d-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e7d-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="28e7d-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="28e7d-109">Utilizzare **null** per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="28e7d-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="28e7d-110">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e7d-111">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86.</span><span class="sxs-lookup"><span data-stu-id="28e7d-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="28e7d-112">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="28e7d-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="28e7d-113">*pszzCoreDriverDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e7d-114">Puntatore a una stringa multistringa con terminazione null che specifica i GUID dei driver della stampante di base.</span><span class="sxs-lookup"><span data-stu-id="28e7d-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="28e7d-115">*cCorePrinterDrivers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e7d-116">Numero di stringhe in *pszzCoreDriverDependencies*.</span><span class="sxs-lookup"><span data-stu-id="28e7d-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="28e7d-117">*pCorePrinterDrivers* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28e7d-118">Puntatore a una matrice di una o più strutture [**di \_ \_ driver della stampante di base**](core-printer-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="28e7d-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e7d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28e7d-119">Return value</span></span>

<span data-ttu-id="28e7d-120">Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="28e7d-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="28e7d-121">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="28e7d-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28e7d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="28e7d-122">Remarks</span></span>

<span data-ttu-id="28e7d-123">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="28e7d-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="28e7d-124">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28e7d-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="28e7d-125">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="28e7d-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e7d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28e7d-126">Requirements</span></span>



| <span data-ttu-id="28e7d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e7d-127">Requirement</span></span> | <span data-ttu-id="28e7d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="28e7d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e7d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28e7d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="28e7d-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="28e7d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28e7d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="28e7d-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28e7d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28e7d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28e7d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e7d-134"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28e7d-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="28e7d-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="28e7d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="28e7d-136"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28e7d-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="28e7d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="28e7d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28e7d-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e7d-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="28e7d-139">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="28e7d-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28e7d-140">**GetCorePrinterDriversW** (Unicode) e **GetCorePrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="28e7d-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="28e7d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28e7d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e7d-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="28e7d-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="28e7d-143">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="28e7d-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

