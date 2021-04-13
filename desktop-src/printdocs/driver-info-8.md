---
description: Contiene informazioni sul driver della stampante.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Struttura DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349091"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="61074-103">\_Struttura informazioni driver \_ 8</span><span class="sxs-lookup"><span data-stu-id="61074-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="61074-104">Contiene informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="61074-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="61074-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61074-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="61074-106">Members</span><span class="sxs-lookup"><span data-stu-id="61074-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="61074-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="61074-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="61074-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="61074-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="61074-109">Il valore supportato è 3.</span><span class="sxs-lookup"><span data-stu-id="61074-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="61074-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="61074-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="61074-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="61074-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="61074-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="61074-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="61074-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver, ad esempio Windows x86, Windows IA64 e Windows x64.</span><span class="sxs-lookup"><span data-stu-id="61074-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="61074-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="61074-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="61074-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo (ad esempio, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="61074-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="61074-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="61074-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="61074-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="61074-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="61074-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="61074-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="61074-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico della configurazione del driver di dispositivo (ad esempio, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="61074-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="61074-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="61074-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="61074-121">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo (ad esempio, C: \\ drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="61074-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="61074-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="61074-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="61074-123">Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="61074-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="61074-124">Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver.</span><span class="sxs-lookup"><span data-stu-id="61074-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="61074-125">La sequenza di stringhe termina con una stringa vuota di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="61074-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="61074-126">Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="61074-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="61074-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="61074-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="61074-128">Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, "monitoraggio PJL").</span><span class="sxs-lookup"><span data-stu-id="61074-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="61074-129">Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="61074-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="61074-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="61074-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="61074-131">Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".</span><span class="sxs-lookup"><span data-stu-id="61074-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="61074-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="61074-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="61074-133">Puntatore a una stringa con terminazione null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver.</span><span class="sxs-lookup"><span data-stu-id="61074-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="61074-134">Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="61074-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="61074-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="61074-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="61074-136">Data del pacchetto di driver, come codificato nei file del driver.</span><span class="sxs-lookup"><span data-stu-id="61074-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="61074-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="61074-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="61074-138">Numero di versione del driver.</span><span class="sxs-lookup"><span data-stu-id="61074-138">The version number of the driver.</span></span> <span data-ttu-id="61074-139">Questo deriva dalla struttura della versione del driver.</span><span class="sxs-lookup"><span data-stu-id="61074-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="61074-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="61074-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="61074-141">Puntatore a una stringa con terminazione null che specifica il nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="61074-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="61074-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="61074-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="61074-143">Puntatore a una stringa con terminazione null che specifica l'URL per il produttore.</span><span class="sxs-lookup"><span data-stu-id="61074-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="61074-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="61074-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="61074-145">Puntatore a una stringa con terminazione null che specifica l'ID hardware per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="61074-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="61074-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="61074-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="61074-147">Puntatore a una stringa con terminazione null che specifica il provider del driver della stampante (ad esempio, "Microsoft Windows 2000").</span><span class="sxs-lookup"><span data-stu-id="61074-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="61074-148">**pszPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="61074-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="61074-149">Puntatore a una stringa con terminazione null che specifica il processore di stampa, ad esempio "WinPrint".</span><span class="sxs-lookup"><span data-stu-id="61074-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="61074-150">**pszVendorSetup**</span><span class="sxs-lookup"><span data-stu-id="61074-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="61074-151">Puntatore a una stringa con terminazione null che specifica la DLL di installazione del driver del fornitore e il punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="61074-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="61074-152">**pszzColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="61074-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="61074-153">Puntatore a una stringa con terminazione null che specifica i profili colori associati al driver.</span><span class="sxs-lookup"><span data-stu-id="61074-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="61074-154">**pszInfPath**</span><span class="sxs-lookup"><span data-stu-id="61074-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="61074-155">Puntatore a una stringa con terminazione null che specifica il percorso del file. inf del driver nell'archivio driver.</span><span class="sxs-lookup"><span data-stu-id="61074-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="61074-156">(Vedere la sezione Osservazioni). Deve essere **null** se il driver \_ info \_ 8 viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="61074-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="61074-157">**dwPrinterDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="61074-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="61074-158">Flag di attributo per i driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="61074-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="61074-159">Deve essere 0 se il DRIVER \_ info \_ 8 viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="61074-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="61074-160">In caso contrario, può essere una qualsiasi combinazione dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="61074-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="61074-161">Nome/valore del flag</span><span class="sxs-lookup"><span data-stu-id="61074-161">Flag name/value</span></span>                                                         | <span data-ttu-id="61074-162">Significato</span><span class="sxs-lookup"><span data-stu-id="61074-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="61074-163">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="61074-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="61074-164">compatibile con il \_ pacchetto driver della stampante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61074-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="61074-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="61074-165">0x00000001</span></span><br/>        | <span data-ttu-id="61074-166">Il driver della stampante fa parte di un pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="61074-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="61074-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61074-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="61074-168">DRIVER della stampante \_ \_ XPS</span><span class="sxs-lookup"><span data-stu-id="61074-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="61074-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="61074-169">0x00000002</span></span><br/>                   | <span data-ttu-id="61074-170">Il driver della stampante supporta il formato XPS Microsoft descritto in [XML Paper Specification: Panoramica](/previous-versions/windows/hardware/design/dn641615(v=vs.85))e anche in [comportamento del prodotto, sezione <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="61074-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="61074-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-171">Windows 8</span></span><br/> <span data-ttu-id="61074-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-173">\_sandbox driver della stampante \_ \_ abilitato</span><span class="sxs-lookup"><span data-stu-id="61074-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="61074-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="61074-174">0x00000004</span></span><br/>      | <span data-ttu-id="61074-175">Il driver della stampante è compatibile con l' [isolamento dei driver della stampante](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="61074-176">Per ulteriori informazioni, vedere il [comportamento del prodotto, sezione <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="61074-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="61074-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61074-177">Windows 7</span></span><br/> <span data-ttu-id="61074-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61074-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="61074-179">\_classe driver della stampante \_</span><span class="sxs-lookup"><span data-stu-id="61074-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="61074-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="61074-180">0x00000008</span></span><br/>                 | <span data-ttu-id="61074-181">Il driver della stampante è un [driver della stampante di classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="61074-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-182">Windows 8</span></span><br/> <span data-ttu-id="61074-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-184">DRIVER della stampante \_ \_ derivato</span><span class="sxs-lookup"><span data-stu-id="61074-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="61074-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61074-185">0x00000010</span></span><br/>               | <span data-ttu-id="61074-186">Il driver della stampante è un [driver della stampante derivato](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="61074-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-187">Windows 8</span></span><br/> <span data-ttu-id="61074-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-189">DRIVER della stampante \_ \_ non \_ condivisibile</span><span class="sxs-lookup"><span data-stu-id="61074-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="61074-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="61074-190">0x00000020</span></span><br/>        | <span data-ttu-id="61074-191">Le stampanti che utilizzano questo driver della stampante non possono essere condivise.</span><span class="sxs-lookup"><span data-stu-id="61074-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="61074-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-192">Windows 8</span></span><br/> <span data-ttu-id="61074-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-194">\_ \_ Fax categoria driver della stampante \_</span><span class="sxs-lookup"><span data-stu-id="61074-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="61074-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="61074-195">0x00000040</span></span><br/>         | <span data-ttu-id="61074-196">Il driver della stampante è destinato all'utilizzo con [stampanti fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="61074-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-197">Windows 8</span></span><br/> <span data-ttu-id="61074-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-199">\_file di \_ categoria del driver della stampante \_</span><span class="sxs-lookup"><span data-stu-id="61074-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="61074-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="61074-200">0x00000080</span></span><br/>        | <span data-ttu-id="61074-201">Il driver della stampante è destinato all'uso con [stampanti di file](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="61074-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-202">Windows 8</span></span><br/> <span data-ttu-id="61074-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-204">\_categoria driver della stampante \_ \_ virtuale</span><span class="sxs-lookup"><span data-stu-id="61074-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="61074-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="61074-205">0x00000100</span></span><br/>     | <span data-ttu-id="61074-206">Il driver della stampante è destinato all'uso con le [stampanti virtuali](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="61074-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-207">Windows 8</span></span><br/> <span data-ttu-id="61074-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-209">\_ \_ servizio categoria driver \_ stampanti</span><span class="sxs-lookup"><span data-stu-id="61074-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="61074-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="61074-210">0x00000200</span></span><br/>     | <span data-ttu-id="61074-211">Il driver della stampante è destinato all'uso con le [stampanti del servizio](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="61074-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="61074-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-212">Windows 8</span></span><br/> <span data-ttu-id="61074-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="61074-214">reimpostazione soft del driver della stampante \_ \_ \_ \_ obbligatoria</span><span class="sxs-lookup"><span data-stu-id="61074-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="61074-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="61074-215">0x00000400</span></span><br/> | <span data-ttu-id="61074-216">Le stampanti che utilizzano questo driver della stampante devono seguire le linee guida descritte nella definizione della classe dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="61074-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="61074-217">Per ulteriori informazioni, vedere il [comportamento del prodotto, sezione <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="61074-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="61074-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61074-218">Windows 8</span></span><br/> <span data-ttu-id="61074-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61074-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="61074-220">**pszzCoreDriverDependencies**</span><span class="sxs-lookup"><span data-stu-id="61074-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="61074-221">Puntatore a una stringa multistringa con terminazione null che specifica tutti i driver della stampante di base da cui dipende il driver.</span><span class="sxs-lookup"><span data-stu-id="61074-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="61074-222">Deve essere **null** se il **driver \_ info \_ 8** viene passato a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="61074-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="61074-223">**ftMinInboxDriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="61074-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="61074-224">Data più recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.</span><span class="sxs-lookup"><span data-stu-id="61074-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="61074-225">**dwlMinInboxDriverVerVersion**</span><span class="sxs-lookup"><span data-stu-id="61074-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="61074-226">La versione più recente consentita di tutti i driver forniti con Windows e da cui dipende questo driver.</span><span class="sxs-lookup"><span data-stu-id="61074-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61074-227">Commenti</span><span class="sxs-lookup"><span data-stu-id="61074-227">Remarks</span></span>

<span data-ttu-id="61074-228">Le stringhe per questi membri sono contenute nel file con estensione inf utilizzato per aggiungere il driver.</span><span class="sxs-lookup"><span data-stu-id="61074-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="61074-229">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61074-229">Requirements</span></span>



| <span data-ttu-id="61074-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="61074-230">Requirement</span></span> | <span data-ttu-id="61074-231">Valore</span><span class="sxs-lookup"><span data-stu-id="61074-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61074-232">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61074-232">Minimum supported client</span></span><br/> | <span data-ttu-id="61074-233">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61074-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="61074-234">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61074-234">Minimum supported server</span></span><br/> | <span data-ttu-id="61074-235">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61074-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61074-236">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61074-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="61074-237"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61074-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="61074-238">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="61074-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="61074-239">**\_ \_ Informazioni driver \_ 8W** (Unicode) e **\_ driver \_ info \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="61074-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="61074-240">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61074-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61074-241">Stampa</span><span class="sxs-lookup"><span data-stu-id="61074-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="61074-242">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="61074-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="61074-243">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="61074-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="61074-244">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="61074-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

