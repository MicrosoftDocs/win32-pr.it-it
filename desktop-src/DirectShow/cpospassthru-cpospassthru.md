---
description: Metodo del costruttore.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Costruttore CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303784"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="d1837-103">Costruttore CPosPassThru. CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="d1837-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="d1837-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d1837-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1837-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1837-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="d1837-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1837-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d1837-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d1837-108">Puntatore al nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="d1837-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="d1837-109">Allocare questo parametro nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="d1837-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="d1837-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d1837-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d1837-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d1837-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d1837-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d1837-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d1837-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="d1837-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1837-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="d1837-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d1837-115">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1837-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d1837-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="d1837-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d1837-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="d1837-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d1837-118">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="d1837-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



