---
description: 'Il metodo GetInfo recupera informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine. Questo metodo implementa il metodo IAMStreamControl:: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Metodo CBaseStreamControl. GetInfo (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331649"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="2f2ff-104">CBaseStreamControl. GetInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="2f2ff-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="2f2ff-105">Il `GetInfo` metodo recupera informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="2f2ff-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="2f2ff-106">Questo metodo implementa il metodo [**IAMStreamControl:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="2f2ff-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f2ff-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2f2ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f2ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2ff-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="2f2ff-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2f2ff-110">Puntatore a una struttura di [**\_ \_ informazioni del flusso AM**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , allocata dal chiamante, che riceve le impostazioni correnti del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="2f2ff-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f2ff-111">Return value</span></span>

<span data-ttu-id="2f2ff-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="2f2ff-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2ff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2ff-113">Requirements</span></span>



| <span data-ttu-id="2f2ff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2ff-114">Requirement</span></span> | <span data-ttu-id="2f2ff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2ff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2ff-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f2ff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2f2ff-117"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ff-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f2ff-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f2ff-118">Library</span></span><br/> | <dl> <span data-ttu-id="2f2ff-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2ff-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f2ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2ff-121">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="2f2ff-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




