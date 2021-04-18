---
description: Il metodo CheckBitFields convalida le maschere dei colori in una struttura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Metodo CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325325"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="efbbc-103">CImageDisplay. CheckBitFields, metodo</span><span class="sxs-lookup"><span data-stu-id="efbbc-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="efbbc-104">Il `CheckBitFields` metodo convalida le maschere dei colori in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="efbbc-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbbc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efbbc-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="efbbc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efbbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbbc-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="efbbc-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="efbbc-108">Puntatore a una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="efbbc-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbbc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efbbc-109">Return value</span></span>

<span data-ttu-id="efbbc-110">Restituisce **true** se le maschere dei colori sono valide o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efbbc-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efbbc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="efbbc-111">Remarks</span></span>

<span data-ttu-id="efbbc-112">Questo metodo verifica che la maschera di colore per ogni componente del colore sia compresa tra uno e otto bit e che ogni maschera di colore sia una sequenza di bit contigua.</span><span class="sxs-lookup"><span data-stu-id="efbbc-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="efbbc-113">Chiamare questo metodo solo quando il membro di **biCompression** è impostato su bi \_ campi.</span><span class="sxs-lookup"><span data-stu-id="efbbc-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbbc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbbc-114">Requirements</span></span>



| <span data-ttu-id="efbbc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbbc-115">Requirement</span></span> | <span data-ttu-id="efbbc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="efbbc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbbc-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efbbc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="efbbc-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efbbc-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efbbc-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="efbbc-119">Library</span></span><br/> | <dl> <span data-ttu-id="efbbc-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efbbc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbbc-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efbbc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbbc-122">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="efbbc-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




