---
description: Membro CUnknown::m_cRef - Conteggio dei riferimenti.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: Membro CUnknown::m_cRef (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084579"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="6cad4-103">Membro cRef CUnknown::m \_</span><span class="sxs-lookup"><span data-stu-id="6cad4-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="6cad4-104">Conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="6cad4-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cad4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6cad4-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="6cad4-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6cad4-106">Remarks</span></span>

<span data-ttu-id="6cad4-107">Usare questa variabile membro se si esegue l'override [**del metodo NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) [**o NonDelegatingRelease.**](cunknown-nondelegatingrelease.md)</span><span class="sxs-lookup"><span data-stu-id="6cad4-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cad4-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cad4-108">Requirements</span></span>



| <span data-ttu-id="6cad4-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cad4-109">Requirement</span></span> | <span data-ttu-id="6cad4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6cad4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cad4-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cad4-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6cad4-112"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cad4-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cad4-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="6cad4-113">Library</span></span><br/> | <dl> <span data-ttu-id="6cad4-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cad4-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




