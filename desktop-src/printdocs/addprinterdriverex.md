---
description: La funzione AddPrinterDriverEx installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Funzione AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311565"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="7c06c-103">AddPrinterDriverEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c06c-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="7c06c-104">La funzione **AddPrinterDriverEx** installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver.</span><span class="sxs-lookup"><span data-stu-id="7c06c-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="7c06c-105">Oltre a disporre delle funzionalità di [**AddPrinterDriver**](addprinterdriver.md), dispone anche di opzioni che consentono l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori temporali dei file).</span><span class="sxs-lookup"><span data-stu-id="7c06c-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="7c06c-106">Non è più consigliabile installare un driver della stampante senza un pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="7c06c-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="7c06c-107">In alternativa, usare [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) .</span><span class="sxs-lookup"><span data-stu-id="7c06c-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7c06c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c06c-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7c06c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c06c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c06c-110">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c06c-111">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il driver.</span><span class="sxs-lookup"><span data-stu-id="7c06c-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="7c06c-112">Se questo parametro è **null**, la funzione installa il driver nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="7c06c-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7c06c-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c06c-114">Versione della struttura a cui punta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="7c06c-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="7c06c-115">Questo valore può essere 2, 3, 4, 6 o 8.</span><span class="sxs-lookup"><span data-stu-id="7c06c-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="7c06c-116">*pDriverInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c06c-117">Puntatore a una struttura contenente informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c06c-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="7c06c-118">Può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c06c-118">It can be one of the following.</span></span>



| <span data-ttu-id="7c06c-119">Valore del livello</span><span class="sxs-lookup"><span data-stu-id="7c06c-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="7c06c-120">\_Struttura informazioni \_ \* driver</span><span class="sxs-lookup"><span data-stu-id="7c06c-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="7c06c-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="7c06c-122">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7c06c-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="7c06c-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="7c06c-124">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="7c06c-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="7c06c-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="7c06c-126">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="7c06c-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="7c06c-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="7c06c-128">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="7c06c-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="7c06c-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="7c06c-130">**\_Informazioni driver \_ 8**</span><span class="sxs-lookup"><span data-stu-id="7c06c-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="7c06c-131">Se il membro **pEnvironment** della struttura a cui punta *pDriverInfo* è **null**, la funzione usa l'ambiente corrente del chiamante/client, non l'ambiente del server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c06c-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="7c06c-132">*dwFileCopyFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c06c-133">Opzioni per la copia dei file del driver.</span><span class="sxs-lookup"><span data-stu-id="7c06c-133">The options for copying the driver files.</span></span> <span data-ttu-id="7c06c-134">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c06c-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7c06c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7c06c-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="7c06c-136">Significato</span><span class="sxs-lookup"><span data-stu-id="7c06c-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="7c06c-137"><dt>**APD \_ Copia \_ tutti \_ i file**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="7c06c-138">Aggiungere il driver della stampante e copiare tutti i file nella Directory Printer-driver.</span><span class="sxs-lookup"><span data-stu-id="7c06c-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="7c06c-139">I timestamp del file vengono ignorati con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="7c06c-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="7c06c-140"><dt>**APD \_ Copia \_ dalla \_ Directory**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="7c06c-141">Aggiungere il driver della stampante utilizzando i nomi di file completi specificati nella [**struttura \_ informazioni driver \_ 6**](driver-info-6.md) .</span><span class="sxs-lookup"><span data-stu-id="7c06c-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="7c06c-142">Questo flag è ORed insieme a uno degli altri flag di copia.</span><span class="sxs-lookup"><span data-stu-id="7c06c-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="7c06c-143">Se questo flag è impostato, **AddPrinterDriverEx** avrà esito negativo se i file non esistono dove sono specificati nella struttura di **informazioni del \_ driver \_ 6** .</span><span class="sxs-lookup"><span data-stu-id="7c06c-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="7c06c-144">Non è necessario copiare i file nella directory del driver della stampante del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c06c-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="7c06c-145">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7c06c-145">See the Remarks.</span></span><br/> <span data-ttu-id="7c06c-146">**Windows 2000:** Questo flag non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c06c-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="7c06c-147"><dt>**APD \_ Copia \_ nuovi \_ file**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="7c06c-148">Aggiungere il driver della stampante e copiare i file nella directory del driver della stampante più recenti rispetto a tutti i file corrispondenti attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7c06c-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="7c06c-149">Questo flag emula il comportamento di [**AddPrinterDriver**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="7c06c-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="7c06c-150"><dt>**\_downgrade Strict di APD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="7c06c-151">Aggiungere il driver della stampante solo se tutti i file nella directory del driver della stampante sono più vecchi di tutti i file corrispondenti attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7c06c-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="7c06c-152"><dt>**aggiornamento di APD \_ strict \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="7c06c-153">Aggiungere il driver della stampante solo se tutti i file nella directory del driver della stampante sono più recenti rispetto ai file attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7c06c-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c06c-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c06c-154">Return value</span></span>

