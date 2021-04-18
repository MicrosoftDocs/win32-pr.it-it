---
description: Il metodo CheckVideoType controlla se un formato VIDEOINFO specificato è compatibile con il formato di visualizzazione.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Metodo CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331642"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="2ce82-103">CImageDisplay. CheckVideoType, metodo</span><span class="sxs-lookup"><span data-stu-id="2ce82-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="2ce82-104">Il `CheckVideoType` metodo controlla se un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) specificato è compatibile con il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ce82-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ce82-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="2ce82-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ce82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce82-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="2ce82-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2ce82-108">Puntatore a una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="2ce82-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce82-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ce82-109">Return value</span></span>

<span data-ttu-id="2ce82-110">Restituisce \_ OK se il formato è compatibile o e \_ INVALIDARG in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2ce82-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce82-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ce82-111">Remarks</span></span>

<span data-ttu-id="2ce82-112">Questo metodo restituisce \_ OK se è possibile visualizzare facilmente il tipo proposto sotto le impostazioni di visualizzazione correnti.</span><span class="sxs-lookup"><span data-stu-id="2ce82-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce82-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ce82-113">Requirements</span></span>



| <span data-ttu-id="2ce82-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce82-114">Requirement</span></span> | <span data-ttu-id="2ce82-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2ce82-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce82-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ce82-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce82-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce82-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2ce82-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ce82-118">Library</span></span><br/> | <dl> <span data-ttu-id="2ce82-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce82-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce82-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ce82-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce82-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="2ce82-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




