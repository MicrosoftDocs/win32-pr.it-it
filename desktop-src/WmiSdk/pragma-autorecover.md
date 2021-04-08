---
description: Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma autocover
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968188"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="f38f6-103">pragma autocover</span><span class="sxs-lookup"><span data-stu-id="f38f6-103">pragma autorecover</span></span>

<span data-ttu-id="f38f6-104">Il comando **pragma autocover** preprocessore consente di aggiungere un file MOF all'elenco di file compilati durante il ripristino del repository.</span><span class="sxs-lookup"><span data-stu-id="f38f6-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="f38f6-105">L'elenco dei file MOF di **autocover** è archiviato in questa chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="f38f6-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="f38f6-106">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autocover file MOF**</span><span class="sxs-lookup"><span data-stu-id="f38f6-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="f38f6-107">WMI controlla l'integrità del repository WMI quando il sistema operativo avvia WMI.</span><span class="sxs-lookup"><span data-stu-id="f38f6-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="f38f6-108">Se il repository è danneggiato, WMI ricompila automaticamente il repository e ricompila tutti i file MOF elencati in questa chiave nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f38f6-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="f38f6-109">Di seguito viene descritta la sintassi per il comando pragma autocover:</span><span class="sxs-lookup"><span data-stu-id="f38f6-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="f38f6-110">Quando si usa questo comando, è tuttavia necessario osservare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f38f6-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="f38f6-111">WMI non è in grado di ripristinare i file MOF presenti in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="f38f6-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="f38f6-112">Pertanto, i file MOF elencati in questa chiave del registro di sistema devono trovarsi nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="f38f6-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="f38f6-113">Non è possibile specificare le opzioni della riga di comando utilizzate dal compilatore MOF quando WMI recupera un file MOF.</span><span class="sxs-lookup"><span data-stu-id="f38f6-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="f38f6-114">Pertanto, è necessario includere i comandi [pragma](-pragma.md) nel file MOF che rendono inutili le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f38f6-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="f38f6-115">Nell'esempio seguente viene descritta un'opzione della riga di comando comune che WMI non utilizza quando si recupera un file MOF da questa chiave del registro di sistema: **mofcomp-N:root \\ test mymof. mof**</span><span class="sxs-lookup"><span data-stu-id="f38f6-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="f38f6-116">È tuttavia possibile specificare lo spazio dei nomi utilizzando un comando [pragma](-pragma.md) nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="f38f6-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="f38f6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f38f6-117">Requirements</span></span>



| <span data-ttu-id="f38f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f38f6-118">Requirement</span></span> | <span data-ttu-id="f38f6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f38f6-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f38f6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f38f6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f38f6-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f38f6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f38f6-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f38f6-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f38f6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f38f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38f6-125">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="f38f6-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




