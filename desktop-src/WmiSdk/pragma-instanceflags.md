---
description: Controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233818"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="108cb-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="108cb-103">pragma instanceflags</span></span>

<span data-ttu-id="108cb-104">Il comando per il preprocessore **pragma instanceflags** controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.</span><span class="sxs-lookup"><span data-stu-id="108cb-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="108cb-105">Di seguito viene descritta la sintassi:</span><span class="sxs-lookup"><span data-stu-id="108cb-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="108cb-106">Il *\[ flag \]* deve essere uno degli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="108cb-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="108cb-107">Flag</span><span class="sxs-lookup"><span data-stu-id="108cb-107">Flag</span></span>       | <span data-ttu-id="108cb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="108cb-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="108cb-109">createonly</span><span class="sxs-lookup"><span data-stu-id="108cb-109">createonly</span></span> | <span data-ttu-id="108cb-110">Impedisce al compilatore di modificare le istanze esistenti nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="108cb-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="108cb-111">UpdateOnly</span><span class="sxs-lookup"><span data-stu-id="108cb-111">updateonly</span></span> | <span data-ttu-id="108cb-112">Impedisce al compilatore di creare nuove istanze se non esiste un'istanza specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="108cb-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="108cb-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="108cb-113">Examples</span></span>

<span data-ttu-id="108cb-114">Nell'esempio seguente viene illustrato come utilizzare questo comando.</span><span class="sxs-lookup"><span data-stu-id="108cb-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="108cb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="108cb-115">Requirements</span></span>



| <span data-ttu-id="108cb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="108cb-116">Requirement</span></span> | <span data-ttu-id="108cb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="108cb-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="108cb-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="108cb-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="108cb-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="108cb-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="108cb-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="108cb-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="108cb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="108cb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108cb-123">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="108cb-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




