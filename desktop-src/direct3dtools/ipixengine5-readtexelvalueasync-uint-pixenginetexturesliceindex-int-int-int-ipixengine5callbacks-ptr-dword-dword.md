---
description: Legge un valore Texel e restituisce il risultato al asynchrnously host.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: ReadTexelValueAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304306"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="b1be9-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: ReadTexelValueAsync</span><span class="sxs-lookup"><span data-stu-id="b1be9-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="b1be9-104">Legge un valore Texel e restituisce il risultato al asynchrnously host.</span><span class="sxs-lookup"><span data-stu-id="b1be9-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1be9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1be9-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b1be9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1be9-106">Parameters</span></span>

<span data-ttu-id="b1be9-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="b1be9-107">*textureId* </span></span>  
<span data-ttu-id="b1be9-108">ID della trama da cui leggere il valore Texel.</span><span class="sxs-lookup"><span data-stu-id="b1be9-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="b1be9-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="b1be9-109">*sliceIndex* </span></span>  
<span data-ttu-id="b1be9-110">Indice della sezione all'interno della trama da cui leggere il valore di Texel.</span><span class="sxs-lookup"><span data-stu-id="b1be9-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="b1be9-111">*x* </span><span class="sxs-lookup"><span data-stu-id="b1be9-111">*x* </span></span>  
<span data-ttu-id="b1be9-112">Coordinata x Texel da leggere.</span><span class="sxs-lookup"><span data-stu-id="b1be9-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="b1be9-113">*y* </span><span class="sxs-lookup"><span data-stu-id="b1be9-113">*y* </span></span>  
<span data-ttu-id="b1be9-114">Coordinata del Texel y da leggere.</span><span class="sxs-lookup"><span data-stu-id="b1be9-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="b1be9-115">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="b1be9-115">*formatOverride* </span></span>  
<span data-ttu-id="b1be9-116">Sostituzione del formato colori.</span><span class="sxs-lookup"><span data-stu-id="b1be9-116">The color format override.</span></span>

<span data-ttu-id="b1be9-117">*callback* </span><span class="sxs-lookup"><span data-stu-id="b1be9-117">*callbacks* </span></span>  
<span data-ttu-id="b1be9-118">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="b1be9-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="b1be9-119">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b1be9-119">*requestCookie* </span></span>  
<span data-ttu-id="b1be9-120">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="b1be9-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b1be9-121">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b1be9-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b1be9-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b1be9-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1be9-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1be9-123">Return value</span></span>

<span data-ttu-id="b1be9-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b1be9-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1be9-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1be9-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1be9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1be9-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b1be9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1be9-127">Header</span></span></p></td><td><span data-ttu-id="b1be9-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b1be9-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b1be9-129"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b1be9-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b1be9-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="b1be9-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
