---
description: Metodo del costruttore. Il costruttore blocca l'oggetto sezione critico specificato.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Costruttore CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327977"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="4b834-104">Costruttore CAutoLock. CAutoLock</span><span class="sxs-lookup"><span data-stu-id="4b834-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="4b834-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="4b834-105">Constructor method.</span></span> <span data-ttu-id="4b834-106">Il costruttore blocca l'oggetto sezione critico specificato.</span><span class="sxs-lookup"><span data-stu-id="4b834-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b834-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b834-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="4b834-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b834-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b834-109">*Plock*</span><span class="sxs-lookup"><span data-stu-id="4b834-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="4b834-110">Puntatore a un oggetto [**CCritSec**](ccritsec.md) che contiene un oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="4b834-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b834-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b834-111">Requirements</span></span>



| <span data-ttu-id="4b834-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b834-112">Requirement</span></span> | <span data-ttu-id="4b834-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4b834-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b834-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b834-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4b834-115"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b834-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b834-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b834-116">Library</span></span><br/> | <dl> <span data-ttu-id="4b834-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b834-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b834-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b834-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b834-119">**Classe CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="4b834-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




