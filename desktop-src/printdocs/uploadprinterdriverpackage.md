---
description: Carica un driver della stampante nell'archivio driver dei server di stampa, in modo che possa essere installato chiamando InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Funzione UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233341"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="f3e9e-103">UploadPrinterDriverPackage (funzione)</span><span class="sxs-lookup"><span data-stu-id="f3e9e-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="f3e9e-104">Carica un driver della stampante nell'archivio driver del server di stampa, in modo che possa essere installato chiamando [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span><span class="sxs-lookup"><span data-stu-id="f3e9e-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3e9e-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="f3e9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3e9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e9e-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="f3e9e-109">Utilizzare **null** se il server è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-110">*pszInfPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-111">Puntatore a una stringa costante a terminazione null che specifica il percorso di origine del file. inf del driver.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-112">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-113">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore del server (ad esempio, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="f3e9e-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="f3e9e-114">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-116">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3e9e-116">This can be any of the following values:</span></span>



| <span data-ttu-id="f3e9e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f3e9e-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="f3e9e-118">Significato</span><span class="sxs-lookup"><span data-stu-id="f3e9e-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="f3e9e-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="f3e9e-120">L'interfaccia utente non verrà visualizzata durante il caricamento.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="f3e9e-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="f3e9e-122">I file verranno caricati anche se il pacchetto è già presente nell'archivio driver del server.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="f3e9e-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="f3e9e-124">L'archivio driver del server verrà verificato prima del caricamento per verificare se il pacchetto è già presente.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="f3e9e-125">Questa impostazione viene ignorata se è impostato UPDP_UPLOAD_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3e9e-126">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-127">Handle per l'interfaccia utente di copia.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-128">*pszDestInfPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-129">Puntatore al percorso di destinazione, nell'archivio driver, in cui è stato copiato il file. inf del driver.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="f3e9e-130">*pcchDestInfPath* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e9e-131">In input, specifica la dimensione, in caratteri, del buffer *pszDestInfPath* .</span><span class="sxs-lookup"><span data-stu-id="f3e9e-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="f3e9e-132">Nell'output, riceve la dimensione, in caratteri, della stringa di percorso, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3e9e-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3e9e-133">Return value</span></span>

<span data-ttu-id="f3e9e-134">Se l'operazione ha esito positivo, il valore restituito viene S_OK. in caso contrario, **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="f3e9e-135">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f3e9e-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e9e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3e9e-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f3e9e-137">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f3e9e-138">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f3e9e-139">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f3e9e-140">L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="f3e9e-141">È possibile caricare un solo pacchetto alla volta.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="f3e9e-142">Se un pacchetto dipende da altri, è necessario caricarlo separatamente.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="f3e9e-143">È possibile caricare solo i pacchetti driver firmati.</span><span class="sxs-lookup"><span data-stu-id="f3e9e-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e9e-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3e9e-144">Requirements</span></span>



| <span data-ttu-id="f3e9e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e9e-145">Requirement</span></span> | <span data-ttu-id="f3e9e-146">Valore</span><span class="sxs-lookup"><span data-stu-id="f3e9e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e9e-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e9e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e9e-148">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f3e9e-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e9e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e9e-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3e9e-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3e9e-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3e9e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e9e-152"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f3e9e-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3e9e-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3e9e-154"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f3e9e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f3e9e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3e9e-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9e-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="f3e9e-157">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f3e9e-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f3e9e-158">**UploadPrinterDriverPackageW** (Unicode) e **UploadPrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3e9e-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f3e9e-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3e9e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e9e-160">Stampa</span><span class="sxs-lookup"><span data-stu-id="f3e9e-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f3e9e-161">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f3e9e-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

