---
description: La \_ struttura informazioni driver \_ 3 contiene informazioni sul driver della stampante.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Struttura DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317296"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="159e3-103">\_Struttura informazioni driver \_ 3</span><span class="sxs-lookup"><span data-stu-id="159e3-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="159e3-104">La **struttura \_ informazioni driver \_ 3** contiene informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="159e3-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="159e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="159e3-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="159e3-106">Members</span><span class="sxs-lookup"><span data-stu-id="159e3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="159e3-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="159e3-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="159e3-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="159e3-109">I valori supportati sono 3 e 4, che rappresentano rispettivamente i driver v3 e V4.</span><span class="sxs-lookup"><span data-stu-id="159e3-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="159e3-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="159e3-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="159e3-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="159e3-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="159e3-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver (ad esempio, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="159e3-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="159e3-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="159e3-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo, ad esempio "C: \\ drivers \\Pscript.dll".</span><span class="sxs-lookup"><span data-stu-id="159e3-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="159e3-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="159e3-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, "C: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="159e3-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="159e3-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="159e3-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria di collegamento dinamico della configurazione del driver di dispositivo, ad esempio "C: \\ drivers \\Pscrptui.dll".</span><span class="sxs-lookup"><span data-stu-id="159e3-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="159e3-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="159e3-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-121">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file della guida del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="159e3-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="159e3-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="159e3-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-123">Puntatore a un buffer MultiSZ che contiene una sequenza di stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="159e3-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="159e3-124">Ogni stringa con terminazione null nel buffer contiene il nome di un file da cui dipende il driver.</span><span class="sxs-lookup"><span data-stu-id="159e3-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="159e3-125">La sequenza di stringhe termina con una stringa vuota di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="159e3-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="159e3-126">Se **pDependentFiles** non è **null** e non contiene nomi di file, punterà a un buffer contenente due stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="159e3-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="159e3-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="159e3-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-128">Puntatore a una stringa con terminazione null che specifica un monitor del linguaggio (ad esempio, "monitoraggio PJL").</span><span class="sxs-lookup"><span data-stu-id="159e3-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="159e3-129">Questo membro può essere **null** e deve essere specificato solo per le stampanti in grado di comunicare bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="159e3-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="159e3-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="159e3-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="159e3-131">Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito del processo di stampa, ad esempio "EMF".</span><span class="sxs-lookup"><span data-stu-id="159e3-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="159e3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="159e3-132">Requirements</span></span>



| <span data-ttu-id="159e3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="159e3-133">Requirement</span></span> | <span data-ttu-id="159e3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="159e3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159e3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="159e3-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="159e3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="159e3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="159e3-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="159e3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="159e3-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="159e3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="159e3-140"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="159e3-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="159e3-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="159e3-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="159e3-142">**\_ Informazioni sul driver \_ \_ 3W** (Unicode) e **\_ informazioni sul driver \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="159e3-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="159e3-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="159e3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159e3-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="159e3-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="159e3-145">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="159e3-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="159e3-146">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="159e3-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="159e3-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="159e3-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="159e3-148">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="159e3-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




