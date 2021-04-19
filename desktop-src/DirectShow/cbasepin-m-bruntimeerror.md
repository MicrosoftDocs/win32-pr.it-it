---
description: Flag che indica se si è verificato un errore in fase di esecuzione.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membro CBasePin:: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332869"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="1c02b-103">Membro bRunTimeError di CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="1c02b-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="1c02b-104">Flag che indica se si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1c02b-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c02b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c02b-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="1c02b-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1c02b-106">Remarks</span></span>

<span data-ttu-id="1c02b-107">Il valore predefinito di questo flag è **false**.</span><span class="sxs-lookup"><span data-stu-id="1c02b-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="1c02b-108">Impostare il flag su **true** se si verifica un errore in fase di esecuzione durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="1c02b-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="1c02b-109">Il metodo [**CBasePin:: inactive**](cbasepin-inactive.md) Reimposta il flag su **false**.</span><span class="sxs-lookup"><span data-stu-id="1c02b-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c02b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c02b-110">Requirements</span></span>



| <span data-ttu-id="1c02b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c02b-111">Requirement</span></span> | <span data-ttu-id="1c02b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1c02b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c02b-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c02b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1c02b-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c02b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1c02b-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c02b-115">Library</span></span><br/> | <dl> <span data-ttu-id="1c02b-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c02b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c02b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c02b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c02b-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="1c02b-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




