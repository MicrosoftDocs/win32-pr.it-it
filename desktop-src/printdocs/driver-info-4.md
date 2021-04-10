---
description: La \_ struttura informazioni driver \_ 4 contiene informazioni sul driver della stampante.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Struttura DRIVER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227350"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="f75fe-103">\_Struttura informazioni driver \_ 4</span><span class="sxs-lookup"><span data-stu-id="f75fe-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="f75fe-104">La **struttura \_ informazioni driver \_ 4** contiene informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="f75fe-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f75fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f75fe-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="f75fe-106">Members</span><span class="sxs-lookup"><span data-stu-id="f75fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f75fe-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="f75fe-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="f75fe-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="f75fe-109">Il valore supportato è 3.</span><span class="sxs-lookup"><span data-stu-id="f75fe-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="f75fe-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="f75fe-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f75fe-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver (ad esempio, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="f75fe-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="f75fe-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo (ad esempio, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="f75fe-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="f75fe-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="f75fe-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="f75fe-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico della configurazione del driver di dispositivo (ad esempio, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="f75fe-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="f75fe-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-121">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f75fe-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="f75fe-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-123">Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="f75fe-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="f75fe-124">Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver.</span><span class="sxs-lookup"><span data-stu-id="f75fe-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="f75fe-125">La sequenza di stringhe termina con una stringa vuota di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="f75fe-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="f75fe-126">Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="f75fe-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="f75fe-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-128">Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, il monitoraggio di PJL).</span><span class="sxs-lookup"><span data-stu-id="f75fe-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="f75fe-129">Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="f75fe-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="f75fe-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-131">Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio EMF.</span><span class="sxs-lookup"><span data-stu-id="f75fe-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="f75fe-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="f75fe-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="f75fe-133">Puntatore a una stringa con terminazione null che specifica i nomi dei driver della stampante precedenti compatibili con questo driver.</span><span class="sxs-lookup"><span data-stu-id="f75fe-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="f75fe-134">Ad esempio, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="f75fe-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f75fe-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f75fe-135">Requirements</span></span>



| <span data-ttu-id="f75fe-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f75fe-136">Requirement</span></span> | <span data-ttu-id="f75fe-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f75fe-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f75fe-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f75fe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f75fe-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f75fe-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f75fe-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f75fe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f75fe-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f75fe-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f75fe-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f75fe-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f75fe-143"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f75fe-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f75fe-144">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f75fe-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f75fe-145">**\_ \_ Informazioni driver \_ 4W** (Unicode) e **\_ driver \_ info \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f75fe-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="f75fe-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f75fe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75fe-147">Stampa</span><span class="sxs-lookup"><span data-stu-id="f75fe-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f75fe-148">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f75fe-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f75fe-149">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="f75fe-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="f75fe-150">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="f75fe-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="f75fe-151">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="f75fe-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