<span data-ttu-id="7c06c-155">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7c06c-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7c06c-156">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="7c06c-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="7c06c-157">Se il driver della stampante presenta problemi di utilizzo del sistema operativo, **AddPrinterDriverEx** avrà esito negativo con uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c06c-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="7c06c-158">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="7c06c-158">Error Code</span></span>                      | <span data-ttu-id="7c06c-159">Significato</span><span class="sxs-lookup"><span data-stu-id="7c06c-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c06c-160">\_driver della stampante di errore \_ \_ bloccato</span><span class="sxs-lookup"><span data-stu-id="7c06c-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="7c06c-161">Il driver non funziona nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c06c-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="7c06c-162">\_ \_ avviso driver stampante \_ errore</span><span class="sxs-lookup"><span data-stu-id="7c06c-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="7c06c-163">Il driver non è affidabile sul sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c06c-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="7c06c-164">Tuttavia, se \_ \_ \_ si specifica il driver APD install warningd, il driver viene installato e non viene fornito alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="7c06c-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="7c06c-165">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7c06c-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c06c-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c06c-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7c06c-167">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7c06c-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7c06c-168">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c06c-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7c06c-169">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="7c06c-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="7c06c-170">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="7c06c-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="7c06c-171">Prima di chiamare la funzione **AddPrinterDriverEx** , tutti i file richiesti dal driver devono essere copiati nella directory di driver della stampante del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c06c-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="7c06c-172">Per recuperare il nome di questa directory, chiamare la funzione [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="7c06c-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="7c06c-173">Per determinare i driver della stampante attualmente installati, chiamare la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="7c06c-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="7c06c-174">Se il driver della stampante è stato aggiunto correttamente, la funzione chiama la funzione DrvDriverEvent (DRIVER \_ Event \_ Initialize, Level, driver \_ info \_ \* , lParam) per consentire al driver di eseguire le inizializzazioni richieste durante l'installazione di un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c06c-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="7c06c-175">Per ulteriori informazioni su **DrvDriverEvent**, vedere Microsoft Windows Driver Development Kit (DDK)</span><span class="sxs-lookup"><span data-stu-id="7c06c-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="7c06c-176">Il driver non deve usare una chiamata dell'interfaccia utente durante la chiamata a **DrvDriverEvent**.</span><span class="sxs-lookup"><span data-stu-id="7c06c-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="7c06c-177">Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce VendorSetup nel file con estensione inf della stampante o, per Plug and Play dispositivi, il programma di installazione può usare un programma di coinstallazione specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c06c-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="7c06c-178">Per ulteriori informazioni su VendorSetup, vedere DDK.</span><span class="sxs-lookup"><span data-stu-id="7c06c-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="7c06c-179">I file a cui viene fatto riferimento nella struttura di [**informazioni sul driver \_ \_ 6**](driver-info-6.md) devono essere locali rispetto al computer da cui viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="7c06c-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="7c06c-180">Un nome file può essere un nome UNC purché il nome UNC sia il computer locale.</span><span class="sxs-lookup"><span data-stu-id="7c06c-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c06c-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c06c-181">Requirements</span></span>



| <span data-ttu-id="7c06c-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c06c-182">Requirement</span></span> | <span data-ttu-id="7c06c-183">Valore</span><span class="sxs-lookup"><span data-stu-id="7c06c-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c06c-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c06c-184">Minimum supported client</span></span><br/> | <span data-ttu-id="7c06c-185">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c06c-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c06c-186">Minimum supported server</span></span><br/> | <span data-ttu-id="7c06c-187">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c06c-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c06c-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c06c-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c06c-189"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7c06c-190">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c06c-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c06c-191"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7c06c-192">DLL</span><span class="sxs-lookup"><span data-stu-id="7c06c-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c06c-193"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7c06c-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7c06c-194">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7c06c-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c06c-195">**AddPrinterDriverExW** (Unicode) e **AddPrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c06c-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7c06c-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c06c-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c06c-197">Stampa</span><span class="sxs-lookup"><span data-stu-id="7c06c-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7c06c-198">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7c06c-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7c06c-199">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="7c06c-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="7c06c-200">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7c06c-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="7c06c-201">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="7c06c-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="7c06c-202">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="7c06c-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="7c06c-203">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="7c06c-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="7c06c-204">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="7c06c-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="7c06c-205">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="7c06c-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="7c06c-206">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="7c06c-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

