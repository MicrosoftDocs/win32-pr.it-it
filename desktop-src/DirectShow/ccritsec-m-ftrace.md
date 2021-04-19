---
description: Valore booleano che specifica se tracciare il blocco.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membro CCritSec:: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332646"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="62a15-103">Membro fTrace di CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="62a15-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="62a15-104">Valore booleano che specifica se tracciare il blocco.</span><span class="sxs-lookup"><span data-stu-id="62a15-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62a15-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="62a15-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="62a15-106">Remarks</span></span>

<span data-ttu-id="62a15-107">Questa variabile membro viene definita solo nella versione di debug della classe di base.</span><span class="sxs-lookup"><span data-stu-id="62a15-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="62a15-108">Se il valore è **true**, una traccia dello stato di blocco viene scritta nel log di debug.</span><span class="sxs-lookup"><span data-stu-id="62a15-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="62a15-109">(È necessario che la registrazione di debug per le sezioni critiche sia attiva). Per ulteriori informazioni, vedere [**DbgLockTrace**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="62a15-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a15-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62a15-110">Requirements</span></span>



| <span data-ttu-id="62a15-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a15-111">Requirement</span></span> | <span data-ttu-id="62a15-112">Valore</span><span class="sxs-lookup"><span data-stu-id="62a15-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a15-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62a15-113">Header</span></span><br/>  | <dl> <span data-ttu-id="62a15-114"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62a15-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="62a15-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="62a15-115">Library</span></span><br/> | <dl> <span data-ttu-id="62a15-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="62a15-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a15-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62a15-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a15-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="62a15-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




