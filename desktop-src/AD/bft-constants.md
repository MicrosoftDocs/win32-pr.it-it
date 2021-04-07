---
title: Costanti BFT (ntdsbcli. h)
description: Le costanti BFT vengono usate come flag di bit per identificare tipi di file diversi in un backup Active Directory Domain Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964064"
---
# <a name="bft-constants"></a><span data-ttu-id="59283-103">Costanti BFT</span><span class="sxs-lookup"><span data-stu-id="59283-103">BFT Constants</span></span>

<span data-ttu-id="59283-104">Le costanti BFT vengono usate come flag di bit per identificare tipi di file diversi in un backup Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="59283-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="59283-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_directory log \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="59283-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-106">0x20</span><span class="sxs-lookup"><span data-stu-id="59283-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="59283-107">Il file appartiene alla directory log.</span><span class="sxs-lookup"><span data-stu-id="59283-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_directory del database BFT \_**</span><span class="sxs-lookup"><span data-stu-id="59283-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-109">0x40</span><span class="sxs-lookup"><span data-stu-id="59283-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="59283-110">Il file appartiene alla directory del database.</span><span class="sxs-lookup"><span data-stu-id="59283-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_directory BFT**</span><span class="sxs-lookup"><span data-stu-id="59283-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-112">0x80</span><span class="sxs-lookup"><span data-stu-id="59283-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="59283-113">Il percorso specificato è una directory e non un nome file.</span><span class="sxs-lookup"><span data-stu-id="59283-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_log BFT**</span><span class="sxs-lookup"><span data-stu-id="59283-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-115">0x21</span><span class="sxs-lookup"><span data-stu-id="59283-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="59283-116">Specifica un file di log che appartiene alla directory dei log.</span><span class="sxs-lookup"><span data-stu-id="59283-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_dir BFT log \_**</span><span class="sxs-lookup"><span data-stu-id="59283-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-118">0x22</span><span class="sxs-lookup"><span data-stu-id="59283-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="59283-119">Il file è il percorso della directory dei log.</span><span class="sxs-lookup"><span data-stu-id="59283-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir del checkpoint BFT \_**</span><span class="sxs-lookup"><span data-stu-id="59283-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-121">0x23</span><span class="sxs-lookup"><span data-stu-id="59283-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="59283-122">Il file è il percorso della directory del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="59283-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_database NTDS \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="59283-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-124">0x44</span><span class="sxs-lookup"><span data-stu-id="59283-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="59283-125">Il file è un database del servizio directory che appartiene alla directory del database.</span><span class="sxs-lookup"><span data-stu-id="59283-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_file patch \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="59283-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-127">0x25</span><span class="sxs-lookup"><span data-stu-id="59283-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="59283-128">Il file è un file di patch che appartiene alla directory dei log.</span><span class="sxs-lookup"><span data-stu-id="59283-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59283-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="59283-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59283-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="59283-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="59283-131">Il file non può essere riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="59283-131">The file cannot be recognized.</span></span> <span data-ttu-id="59283-132">Il file non coincide con i nomi file e i tipi di file noti.</span><span class="sxs-lookup"><span data-stu-id="59283-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59283-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59283-133">Requirements</span></span>



| <span data-ttu-id="59283-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="59283-134">Requirement</span></span> | <span data-ttu-id="59283-135">Valore</span><span class="sxs-lookup"><span data-stu-id="59283-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59283-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59283-136">Minimum supported client</span></span><br/> | <span data-ttu-id="59283-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59283-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="59283-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59283-138">Minimum supported server</span></span><br/> | <span data-ttu-id="59283-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59283-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="59283-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59283-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="59283-141"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="59283-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





