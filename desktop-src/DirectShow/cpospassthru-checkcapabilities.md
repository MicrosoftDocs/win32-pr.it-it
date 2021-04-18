---
description: 'Il metodo CheckCapabilities esegue una query per determinare se un flusso ha specificato funzionalità di ricerca. Questo metodo implementa il metodo IMediaSeeking:: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Metodo CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329518"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="deb41-104">CPosPassThru. CheckCapabilities, metodo</span><span class="sxs-lookup"><span data-stu-id="deb41-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="deb41-105">Il `CheckCapabilities` metodo esegue una query per determinare se un flusso ha specificato funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="deb41-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="deb41-106">Questo metodo implementa il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="deb41-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deb41-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="deb41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="deb41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb41-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="deb41-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="deb41-110">Puntatore a una combinazione bit per bit di uno o più attributi per la [**\_ ricerca di \_ \_ funzionalità**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="deb41-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="deb41-111">Quando il metodo restituisce un risultato, il valore indica quale di questi attributi sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="deb41-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb41-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="deb41-112">Return value</span></span>

<span data-ttu-id="deb41-113">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="deb41-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb41-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deb41-114">Requirements</span></span>



| <span data-ttu-id="deb41-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb41-115">Requirement</span></span> | <span data-ttu-id="deb41-116">Valore</span><span class="sxs-lookup"><span data-stu-id="deb41-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb41-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="deb41-117">Header</span></span><br/>  | <dl> <span data-ttu-id="deb41-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="deb41-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="deb41-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="deb41-119">Library</span></span><br/> | <dl> <span data-ttu-id="deb41-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="deb41-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb41-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deb41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb41-122">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="deb41-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




