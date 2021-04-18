---
description: La funzione DeletePrinterDriverEx rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver. Questa funzione può anche eliminare versioni specifiche del driver.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Funzione DeletePrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313025"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="de5c2-104">DeletePrinterDriverEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="de5c2-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="de5c2-105">La funzione **DeletePrinterDriverEx** rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver.</span><span class="sxs-lookup"><span data-stu-id="de5c2-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="de5c2-106">Questa funzione può anche eliminare versioni specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="de5c2-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5c2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de5c2-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="de5c2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="de5c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de5c2-109">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5c2-110">Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere eliminato il driver.</span><span class="sxs-lookup"><span data-stu-id="de5c2-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="de5c2-111">Se questo parametro è **null**, la funzione eliminerà il driver della stampante dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="de5c2-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="de5c2-112">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5c2-113">Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere eliminato il driver, ad esempio Windows NT x86, Windows IA64 o Windows x64.</span><span class="sxs-lookup"><span data-stu-id="de5c2-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="de5c2-114">Se questo parametro è **null**, il nome del driver viene eliminato dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="de5c2-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="de5c2-115">*pDriverName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5c2-116">Puntatore a una stringa con terminazione null che specifica il nome del driver da eliminare.</span><span class="sxs-lookup"><span data-stu-id="de5c2-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="de5c2-117">*dwDeleteFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5c2-118">Opzioni per l'eliminazione di file e versioni del driver.</span><span class="sxs-lookup"><span data-stu-id="de5c2-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="de5c2-119">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="de5c2-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="de5c2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="de5c2-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="de5c2-121">Significato</span><span class="sxs-lookup"><span data-stu-id="de5c2-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="de5c2-122"><dt>**\_ \_ versione specifica dell'eliminazione DPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="de5c2-123">Elimina la versione specificata in *dwVersionFlag*.</span><span class="sxs-lookup"><span data-stu-id="de5c2-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="de5c2-124">Ciò non garantisce che il driver venga rimosso dall'elenco dei driver supportati per il server.</span><span class="sxs-lookup"><span data-stu-id="de5c2-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="de5c2-125"><dt>**\_Elimina \_ file inutilizzati DPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="de5c2-126">Rimuove tutti i file di driver non utilizzati.</span><span class="sxs-lookup"><span data-stu-id="de5c2-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="de5c2-127"><dt>**DPD \_ Elimina \_ tutti \_ i file**</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="de5c2-128">Elimina il driver solo se è possibile rimuovere tutti i file associati.</span><span class="sxs-lookup"><span data-stu-id="de5c2-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="de5c2-129">L'operazione di eliminazione ha esito negativo se uno dei file del driver viene usato da un altro driver installato.</span><span class="sxs-lookup"><span data-stu-id="de5c2-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="de5c2-130">Se \_ \_ \_ non viene specificata la versione specifica di DPD Delete, la funzione eliminerà tutte le versioni del driver se nessuna di esse è in uso.</span><span class="sxs-lookup"><span data-stu-id="de5c2-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="de5c2-131">Se non \_ vengono eliminati \_ i file inutilizzati \_ o DPD \_ Delete \_ tutti \_ i file, la funzione non elimina i file del driver.</span><span class="sxs-lookup"><span data-stu-id="de5c2-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="de5c2-132">*dwVersionFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de5c2-133">Versione del driver da eliminare.</span><span class="sxs-lookup"><span data-stu-id="de5c2-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="de5c2-134">Questo parametro può essere 0, 1, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="de5c2-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="de5c2-135">Questo parametro viene usato solo se *dwDeleteFlag* include il \_ flag di \_ versione specifico dell'eliminazione DPD \_ .</span><span class="sxs-lookup"><span data-stu-id="de5c2-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de5c2-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de5c2-136">Return value</span></span>

<span data-ttu-id="de5c2-137">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="de5c2-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="de5c2-138">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="de5c2-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5c2-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5c2-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de5c2-140">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="de5c2-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="de5c2-141">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5c2-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="de5c2-142">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="de5c2-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="de5c2-143">Prima che la funzione elimini i file del driver, chiama la funzione **DrvDriverEvent** del driver, consentendo al driver di rimuovere tutti i file privati che non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="de5c2-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="de5c2-144">Per ulteriori informazioni su **DrvDriverEvent**, vedere Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="de5c2-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="de5c2-145">Se i file dei driver sono attualmente caricati, la funzione li sposta in una directory Temp e li contrassegna per l'eliminazione al riavvio.</span><span class="sxs-lookup"><span data-stu-id="de5c2-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="de5c2-146">Prima di chiamare **DeletePrinterDriverEx**, è necessario eliminare tutti gli oggetti stampante che usano il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="de5c2-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5c2-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de5c2-147">Requirements</span></span>



| <span data-ttu-id="de5c2-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5c2-148">Requirement</span></span> | <span data-ttu-id="de5c2-149">Valore</span><span class="sxs-lookup"><span data-stu-id="de5c2-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5c2-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5c2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="de5c2-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de5c2-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5c2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="de5c2-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de5c2-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de5c2-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de5c2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="de5c2-155"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="de5c2-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="de5c2-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="de5c2-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="de5c2-158">DLL</span><span class="sxs-lookup"><span data-stu-id="de5c2-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de5c2-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="de5c2-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="de5c2-160">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="de5c2-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="de5c2-161">**DeletePrinterDriverExW** (Unicode) e **DeletePrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="de5c2-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="de5c2-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de5c2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5c2-163">Stampa</span><span class="sxs-lookup"><span data-stu-id="de5c2-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="de5c2-164">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="de5c2-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="de5c2-165">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="de5c2-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




