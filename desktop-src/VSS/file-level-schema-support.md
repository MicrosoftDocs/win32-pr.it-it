---
description: I writer possono ottimizzare le prestazioni dei vari tipi di backup a livello di set di file indicando tramite un tipo di backup delle specifiche di file, indicato da una maschera di bit o bit per bit dei membri dell' \_ enumerazione del tipo di backup delle specifiche del file VSS \_ \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Supporto dello schema a livello di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968487"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="61efe-103">Supporto dello schema a livello di file</span><span class="sxs-lookup"><span data-stu-id="61efe-103">File Level Schema Support</span></span>

<span data-ttu-id="61efe-104">I writer possono ottimizzare le prestazioni dei vari tipi di backup a livello di [*set di file*](vssgloss-f.md) indicando tramite un tipo di backup delle specifiche di file, indicato da una maschera di bit o bit per bit dei membri dell'enumerazione del [**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .</span><span class="sxs-lookup"><span data-stu-id="61efe-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="61efe-105">Per i tipi di backup specificati, il writer indica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="61efe-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="61efe-106">Indica se sarà necessario eseguire la copia shadow del volume per eseguire correttamente il backup di un set di file.</span><span class="sxs-lookup"><span data-stu-id="61efe-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="61efe-107">Ad esempio, se i file in un set di file non vengono aperti esclusivamente dal writer e possono garantire che sia stabile, non è necessaria una copia shadow.</span><span class="sxs-lookup"><span data-stu-id="61efe-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="61efe-108">Se il richiedente deve eseguire il backup in modo tale che, indipendentemente dall'ora dell'Ultima modifica o da altri problemi, la versione dei file del set di file corrente al backup verrà ripristinata.</span><span class="sxs-lookup"><span data-stu-id="61efe-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="61efe-109">In genere, ciò significa che il set di file viene copiato come parte del backup.</span><span class="sxs-lookup"><span data-stu-id="61efe-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="61efe-110">I valori del [**\_ tipo di \_ \_ backup delle \_ specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che indicano il requisito della copia shadow sono:</span><span class="sxs-lookup"><span data-stu-id="61efe-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="61efe-111">VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari</span><span class="sxs-lookup"><span data-stu-id="61efe-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-112">\_ \_ snapshot completo VSS \_ FSBT \_ necessario</span><span class="sxs-lookup"><span data-stu-id="61efe-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-113">\_ \_ snapshot differenziale FSBT VSS \_ \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="61efe-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-114">\_ \_ snapshot incrementale FSBT \_ VSS \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="61efe-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-115">\_snapshot del \_ log FSBT VSS \_ \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="61efe-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="61efe-116">I valori del [**\_ tipo di \_ \_ backup delle \_ specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che indicano la necessità di eseguire il backup di un file sono:</span><span class="sxs-lookup"><span data-stu-id="61efe-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="61efe-117">VSS \_ FSBT \_ tutti i \_ backup \_ necessari</span><span class="sxs-lookup"><span data-stu-id="61efe-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-118">\_ \_ backup completo VSS \_ FSBT \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="61efe-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-119">è \_ \_ necessario il \_ backup DIFFERENZIAle FSBT VSS \_</span><span class="sxs-lookup"><span data-stu-id="61efe-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-120">è \_ \_ necessario il backup incrementale FSBT VSS \_ \_</span><span class="sxs-lookup"><span data-stu-id="61efe-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="61efe-121">\_backup del \_ log FSBT VSS \_ \_ obbligatorio</span><span class="sxs-lookup"><span data-stu-id="61efe-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="61efe-122">Per impostazione predefinita, i set di file sono contrassegnati con un tipo di backup della specifica del file VSS \_ FSBT \_ tutti i \_ backup \_ necessari \| VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari, ovvero una copia shadow è sempre necessaria per gestire i file del set di file e che i file devono essere copiati in tutti i tipi di backup.</span><span class="sxs-lookup"><span data-stu-id="61efe-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



