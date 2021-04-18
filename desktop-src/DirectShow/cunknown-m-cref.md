---
description: Conteggio riferimenti.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Membro CUnknown:: m_cRef (ComBase. h)'
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
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331449"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="a0430-103">Membro cref di CUnknown:: m \_</span><span class="sxs-lookup"><span data-stu-id="a0430-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="a0430-104">Conteggio riferimenti.</span><span class="sxs-lookup"><span data-stu-id="a0430-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0430-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0430-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="a0430-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a0430-106">Remarks</span></span>

<span data-ttu-id="a0430-107">Usare questa variabile membro se si esegue l'override del metodo [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) o [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="a0430-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0430-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0430-108">Requirements</span></span>



| <span data-ttu-id="a0430-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0430-109">Requirement</span></span> | <span data-ttu-id="a0430-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a0430-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0430-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0430-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a0430-112"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0430-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0430-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0430-113">Library</span></span><br/> | <dl> <span data-ttu-id="a0430-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0430-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




