---
description: Carica una sezione di trama e notifica all'host asynchrnously quando viene completato.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: LoadTextureSliceAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304055"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="09773-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: LoadTextureSliceAsync</span><span class="sxs-lookup"><span data-stu-id="09773-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="09773-104">Carica una sezione di trama e notifica all'host asynchrnously quando viene completato.</span><span class="sxs-lookup"><span data-stu-id="09773-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="09773-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09773-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="09773-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09773-106">Parameters</span></span>

<span data-ttu-id="09773-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="09773-107">*textureId* </span></span>  
<span data-ttu-id="09773-108">ID della trama per cui caricare la sezione.</span><span class="sxs-lookup"><span data-stu-id="09773-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="09773-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="09773-109">*sliceIndex* </span></span>  
<span data-ttu-id="09773-110">Indice della sezione da caricare.</span><span class="sxs-lookup"><span data-stu-id="09773-110">The index of the slice to load.</span></span>

<span data-ttu-id="09773-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="09773-111">*formatOverride* </span></span>  
<span data-ttu-id="09773-112">Specifica l'override del formato.</span><span class="sxs-lookup"><span data-stu-id="09773-112">Specifies the format override.</span></span>

<span data-ttu-id="09773-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="09773-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="09773-114">Stringa COM contenente il nome del file di dati dell'istogramma associato alla sezione della trama.</span><span class="sxs-lookup"><span data-stu-id="09773-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="09773-115">*callback* </span><span class="sxs-lookup"><span data-stu-id="09773-115">*callbacks* </span></span>  
<span data-ttu-id="09773-116">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="09773-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="09773-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="09773-117">*requestCookie* </span></span>  
<span data-ttu-id="09773-118">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="09773-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="09773-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="09773-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="09773-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="09773-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="09773-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09773-121">Return value</span></span>

<span data-ttu-id="09773-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09773-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09773-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09773-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="09773-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09773-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="09773-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09773-125">Header</span></span></p></td><td><span data-ttu-id="09773-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="09773-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="09773-127"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="09773-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="09773-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="09773-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
