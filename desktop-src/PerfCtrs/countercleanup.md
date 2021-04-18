---
description: Rimuove la registrazione dei provider.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312182"
---
# <a name="countercleanup-function"></a><span data-ttu-id="8c0ed-103">CounterCleanup (funzione)</span><span class="sxs-lookup"><span data-stu-id="8c0ed-103">CounterCleanup function</span></span>

<span data-ttu-id="8c0ed-104">Rimuove la registrazione del provider.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c0ed-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="8c0ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c0ed-106">Parameters</span></span>

<span data-ttu-id="8c0ed-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c0ed-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c0ed-108">Return value</span></span>

<span data-ttu-id="8c0ed-109">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0ed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c0ed-110">Remarks</span></span>

<span data-ttu-id="8c0ed-111">Il provider chiama questa funzione.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-111">Your provider calls this function.</span></span> <span data-ttu-id="8c0ed-112">La funzione chiama la funzione [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) per rimuovere la registrazione del provider.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="8c0ed-113">Lo strumento [**CTRPP**](ctrpp.md) genera questa funzione inline quando si specifica l'argomento **-o** .</span><span class="sxs-lookup"><span data-stu-id="8c0ed-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="8c0ed-114">Il nome della funzione include una stringa di *prefisso* se si specifica l'argomento **-Prefix** , ad esempio **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="8c0ed-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0ed-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c0ed-115">Requirements</span></span>



| <span data-ttu-id="8c0ed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c0ed-116">Requirement</span></span> | <span data-ttu-id="8c0ed-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8c0ed-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8c0ed-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c0ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0ed-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8c0ed-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8c0ed-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c0ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0ed-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c0ed-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




