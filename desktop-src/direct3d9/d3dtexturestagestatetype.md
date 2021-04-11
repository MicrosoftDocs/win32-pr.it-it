---
description: Gli Stati della fase trama definiscono le operazioni di trama a più Blend.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumerazione D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234983"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="ede6d-103">Enumerazione D3DTEXTURESTAGESTATETYPE</span><span class="sxs-lookup"><span data-stu-id="ede6d-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="ede6d-104">Gli Stati della fase trama definiscono le operazioni di trama a più Blend.</span><span class="sxs-lookup"><span data-stu-id="ede6d-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="ede6d-105">Alcuni Stati del campionatore configurano l'elaborazione dei vertici e alcuni configurano l'elaborazione dei pixel.</span><span class="sxs-lookup"><span data-stu-id="ede6d-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="ede6d-106">Gli Stati della fase della trama possono essere salvati e ripristinati usando stateblocks (vedere lo stato [di salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="ede6d-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="ede6d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ede6d-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="ede6d-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ede6d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ede6d-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**\_COLOROP D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-110">Lo stato della fase di trama è un'operazione di combinazione dei colori di trama identificata da un membro del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="ede6d-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="ede6d-111">Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP \_ Modulation. per tutte le altre fasi, il valore predefinito è D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="ede6d-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**\_COLORARG1 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-113">Trama: lo stato della fase è il primo argomento di colore per la fase, identificato da uno dei [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-114">L'argomento predefinito è D3DTA \_ texture.</span><span class="sxs-lookup"><span data-stu-id="ede6d-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="ede6d-115">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-116">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-117">Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**\_COLORARG2 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-119">Trama: lo stato della fase è il secondo argomento di colore per la fase, identificato da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-120">L'argomento predefinito è D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="ede6d-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="ede6d-121">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-122">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-123">Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="ede6d-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**\_ALPHAOP D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-125">Lo stato della fase di trama è un'operazione di fusione alfa di trama identificata da un membro del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="ede6d-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="ede6d-126">Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP \_ SELECTARG1 e per tutte le altre fasi il valore predefinito è D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="ede6d-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**\_ALPHAARG1 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-128">Trama: lo stato della fase è il primo argomento alfa per la fase, identificato da da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-129">L'argomento predefinito è D3DTA \_ texture.</span><span class="sxs-lookup"><span data-stu-id="ede6d-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="ede6d-130">Se per questa fase non è impostata alcuna trama, l'argomento predefinito è D3DTA \_ Diffusion.</span><span class="sxs-lookup"><span data-stu-id="ede6d-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="ede6d-131">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-132">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-133">Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**\_ALPHAARG2 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-135">Lo stato della fase di trama è il secondo argomento Alpha per la fase, identificato da da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-136">L'argomento predefinito è D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="ede6d-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="ede6d-137">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-138">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-139">Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**\_BUMPENVMAT00 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-141">Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 0 0 in una matrice di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="ede6d-142">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**\_BUMPENVMAT01 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-144">Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 0 1 in una matrice di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="ede6d-145">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**\_BUMPENVMAT10 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-147">Lo stato della fase trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 1 0 in una matrice di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="ede6d-148">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**\_BUMPENVMAT11 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-150">Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 1 1 in una matrice di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="ede6d-151">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**\_TEXCOORDINDEX D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-153">Indice del set di coordinate di trama da usare con questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="ede6d-154">È possibile specificare fino a otto set di coordinate di trama per vertice.</span><span class="sxs-lookup"><span data-stu-id="ede6d-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="ede6d-155">Se un vertice non include un set di coordinate di trama in corrispondenza dell'indice specificato, l'impostazione predefinita del sistema è le coordinate utente e v (0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="ede6d-156">Quando si esegue il rendering usando vertex shader, l'indice delle coordinate di trama di ogni fase deve essere impostato sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ede6d-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="ede6d-157">L'indice predefinito per ogni fase è uguale all'indice della fase.</span><span class="sxs-lookup"><span data-stu-id="ede6d-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="ede6d-158">Impostare questo stato sull'indice in base zero del set di coordinate per ogni vertice utilizzato da questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="ede6d-159">Inoltre, le applicazioni possono includere, come Logical o con l'indice da impostare, una delle costanti per richiedere che Direct3D generi automaticamente le coordinate di trama di input per una trasformazione di trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="ede6d-160">Per un elenco di tutte le costanti, vedere [D3DTSS \_ TCI](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="ede6d-161">Ad eccezione di D3DTSS \_ TCI \_ PassThru, che viene risolto in zero, se è incluso uno dei valori seguenti con l'indice da impostare, il sistema usa l'indice esclusivamente per determinare la modalità di wrapping della trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="ede6d-162">Questi flag sono particolarmente utili quando si esegue il mapping dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="ede6d-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**\_BUMPENVLSCALE D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-164">Valore della scala a virgola mobile per la luminanza della mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="ede6d-165">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**\_BUMPENVLOFFSET D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-167">Valore di offset a virgola mobile per la luminanza della mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="ede6d-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="ede6d-168">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**\_TEXTURETRANSFORMFLAGS D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-170">Membro del tipo enumerato [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) che controlla la trasformazione delle coordinate di trama per questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="ede6d-171">Il valore predefinito è D3DTTFF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="ede6d-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**\_COLORARG0 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-173">Impostazioni per il terzo operando di colore per le operazioni triadi (moltiplicazione, aggiunta e interpolazione lineare), identificate da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-174">Questa impostazione è supportata se \_ sono presenti le funzionalità del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ LERP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="ede6d-175">L'argomento predefinito è D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="ede6d-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="ede6d-176">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-177">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-178">Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**\_ALPHAARG0 D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-180">Impostazioni per l'operando del selettore di canale alfa per le operazioni di triade (moltiplicazione, aggiunta e interpolazione lineare), identificate da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-181">Questa impostazione è supportata se \_ sono presenti le funzionalità del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ LERP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="ede6d-182">L'argomento predefinito è D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="ede6d-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="ede6d-183">Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ede6d-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="ede6d-184">D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP.</span><span class="sxs-lookup"><span data-stu-id="ede6d-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="ede6d-185">L'argomento predefinito è (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**\_RESULTARG D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-187">Impostazione per selezionare il registro di destinazione per il risultato di questa fase, identificato da [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="ede6d-188">Questo valore può essere impostato su D3DTA \_ Current (valore predefinito) o su D3DTA \_ Temp, ovvero un singolo registro temporaneo che può essere letto nelle fasi successive come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="ede6d-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="ede6d-189">Il colore finale passato al Blender di nebbia e al buffer dei frame viene ricavato da D3DTA \_ Current, quindi l'ultimo stato della fase della trama attivo deve essere impostato su Write in Current.</span><span class="sxs-lookup"><span data-stu-id="ede6d-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="ede6d-190">Questa impostazione è supportata se \_ è presente la funzionalità del dispositivo TSSARGTEMP D3DPMISCCAPS.</span><span class="sxs-lookup"><span data-stu-id="ede6d-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**\_Costante D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="ede6d-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-192">Colore costante per fase.</span><span class="sxs-lookup"><span data-stu-id="ede6d-192">Per-stage constant color.</span></span> <span data-ttu-id="ede6d-193">Per verificare se un dispositivo supporta un colore costante per fase, vedere la costante D3DPMISCCAPS \_ PERSTAGECONSTANT in [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="ede6d-194">\_La costante D3DTSS viene utilizzata dalla \_ costante D3DTA.</span><span class="sxs-lookup"><span data-stu-id="ede6d-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="ede6d-195">Vedere [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="ede6d-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="ede6d-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ede6d-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ede6d-197">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ede6d-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ede6d-198">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ede6d-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ede6d-199">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ede6d-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ede6d-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="ede6d-200">Remarks</span></span>

<span data-ttu-id="ede6d-201">I membri di questo tipo enumerato vengono utilizzati con i metodi [**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per recuperare e impostare i valori dello stato della trama.</span><span class="sxs-lookup"><span data-stu-id="ede6d-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="ede6d-202">L'intervallo valido di valori per i \_ coefficienti della matrice di mapping di D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 e D3DTSS BUMPENVMAT11 \_ è maggiore o uguale a-8,0 e minore di 8,0.</span><span class="sxs-lookup"><span data-stu-id="ede6d-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="ede6d-203">Questo intervallo, espresso in notazione matematica è (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="ede6d-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ede6d-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ede6d-204">Requirements</span></span>



| <span data-ttu-id="ede6d-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="ede6d-205">Requirement</span></span> | <span data-ttu-id="ede6d-206">Valore</span><span class="sxs-lookup"><span data-stu-id="ede6d-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ede6d-207">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ede6d-207">Header</span></span><br/> | <dl> <span data-ttu-id="ede6d-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede6d-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede6d-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ede6d-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede6d-210">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="ede6d-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ede6d-211">**IDirect3DDevice9:: GetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="ede6d-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="ede6d-212">**IDirect3DDevice9:: SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="ede6d-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
