---
description: Elimina una classe esistente e le relative istanze dal repository.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885234"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="d9da8-103">pragma deleteclass</span><span class="sxs-lookup"><span data-stu-id="d9da8-103">pragma deleteclass</span></span>

<span data-ttu-id="d9da8-104">Il comando per il preprocessore **pragma deleteclass** Elimina una classe esistente e le relative istanze dal repository.</span><span class="sxs-lookup"><span data-stu-id="d9da8-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="d9da8-105">Di seguito viene descritta la sintassi:</span><span class="sxs-lookup"><span data-stu-id="d9da8-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="d9da8-106">*NomeClasse* è il nome della classe che il compilatore MOF Elimina dallo spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="d9da8-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="d9da8-107">Il *\[ flag \]* deve essere uno degli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9da8-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="d9da8-108">Flag</span><span class="sxs-lookup"><span data-stu-id="d9da8-108">Flag</span></span>   | <span data-ttu-id="d9da8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9da8-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9da8-110">fail</span><span class="sxs-lookup"><span data-stu-id="d9da8-110">fail</span></span>   | <span data-ttu-id="d9da8-111">Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository.</span><span class="sxs-lookup"><span data-stu-id="d9da8-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="d9da8-112">nofail</span><span class="sxs-lookup"><span data-stu-id="d9da8-112">nofail</span></span> | <span data-ttu-id="d9da8-113">Determina la continuazione del compilatore MOF anche se la classe non esiste già.</span><span class="sxs-lookup"><span data-stu-id="d9da8-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="d9da8-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="d9da8-114">Examples</span></span>

<span data-ttu-id="d9da8-115">Nell'esempio seguente viene illustrato come utilizzare questo comando.</span><span class="sxs-lookup"><span data-stu-id="d9da8-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="d9da8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9da8-116">Requirements</span></span>



| <span data-ttu-id="d9da8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9da8-117">Requirement</span></span> | <span data-ttu-id="d9da8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d9da8-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d9da8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9da8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9da8-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d9da8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9da8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9da8-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9da8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9da8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9da8-124">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="d9da8-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




