---
description: Elimina un'istanza esistente di una classe dal repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049645"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="f23ac-103">pragma DeleteInstance</span><span class="sxs-lookup"><span data-stu-id="f23ac-103">pragma deleteinstance</span></span>

<span data-ttu-id="f23ac-104">Il comando **pragma DeleteInstance** Elimina un'istanza esistente di una classe dal repository.</span><span class="sxs-lookup"><span data-stu-id="f23ac-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="f23ac-105">Di seguito viene descritta la sintassi per questo comando:</span><span class="sxs-lookup"><span data-stu-id="f23ac-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="f23ac-106">*InstanceID* è un identificatore univoco dell'istanza eliminata dal compilatore MOF dallo spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="f23ac-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="f23ac-107">Il *\[ flag \]* deve essere uno degli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f23ac-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="f23ac-108">Flag</span><span class="sxs-lookup"><span data-stu-id="f23ac-108">Flag</span></span>   | <span data-ttu-id="f23ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f23ac-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23ac-110">fail</span><span class="sxs-lookup"><span data-stu-id="f23ac-110">fail</span></span>   | <span data-ttu-id="f23ac-111">Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository.</span><span class="sxs-lookup"><span data-stu-id="f23ac-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="f23ac-112">nofail</span><span class="sxs-lookup"><span data-stu-id="f23ac-112">nofail</span></span> | <span data-ttu-id="f23ac-113">Determina la continuazione del compilatore MOF anche se la classe non esiste già.</span><span class="sxs-lookup"><span data-stu-id="f23ac-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="f23ac-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="f23ac-114">Examples</span></span>

<span data-ttu-id="f23ac-115">Nell'esempio seguente viene illustrato come utilizzare questo comando.</span><span class="sxs-lookup"><span data-stu-id="f23ac-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="f23ac-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f23ac-116">Requirements</span></span>



| <span data-ttu-id="f23ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23ac-117">Requirement</span></span> | <span data-ttu-id="f23ac-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f23ac-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f23ac-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f23ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f23ac-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f23ac-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f23ac-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f23ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f23ac-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f23ac-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f23ac-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f23ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23ac-124">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="f23ac-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




