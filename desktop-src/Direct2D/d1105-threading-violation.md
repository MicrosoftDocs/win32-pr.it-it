---
title: Violazione Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Un'interfaccia a thread di noleggio è stata accessibile simultaneamente da più thread.
keywords:
- Direct2D violazione Threading D1105
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334280"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="72b75-104">D1105: violazione Threading</span><span class="sxs-lookup"><span data-stu-id="72b75-104">D1105: Threading Violation</span></span>

<span data-ttu-id="72b75-105">Un'interfaccia di interfaccia a thread \[  \] di noleggio è stata accessibile simultaneamente da più thread.</span><span class="sxs-lookup"><span data-stu-id="72b75-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="72b75-106">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="72b75-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="72b75-107"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="72b75-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="72b75-108">Indirizzo dell'interfaccia accessibile da più thread.</span><span class="sxs-lookup"><span data-stu-id="72b75-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="72b75-109">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="72b75-109">Possible Causes</span></span>

<span data-ttu-id="72b75-110">Uso di un'istanza di oggetto dalla stessa Factory a thread singolo da due thread diversi.</span><span class="sxs-lookup"><span data-stu-id="72b75-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




