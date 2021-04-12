---
description: Installa un driver della stampante da un pacchetto driver presente nell'archivio driver dei server di stampa.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Funzione InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233724"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="11012-103">InstallPrinterDriverFromPackage (funzione)</span><span class="sxs-lookup"><span data-stu-id="11012-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="11012-104">Installa un driver della stampante da un pacchetto driver presente nell'archivio driver del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="11012-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="11012-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11012-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="11012-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11012-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11012-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11012-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="11012-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="11012-109">**Null** indica il computer locale.</span><span class="sxs-lookup"><span data-stu-id="11012-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="11012-110">*pszInfPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11012-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11012-111">Puntatore a una stringa costante a terminazione null che specifica il percorso dell'archivio driver per il file. inf del driver di stampa.</span><span class="sxs-lookup"><span data-stu-id="11012-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="11012-112">**Null** indica che il driver si trova in un file inf fornito con Windows.</span><span class="sxs-lookup"><span data-stu-id="11012-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="11012-113">*pszDriverName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11012-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11012-114">Puntatore a una stringa costante a terminazione null che specifica il nome del driver.</span><span class="sxs-lookup"><span data-stu-id="11012-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="11012-115">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11012-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11012-116">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86.</span><span class="sxs-lookup"><span data-stu-id="11012-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="11012-117">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="11012-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11012-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11012-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11012-119">Questo può essere solo 0 o IPDFP \_ Copia \_ tutti \_ i file.</span><span class="sxs-lookup"><span data-stu-id="11012-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="11012-120">Il valore 0 indica che è necessario aggiungere il driver della stampante ed è necessario copiare tutti i file nella directory del driver della stampante più recenti rispetto ai file corrispondenti attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="11012-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="11012-121">Il valore IPDFP \_ copy \_ All \_ files indica che è necessario aggiungere il driver della stampante e tutti i file nella directory del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="11012-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="11012-122">I timestamp del file vengono ignorati quando *dwFlags* ha un valore IPDFP \_ Copia \_ tutti \_ i file.</span><span class="sxs-lookup"><span data-stu-id="11012-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11012-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11012-123">Return value</span></span>

<span data-ttu-id="11012-124">Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="11012-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="11012-125">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="11012-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11012-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="11012-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11012-127">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="11012-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="11012-128">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11012-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="11012-129">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="11012-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="11012-130">L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="11012-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="11012-131">**InstallPrinterDriverFromPackage** installa anche altri file nel pacchetto, ad esempio i profili colori e i processori di stampa.</span><span class="sxs-lookup"><span data-stu-id="11012-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="11012-132">Gli utenti devono disporre dei diritti di amministrazione della stampante per installare in un computer remoto o nel computer locale quando l'utente è connesso con Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="11012-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="11012-133">Solo i pacchetti firmati possono essere installati in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="11012-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="11012-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11012-134">Requirements</span></span>



| <span data-ttu-id="11012-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="11012-135">Requirement</span></span> | <span data-ttu-id="11012-136">Valore</span><span class="sxs-lookup"><span data-stu-id="11012-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11012-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11012-137">Minimum supported client</span></span><br/> | <span data-ttu-id="11012-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11012-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="11012-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11012-139">Minimum supported server</span></span><br/> | <span data-ttu-id="11012-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11012-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11012-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11012-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="11012-142"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11012-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="11012-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="11012-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="11012-144"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11012-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="11012-145">DLL</span><span class="sxs-lookup"><span data-stu-id="11012-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11012-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11012-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="11012-147">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="11012-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11012-148">**InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11012-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11012-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11012-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11012-150">Stampa</span><span class="sxs-lookup"><span data-stu-id="11012-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="11012-151">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="11012-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

