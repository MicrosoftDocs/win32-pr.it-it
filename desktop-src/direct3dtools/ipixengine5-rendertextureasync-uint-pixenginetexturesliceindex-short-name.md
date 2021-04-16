---
description: Esegue il rendering di una trama in un file e restituisce il risultato al asynchrnously host.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: RenderTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521522"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="e6210-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: RenderTextureAsync</span><span class="sxs-lookup"><span data-stu-id="e6210-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="e6210-104">Esegue il rendering di una trama in un file e restituisce il risultato al asynchrnously host.</span><span class="sxs-lookup"><span data-stu-id="e6210-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6210-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6210-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e6210-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6210-106">Parameters</span></span>

<span data-ttu-id="e6210-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="e6210-107">*textureId* </span></span>  
<span data-ttu-id="e6210-108">ID della trama di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="e6210-108">The ID of the texture to render.</span></span>

<span data-ttu-id="e6210-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="e6210-109">*sliceIndex* </span></span>  
<span data-ttu-id="e6210-110">Indice della sezione all'interno della trama di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="e6210-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="e6210-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="e6210-111">*formatOverride* </span></span>  
<span data-ttu-id="e6210-112">Sostituzione del formato colori.</span><span class="sxs-lookup"><span data-stu-id="e6210-112">The color format override.</span></span>

<span data-ttu-id="e6210-113">*inferiore*</span><span class="sxs-lookup"><span data-stu-id="e6210-113">*lower*</span></span>   

<span data-ttu-id="e6210-114">*superiore*</span><span class="sxs-lookup"><span data-stu-id="e6210-114">*upper*</span></span>   

<span data-ttu-id="e6210-115">*shaderFileName* </span><span class="sxs-lookup"><span data-stu-id="e6210-115">*shaderFileName* </span></span>  
<span data-ttu-id="e6210-116">Stringa COM contenente il percorso del file shader.</span><span class="sxs-lookup"><span data-stu-id="e6210-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="e6210-117">*numFloatShaderVars* </span><span class="sxs-lookup"><span data-stu-id="e6210-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="e6210-118">Numero di variabili shader a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="e6210-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="e6210-119">*\_shaderFloatVarName count6* </span><span class="sxs-lookup"><span data-stu-id="e6210-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="e6210-120">Stringhe COM che consono i nomi delle variabili shader a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e6210-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="e6210-121">*\_shaderFloatVarValue count6* </span><span class="sxs-lookup"><span data-stu-id="e6210-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="e6210-122">Variabili shader a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e6210-122">The floating-point shader variables.</span></span>

<span data-ttu-id="e6210-123">*numBoolShaderVars* </span><span class="sxs-lookup"><span data-stu-id="e6210-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="e6210-124">Numero di variabili di shader booleane.</span><span class="sxs-lookup"><span data-stu-id="e6210-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="e6210-125">*\_shaderBoolVarName count9* </span><span class="sxs-lookup"><span data-stu-id="e6210-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="e6210-126">Stringhe COM che denominano i nomi delle variabili shader booleane.</span><span class="sxs-lookup"><span data-stu-id="e6210-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="e6210-127">*\_shaderBoolVarValue count9* </span><span class="sxs-lookup"><span data-stu-id="e6210-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="e6210-128">Variabili shader booleane.</span><span class="sxs-lookup"><span data-stu-id="e6210-128">The boolean shader variables.</span></span>

<span data-ttu-id="e6210-129">*renderContentFileName* </span><span class="sxs-lookup"><span data-stu-id="e6210-129">*renderContentFileName* </span></span>  
<span data-ttu-id="e6210-130">Stringa COM contenente il percorso del file in cui è stata scritta la trama di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="e6210-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="e6210-131">*callback* </span><span class="sxs-lookup"><span data-stu-id="e6210-131">*callbacks* </span></span>  
<span data-ttu-id="e6210-132">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="e6210-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="e6210-133">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e6210-133">*requestCookie* </span></span>  
<span data-ttu-id="e6210-134">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="e6210-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e6210-135">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e6210-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e6210-136">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e6210-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6210-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6210-137">Return value</span></span>

<span data-ttu-id="e6210-138">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6210-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6210-139">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6210-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6210-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6210-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e6210-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6210-141">Header</span></span></p></td><td><span data-ttu-id="e6210-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e6210-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e6210-143"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e6210-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e6210-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="e6210-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
