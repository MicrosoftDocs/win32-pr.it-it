---
description: Il metodo RefreshDisplayType aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Metodo CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329382"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="692f2-103">CImageDisplay. RefreshDisplayType, metodo</span><span class="sxs-lookup"><span data-stu-id="692f2-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="692f2-104">Il `RefreshDisplayType` metodo aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata.</span><span class="sxs-lookup"><span data-stu-id="692f2-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="692f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="692f2-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="692f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="692f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692f2-107">*szDeviceName*</span><span class="sxs-lookup"><span data-stu-id="692f2-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="692f2-108">Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI.</span><span class="sxs-lookup"><span data-stu-id="692f2-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="692f2-109">Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="692f2-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692f2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="692f2-110">Return value</span></span>

<span data-ttu-id="692f2-111">Restituisce \_ OK se ha esito positivo o se l'operazione ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="692f2-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="692f2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="692f2-112">Remarks</span></span>

<span data-ttu-id="692f2-113">Questo metodo inizializza il membro di **\_ visualizzazione m** in un tipo video che corrisponde alla modalità di visualizzazione sul dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="692f2-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="692f2-114">Chiamare questo metodo ogni volta che \_ viene ricevuto un messaggio WM DISPLAYCHANGED o per specificare un dispositivo di visualizzazione secondario.</span><span class="sxs-lookup"><span data-stu-id="692f2-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="692f2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="692f2-115">Requirements</span></span>



| <span data-ttu-id="692f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="692f2-116">Requirement</span></span> | <span data-ttu-id="692f2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="692f2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="692f2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="692f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="692f2-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="692f2-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="692f2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="692f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="692f2-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="692f2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="692f2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="692f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692f2-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="692f2-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




