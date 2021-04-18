---
description: Richiesta asincrona di caricamento dei dati dell'istogramma.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: LoadHistogramAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304307"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="b5349-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: LoadHistogramAsync</span><span class="sxs-lookup"><span data-stu-id="b5349-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="b5349-104">Richiesta asincrona di caricamento dei dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="b5349-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5349-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5349-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b5349-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5349-106">Parameters</span></span>

<span data-ttu-id="b5349-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="b5349-107">*textureId* </span></span>  
<span data-ttu-id="b5349-108">ID della trama per cui caricare i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="b5349-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="b5349-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="b5349-109">*sliceIndex* </span></span>  
<span data-ttu-id="b5349-110">Indice della sezione per cui caricare i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="b5349-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="b5349-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="b5349-111">*formatOverride* </span></span>  
<span data-ttu-id="b5349-112">Specifica l'override del formato.</span><span class="sxs-lookup"><span data-stu-id="b5349-112">Specifies the format override.</span></span>

<span data-ttu-id="b5349-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="b5349-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="b5349-114">Stringa COM contenente il nome del file di dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="b5349-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="b5349-115">*callback* </span><span class="sxs-lookup"><span data-stu-id="b5349-115">*callbacks* </span></span>  
<span data-ttu-id="b5349-116">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="b5349-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="b5349-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b5349-117">*requestCookie* </span></span>  
<span data-ttu-id="b5349-118">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="b5349-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b5349-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b5349-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b5349-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b5349-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5349-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5349-121">Return value</span></span>

<span data-ttu-id="b5349-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5349-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5349-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5349-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5349-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5349-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b5349-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5349-125">Header</span></span></p></td><td><span data-ttu-id="b5349-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b5349-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b5349-127"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5349-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b5349-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="b5349-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
