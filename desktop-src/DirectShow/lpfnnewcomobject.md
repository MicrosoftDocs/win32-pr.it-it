---
description: "Puntatore a funzione LPFNNewCOMObject: puntatore a una funzione che crea un'istanza dell'oggetto."
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntatore a funzione LPFNNewCOMObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116529"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="97fc7-103">Puntatore alla funzione LPFNNewCOMObject</span><span class="sxs-lookup"><span data-stu-id="97fc7-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="97fc7-104">Puntatore a una funzione che crea un'istanza dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="97fc7-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fc7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97fc7-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="97fc7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97fc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97fc7-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="97fc7-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="97fc7-108">Puntatore **all'interfaccia IUnknown** dell'oggetto che aggrega il nuovo oggetto, se presente.</span><span class="sxs-lookup"><span data-stu-id="97fc7-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="97fc7-109">Questo puntatore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="97fc7-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97fc7-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="97fc7-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="97fc7-111">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="97fc7-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="97fc7-112">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="97fc7-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97fc7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97fc7-113">Return value</span></span>

<span data-ttu-id="97fc7-114">Restituisce un puntatore a una nuova istanza dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="97fc7-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fc7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97fc7-115">Requirements</span></span>



| <span data-ttu-id="97fc7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="97fc7-116">Requirement</span></span> | <span data-ttu-id="97fc7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="97fc7-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fc7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97fc7-118">Header</span></span><br/> | <dl> <span data-ttu-id="97fc7-119"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="97fc7-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97fc7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97fc7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fc7-121">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="97fc7-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




