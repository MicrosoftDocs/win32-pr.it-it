---
description: Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni con fotogrammi chiave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interfaccia ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323480"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="d8e54-103">Interfaccia ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d8e54-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="d8e54-104">Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni con fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="d8e54-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="d8e54-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d8e54-105">Members</span></span>

<span data-ttu-id="d8e54-106">L'interfaccia **ID3DXKeyframedAnimationSet** eredita da [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="d8e54-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="d8e54-107">**ID3DXKeyframedAnimationSet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d8e54-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="d8e54-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d8e54-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8e54-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d8e54-109">Methods</span></span>

<span data-ttu-id="d8e54-110">L'interfaccia **ID3DXKeyframedAnimationSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d8e54-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="d8e54-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="d8e54-111">Method</span></span>                                                                                   | <span data-ttu-id="d8e54-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8e54-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8e54-113">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="d8e54-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="d8e54-114">Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="d8e54-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="d8e54-115">**GetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="d8e54-116">Ottiene informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d8e54-117">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="d8e54-118">Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="d8e54-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d8e54-119">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="d8e54-120">Ottiene il numero di chiavi di callback nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d8e54-121">**GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="d8e54-122">Ottiene il numero di chiavi di rotazione nell'animazione del fotogramma chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d8e54-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="d8e54-123">**GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="d8e54-124">Ottiene il numero di chiavi di scala nell'animazione del fotogramma chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d8e54-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d8e54-125">**GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="d8e54-126">Ottiene il numero di chiavi di traslazione nell'animazione del fotogramma chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d8e54-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="d8e54-127">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="d8e54-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="d8e54-128">Ottiene il tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d8e54-129">**GetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="d8e54-130">Ottenere le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d8e54-131">**GetRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="d8e54-132">Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="d8e54-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="d8e54-133">**GetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="d8e54-134">Ottenere informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d8e54-135">**GetScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="d8e54-136">Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="d8e54-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="d8e54-137">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="d8e54-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="d8e54-138">Ottiene il numero di cicli del fotogramma chiave di animazione che si verificano al secondo.</span><span class="sxs-lookup"><span data-stu-id="d8e54-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="d8e54-139">**GetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="d8e54-140">Ottiene le informazioni di conversione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d8e54-141">**GetTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="d8e54-142">Compila una matrice con i dati della chiave di conversione utilizzati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="d8e54-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="d8e54-143">**RegisterAnimationSRTKeys**</span><span class="sxs-lookup"><span data-stu-id="d8e54-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="d8e54-144">Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.</span><span class="sxs-lookup"><span data-stu-id="d8e54-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="d8e54-145">**SetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="d8e54-146">Imposta le informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d8e54-147">**SetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="d8e54-148">Impostare le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d8e54-149">**SetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="d8e54-150">Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d8e54-151">**SetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="d8e54-152">Impostare le informazioni di traduzione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d8e54-153">**UnregisterAnimation**</span><span class="sxs-lookup"><span data-stu-id="d8e54-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="d8e54-154">Rimuovere i dati di animazione dal set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d8e54-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d8e54-155">**UnregisterRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="d8e54-156">Rimuove i dati di rotazione in corrispondenza del fotogramma chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="d8e54-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d8e54-157">**UnregisterScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="d8e54-158">Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="d8e54-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d8e54-159">**UnregisterTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d8e54-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="d8e54-160">Rimuove i dati di traduzione in corrispondenza del fotogramma chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="d8e54-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="d8e54-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8e54-161">Remarks</span></span>

<span data-ttu-id="d8e54-162">Creare un set di animazioni con fotogramma chiave con [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="d8e54-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="d8e54-163">Il tipo LPD3DXKEYFRAMEDANIMATIONSET è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d8e54-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="d8e54-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e54-164">Requirements</span></span>



| <span data-ttu-id="d8e54-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e54-165">Requirement</span></span> | <span data-ttu-id="d8e54-166">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e54-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e54-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8e54-167">Header</span></span><br/>  | <dl> <span data-ttu-id="d8e54-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8e54-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d8e54-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8e54-169">Library</span></span><br/> | <dl> <span data-ttu-id="d8e54-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8e54-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8e54-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e54-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e54-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="d8e54-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="d8e54-173">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="d8e54-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




