---
description: La \_ struttura informazioni driver \_ 2 identifica un driver della stampante, il numero di versione del driver, l'ambiente per cui è stato scritto il driver, il nome del file in cui è archiviato il driver e così via.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Struttura DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311541"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="c0261-103">\_Struttura informazioni driver \_ 2</span><span class="sxs-lookup"><span data-stu-id="c0261-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="c0261-104">La **struttura \_ informazioni driver \_ 2** identifica un driver della stampante, il numero di versione del driver, l'ambiente per cui è stato scritto il driver, il nome del file in cui è archiviato il driver e così via.</span><span class="sxs-lookup"><span data-stu-id="c0261-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0261-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0261-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="c0261-106">Members</span><span class="sxs-lookup"><span data-stu-id="c0261-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0261-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="c0261-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-108">Versione del sistema operativo per cui è stato scritto il driver.</span><span class="sxs-lookup"><span data-stu-id="c0261-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="c0261-109">Il valore supportato è 3.</span><span class="sxs-lookup"><span data-stu-id="c0261-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="c0261-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="c0261-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-111">Puntatore a una stringa con terminazione null che specifica il nome del driver (ad esempio, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="c0261-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="c0261-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="c0261-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-113">Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il driver (ad esempio, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="c0261-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="c0261-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="c0261-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-115">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file contenente il driver di dispositivo, ad esempio "c: \\ drivers \\pscript.dll".</span><span class="sxs-lookup"><span data-stu-id="c0261-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="c0261-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="c0261-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-117">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per il file che contiene i dati del driver (ad esempio, "c: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="c0261-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="c0261-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="c0261-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="c0261-119">Puntatore a una stringa con terminazione null che specifica un nome file o un percorso completo e un nome file per la dll di configurazione del driver del dispositivo (ad esempio, "c: \\ drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="c0261-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0261-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0261-120">Requirements</span></span>



| <span data-ttu-id="c0261-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0261-121">Requirement</span></span> | <span data-ttu-id="c0261-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c0261-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0261-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0261-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0261-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0261-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c0261-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0261-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0261-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0261-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c0261-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0261-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0261-128"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0261-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c0261-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c0261-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0261-130">**\_ \_ Informazioni driver \_ 2W** (Unicode) e **\_ \_ informazioni driver \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c0261-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="c0261-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0261-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0261-132">Stampa</span><span class="sxs-lookup"><span data-stu-id="c0261-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c0261-133">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="c0261-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c0261-134">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c0261-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="c0261-135">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c0261-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




