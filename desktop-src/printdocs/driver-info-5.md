---
description: La \_ struttura informazioni driver \_ 5 contiene informazioni sul driver della stampante.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: Struttura DRIVER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318034"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="97003-103">\_Struttura informazioni driver \_ 5</span><span class="sxs-lookup"><span data-stu-id="97003-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="97003-104">La **struttura \_ informazioni driver \_ 5** contiene informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="97003-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="97003-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97003-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="97003-106">Members</span><span class="sxs-lookup"><span data-stu-id="97003-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="97003-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="97003-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="97003-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="97003-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="97003-109">Il valore supportato è 3.</span><span class="sxs-lookup"><span data-stu-id="97003-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="97003-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="97003-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="97003-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="97003-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="97003-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="97003-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="97003-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver (ad esempio, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="97003-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="97003-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="97003-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="97003-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo (ad esempio, C: \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="97003-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="97003-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="97003-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="97003-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="97003-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="97003-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="97003-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="97003-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la libreria a collegamento dinamico della configurazione del driver di dispositivo (ad esempio, C: \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="97003-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="97003-120">**dwDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="97003-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="97003-121">Attributi del driver, ad esempio UMPD/KMPD.</span><span class="sxs-lookup"><span data-stu-id="97003-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="97003-122">**dwConfigVersion**</span><span class="sxs-lookup"><span data-stu-id="97003-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="97003-123">Numero di volte in cui il file di configurazione per questo driver è stato aggiornato o è stato eseguito il downgrade dall'ultimo riavvio dello spooler.</span><span class="sxs-lookup"><span data-stu-id="97003-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="97003-124">**dwDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="97003-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="97003-125">Numero di volte in cui è stato eseguito l'aggiornamento o il downgrade del file del driver per questo driver dall'ultimo riavvio dello spooler.</span><span class="sxs-lookup"><span data-stu-id="97003-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97003-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97003-126">Requirements</span></span>



| <span data-ttu-id="97003-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="97003-127">Requirement</span></span> | <span data-ttu-id="97003-128">Valore</span><span class="sxs-lookup"><span data-stu-id="97003-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97003-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97003-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97003-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97003-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97003-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97003-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97003-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97003-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="97003-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97003-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="97003-134"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97003-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="97003-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="97003-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="97003-136">**\_ Informazioni sul driver \_ \_ 5W** (Unicode) e **\_ informazioni sul driver \_ \_ 5a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="97003-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="97003-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97003-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97003-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="97003-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="97003-139">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="97003-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="97003-140">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="97003-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="97003-141">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="97003-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="97003-142">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="97003-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




