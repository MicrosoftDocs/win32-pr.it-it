---
description: Puntatore a una funzione che crea un'istanza dell'oggetto.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntatore alla funzione LPFNNewCOMObject (ComBase. h)
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
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330383"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="6a6cc-103">Puntatore alla funzione LPFNNewCOMObject</span><span class="sxs-lookup"><span data-stu-id="6a6cc-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="6a6cc-104">Puntatore a una funzione che crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6a6cc-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a6cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a6cc-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6a6cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a6cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a6cc-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="6a6cc-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="6a6cc-108">Puntatore all'interfaccia **IUnknown** dell'oggetto che aggrega il nuovo oggetto, se presente.</span><span class="sxs-lookup"><span data-stu-id="6a6cc-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="6a6cc-109">Questo puntatore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6a6cc-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a6cc-110">*PHR*</span><span class="sxs-lookup"><span data-stu-id="6a6cc-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6a6cc-111">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a6cc-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6a6cc-112">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="6a6cc-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a6cc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a6cc-113">Return value</span></span>

<span data-ttu-id="6a6cc-114">Restituisce un puntatore a una nuova istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6a6cc-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a6cc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a6cc-115">Requirements</span></span>



| <span data-ttu-id="6a6cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a6cc-116">Requirement</span></span> | <span data-ttu-id="6a6cc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6a6cc-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6cc-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a6cc-118">Header</span></span><br/> | <dl> <span data-ttu-id="6a6cc-119"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a6cc-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a6cc-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a6cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a6cc-121">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="6a6cc-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




