---
description: La \_ struttura informazioni driver \_ 6 contiene informazioni sul driver della stampante.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Struttura DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311539"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="844de-103">\_Struttura informazioni driver \_ 6</span><span class="sxs-lookup"><span data-stu-id="844de-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="844de-104">La **struttura \_ informazioni driver \_ 6** contiene informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="844de-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="844de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="844de-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
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
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="844de-106">Members</span><span class="sxs-lookup"><span data-stu-id="844de-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="844de-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="844de-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="844de-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="844de-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="844de-109">Il valore supportato è 3.</span><span class="sxs-lookup"><span data-stu-id="844de-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="844de-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="844de-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="844de-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="844de-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="844de-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="844de-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="844de-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver, ad esempio Windows NT x86, Windows IA64 e Windows x64.</span><span class="sxs-lookup"><span data-stu-id="844de-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="844de-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="844de-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="844de-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo (ad esempio, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="844de-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="844de-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="844de-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="844de-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="844de-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="844de-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="844de-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="844de-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico della configurazione del driver di dispositivo (ad esempio, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="844de-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="844de-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="844de-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="844de-121">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo (ad esempio, C: \\ drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="844de-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="844de-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="844de-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="844de-123">Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="844de-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="844de-124">Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver.</span><span class="sxs-lookup"><span data-stu-id="844de-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="844de-125">La sequenza di stringhe termina con una stringa vuota di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="844de-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="844de-126">Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="844de-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="844de-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="844de-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="844de-128">Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, "monitoraggio PJL").</span><span class="sxs-lookup"><span data-stu-id="844de-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="844de-129">Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="844de-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="844de-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="844de-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="844de-131">Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".</span><span class="sxs-lookup"><span data-stu-id="844de-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="844de-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="844de-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="844de-133">Puntatore a una stringa con terminazione null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver.</span><span class="sxs-lookup"><span data-stu-id="844de-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="844de-134">Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="844de-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="844de-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="844de-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="844de-136">Data del pacchetto di driver, come codificato nei file del driver.</span><span class="sxs-lookup"><span data-stu-id="844de-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="844de-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="844de-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="844de-138">Numero di versione del driver.</span><span class="sxs-lookup"><span data-stu-id="844de-138">Version number of the driver.</span></span> <span data-ttu-id="844de-139">Questo deriva dalla struttura della versione del driver.</span><span class="sxs-lookup"><span data-stu-id="844de-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="844de-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="844de-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="844de-141">Puntatore a una stringa con terminazione null che specifica il nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="844de-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="844de-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="844de-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="844de-143">Puntatore a una stringa con terminazione null che specifica l'URL per il produttore.</span><span class="sxs-lookup"><span data-stu-id="844de-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="844de-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="844de-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="844de-145">Puntatore a una stringa con terminazione null che specifica l'ID hardware per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="844de-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="844de-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="844de-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="844de-147">Puntatore a una stringa con terminazione null che specifica il provider del driver della stampante (ad esempio, "Microsoft Windows 2000")</span><span class="sxs-lookup"><span data-stu-id="844de-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="844de-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="844de-148">Remarks</span></span>

<span data-ttu-id="844de-149">Le stringhe per questi membri sono contenute nel file con estensione inf utilizzato per aggiungere il driver.</span><span class="sxs-lookup"><span data-stu-id="844de-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="844de-150">Se si chiama [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md) con un *livello* diverso da 6 e quindi si chiama [**GetPrinterDriver**](getprinterdriver.md) o [**EnumPrinterDrivers**](enumprinterdrivers.md) con *Level* uguale a 6, viene restituita la struttura **info del driver \_ \_ 6** con **pszMfgName**, **pszOEMUrl**, **pszHardwareID** e **pszProvider** impostati su **null**, **dwlDriverVersion** impostato su 0 e **ftDriverDate** impostato su (0, 0).</span><span class="sxs-lookup"><span data-stu-id="844de-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="844de-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="844de-151">Requirements</span></span>



| <span data-ttu-id="844de-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="844de-152">Requirement</span></span> | <span data-ttu-id="844de-153">Valore</span><span class="sxs-lookup"><span data-stu-id="844de-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="844de-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844de-154">Minimum supported client</span></span><br/> | <span data-ttu-id="844de-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="844de-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="844de-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844de-156">Minimum supported server</span></span><br/> | <span data-ttu-id="844de-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="844de-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="844de-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="844de-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="844de-159"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="844de-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="844de-160">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="844de-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="844de-161">**\_ Informazioni sul driver \_ \_ 6W** (Unicode) e **\_ informazioni sul driver \_ \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="844de-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="844de-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="844de-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="844de-163">Stampa</span><span class="sxs-lookup"><span data-stu-id="844de-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="844de-164">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="844de-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="844de-165">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="844de-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="844de-166">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="844de-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="844de-167">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="844de-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="844de-168">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="844de-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




