---
title: Struttura RECORD_HEADER
description: Intestazione del record utilizzata dalla voce del \_ registro delle modifiche e dalle strutture dell'intestazione del log delle \_ modifiche \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Ripristino del sistema della struttura RECORD_HEADER
- Ripristino del sistema del puntatore della struttura PRECORD_HEADER
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478292"
---
# <a name="record_header-structure"></a><span data-ttu-id="48366-105">Struttura di intestazione del RECORD \_</span><span class="sxs-lookup"><span data-stu-id="48366-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="48366-106">\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="48366-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="48366-107">Intestazione del record utilizzata dalla [**voce del \_ registro \_ delle modifiche**](change-log-entry.md) e dalle strutture dell' [**\_ \_ intestazione del log delle modifiche**](change-log-header.md) .</span><span class="sxs-lookup"><span data-stu-id="48366-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="48366-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48366-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="48366-109">Members</span><span class="sxs-lookup"><span data-stu-id="48366-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="48366-110">**dwRecordSize**</span><span class="sxs-lookup"><span data-stu-id="48366-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="48366-111">Dimensioni totali del record, inclusa l'intestazione, in byte.</span><span class="sxs-lookup"><span data-stu-id="48366-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="48366-112">**dwRecordType**</span><span class="sxs-lookup"><span data-stu-id="48366-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="48366-113">Tipo di record.</span><span class="sxs-lookup"><span data-stu-id="48366-113">The record type.</span></span> <span data-ttu-id="48366-114">Questo membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="48366-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="48366-115">Valore</span><span class="sxs-lookup"><span data-stu-id="48366-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="48366-116">Significato</span><span class="sxs-lookup"><span data-stu-id="48366-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="48366-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48366-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="48366-118">Il record è l'intestazione del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="48366-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48366-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="48366-120">Il record è l'intestazione di una voce del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="48366-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="48366-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="48366-122">I dati sono il percorso del volume per la voce del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="48366-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="48366-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="48366-124">I dati sono il percorso del file per la voce del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="48366-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="48366-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="48366-126">I dati vengono utilizzati durante la ridenominazione delle voci del log delle modifiche. Questo percorso è la posizione in cui è archiviato il file rinominato.</span><span class="sxs-lookup"><span data-stu-id="48366-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="48366-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="48366-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="48366-128">I dati sono il nome del file di backup utilizzato per ripristinare la voce del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="48366-129">I file di backup si trovano nella cartella RP *n* .</span><span class="sxs-lookup"><span data-stu-id="48366-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="48366-130">Il nome del file ha il formato seguente: un *xxxxxxx*. *ext*, dove *xxxxxxx* è un numero a sette cifre ed *ext* è l'estensione del nome di file.</span><span class="sxs-lookup"><span data-stu-id="48366-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="48366-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="48366-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="48366-132">I dati sono un ACL.</span><span class="sxs-lookup"><span data-stu-id="48366-132">The data is an ACL.</span></span> <span data-ttu-id="48366-133">Il formato dei dati è una struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="48366-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="48366-134">Questo valore non può essere superiore a 8.192 byte.</span><span class="sxs-lookup"><span data-stu-id="48366-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="48366-135">Per specificare un valore maggiore di 8.192 byte, usare il membro **RecordTypeAclFile** .</span><span class="sxs-lookup"><span data-stu-id="48366-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="48366-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="48366-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="48366-137">I dati sono il nome del file ACL usato per archiviare l'ACL.</span><span class="sxs-lookup"><span data-stu-id="48366-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="48366-138">I file ACL si trovano nella cartella RP *n* .</span><span class="sxs-lookup"><span data-stu-id="48366-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="48366-139">Il nome del file ha il formato seguente: S *xxxxxxx*. ACL, dove *xxxxxxx* è un numero a sette cifre.</span><span class="sxs-lookup"><span data-stu-id="48366-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="48366-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="48366-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="48366-141">I dati sono informazioni di debug per la voce del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="48366-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="48366-142">Il formato dei dati è una struttura di **\_ informazioni di \_ debug \_ del log SR** .</span><span class="sxs-lookup"><span data-stu-id="48366-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="48366-143">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="48366-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="48366-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="48366-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="48366-145">I dati sono il nome breve del file di backup.</span><span class="sxs-lookup"><span data-stu-id="48366-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48366-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="48366-146">Remarks</span></span>

<span data-ttu-id="48366-147">La struttura delle **\_ informazioni di \_ debug \_ del log SR** è definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="48366-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="48366-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48366-148">Requirements</span></span>



| <span data-ttu-id="48366-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="48366-149">Requirement</span></span> | <span data-ttu-id="48366-150">Valore</span><span class="sxs-lookup"><span data-stu-id="48366-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48366-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48366-151">Minimum supported client</span></span><br/> | <span data-ttu-id="48366-152">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="48366-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48366-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48366-153">Minimum supported server</span></span><br/> | <span data-ttu-id="48366-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="48366-154">None supported</span></span><br/>                            |
| <span data-ttu-id="48366-155">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="48366-155">End of client support</span></span><br/>    | <span data-ttu-id="48366-156">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="48366-156">Windows XP with SP2</span></span><br/>                       |



 

