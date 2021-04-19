---
description: Il metodo CountPrefixBits calcola il numero di bit zero all'inizio di un campo di bit specificato.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Metodo CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330230"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="9778c-103">CImageDisplay. CountPrefixBits, metodo</span><span class="sxs-lookup"><span data-stu-id="9778c-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="9778c-104">Il `CountPrefixBits` metodo calcola il numero di bit zero all'inizio di un campo di bit specificato.</span><span class="sxs-lookup"><span data-stu-id="9778c-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="9778c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9778c-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="9778c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9778c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9778c-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="9778c-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="9778c-108">Specifica un campo di bit come valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9778c-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9778c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9778c-109">Return value</span></span>

<span data-ttu-id="9778c-110">Restituisce il numero di bit zero che si verificano prima del primo bit o 0x80000000 se tutti i bit sono zero.</span><span class="sxs-lookup"><span data-stu-id="9778c-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9778c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9778c-111">Remarks</span></span>

<span data-ttu-id="9778c-112">Questo metodo è utile per lavorare con le maschere dei colori nelle strutture [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="9778c-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9778c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9778c-113">Requirements</span></span>



| <span data-ttu-id="9778c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9778c-114">Requirement</span></span> | <span data-ttu-id="9778c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9778c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9778c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9778c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9778c-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9778c-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9778c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="9778c-118">Library</span></span><br/> | <dl> <span data-ttu-id="9778c-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9778c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9778c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9778c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9778c-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="9778c-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




