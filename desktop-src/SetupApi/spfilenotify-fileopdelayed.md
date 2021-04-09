---
description: La \_ notifica SPFILENOTIFY FILEOPDELAYED viene inviata da SetupInstallFileEx o SetupCommitFileQueue a una routine di callback quando un'operazione su file è stata posticipata perché il file è in uso. L'operazione verrà elaborata al successivo riavvio del sistema.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Messaggio SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880837"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="c71f0-104">\_Messaggio SPFILENOTIFY FILEOPDELAYED</span><span class="sxs-lookup"><span data-stu-id="c71f0-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="c71f0-105">La notifica **SPFILENOTIFY \_ FILEOPDELAYED** viene inviata da [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) a una routine di callback quando un'operazione su file è stata posticipata perché il file è in uso.</span><span class="sxs-lookup"><span data-stu-id="c71f0-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="c71f0-106">L'operazione verrà elaborata al successivo riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c71f0-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="c71f0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c71f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71f0-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="c71f0-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="c71f0-109">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="c71f0-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="c71f0-110">Se l'operazione ritardata è un'operazione di copia dei file, la struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c71f0-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="c71f0-111">Membro filePaths</span><span class="sxs-lookup"><span data-stu-id="c71f0-111">FILEPATHS member</span></span> | <span data-ttu-id="c71f0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c71f0-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="c71f0-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="c71f0-113">**Win32Error**</span></span>   | <span data-ttu-id="c71f0-114">Nessun \_ errore</span><span class="sxs-lookup"><span data-stu-id="c71f0-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="c71f0-115">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c71f0-115">**Flags**</span></span>        | <span data-ttu-id="c71f0-116">copia di FILEOP \_</span><span class="sxs-lookup"><span data-stu-id="c71f0-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="c71f0-117">**Origine**</span><span class="sxs-lookup"><span data-stu-id="c71f0-117">**Source**</span></span>       | <span data-ttu-id="c71f0-118">Percorso completo del file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c71f0-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="c71f0-119">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="c71f0-119">**Target**</span></span>       | <span data-ttu-id="c71f0-120">Percorso completo del file di destinazione effettivo.</span><span class="sxs-lookup"><span data-stu-id="c71f0-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="c71f0-121">Il file temporaneo verrà copiato nella directory di destinazione al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c71f0-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="c71f0-122">Le funzioni di installazione generano automaticamente un percorso per il file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c71f0-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="c71f0-123">Se l'operazione ritardata è un'operazione di eliminazione di file, la struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c71f0-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="c71f0-124">Membro filePaths</span><span class="sxs-lookup"><span data-stu-id="c71f0-124">FILEPATHS member</span></span> | <span data-ttu-id="c71f0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c71f0-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="c71f0-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="c71f0-126">**Win32Error**</span></span>   | <span data-ttu-id="c71f0-127">Nessun \_ errore</span><span class="sxs-lookup"><span data-stu-id="c71f0-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="c71f0-128">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c71f0-128">**Flags**</span></span>        | <span data-ttu-id="c71f0-129">eliminazione di FILEOP \_</span><span class="sxs-lookup"><span data-stu-id="c71f0-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="c71f0-130">**Origine**</span><span class="sxs-lookup"><span data-stu-id="c71f0-130">**Source**</span></span>       | <span data-ttu-id="c71f0-131">NULL</span><span class="sxs-lookup"><span data-stu-id="c71f0-131">NULL</span></span>                                 |
| <span data-ttu-id="c71f0-132">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="c71f0-132">**Target**</span></span>       | <span data-ttu-id="c71f0-133">Percorso completo del file da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c71f0-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c71f0-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="c71f0-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="c71f0-135">Non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c71f0-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71f0-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c71f0-136">Return value</span></span>

<span data-ttu-id="c71f0-137">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c71f0-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71f0-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c71f0-138">Requirements</span></span>



| <span data-ttu-id="c71f0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c71f0-139">Requirement</span></span> | <span data-ttu-id="c71f0-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c71f0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c71f0-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c71f0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c71f0-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c71f0-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c71f0-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c71f0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c71f0-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c71f0-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c71f0-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c71f0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71f0-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71f0-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71f0-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c71f0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71f0-148">Overview</span><span class="sxs-lookup"><span data-stu-id="c71f0-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="c71f0-149">Notifications</span><span class="sxs-lookup"><span data-stu-id="c71f0-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c71f0-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="c71f0-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="c71f0-151">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="c71f0-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="c71f0-152">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="c71f0-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="c71f0-153">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="c71f0-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="c71f0-154">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="c71f0-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




