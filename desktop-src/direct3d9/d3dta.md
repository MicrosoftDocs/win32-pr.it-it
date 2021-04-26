---
description: "Le costanti dell'argomento texture vengono usate come valori per i membri seguenti del tipo enumerato D3DTEXTURESTAGESTATETYPE:"
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995288"
---
# <a name="d3dta"></a><span data-ttu-id="4adb6-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="4adb6-103">D3DTA</span></span>

<span data-ttu-id="4adb6-104">Le costanti dell'argomento texture vengono usate come valori per i membri seguenti del tipo enumerato [**D3DTEXTURESTAGESTATETYPE:**](./d3dtexturestagestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="4adb6-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="4adb6-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="4adb6-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="4adb6-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="4adb6-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="4adb6-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="4adb6-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="4adb6-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="4adb6-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="4adb6-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="4adb6-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="4adb6-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="4adb6-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="4adb6-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="4adb6-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="4adb6-112">Impostare e recuperare gli argomenti di trama chiamando i [**metodi SetTextureStageState**](/windows/desktop/api) [**e GetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)</span><span class="sxs-lookup"><span data-stu-id="4adb6-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="4adb6-113">Flag di argomento</span><span class="sxs-lookup"><span data-stu-id="4adb6-113">Argument flags</span></span>

<span data-ttu-id="4adb6-114">È possibile combinare un flag di argomento con un modificatore, ma non è possibile combinare due flag di argomento.</span><span class="sxs-lookup"><span data-stu-id="4adb6-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="4adb6-115">\#Definire</span><span class="sxs-lookup"><span data-stu-id="4adb6-115">\#define</span></span>          | <span data-ttu-id="4adb6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4adb6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adb6-117">COSTANTE D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="4adb6-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="4adb6-118">Selezionare una costante da una fase di trama.</span><span class="sxs-lookup"><span data-stu-id="4adb6-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="4adb6-119">Il valore predefinito è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="4adb6-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4adb6-120">D3DTA \_ CURRENT</span><span class="sxs-lookup"><span data-stu-id="4adb6-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="4adb6-121">L'argomento texture è il risultato della fase di fusione precedente.</span><span class="sxs-lookup"><span data-stu-id="4adb6-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="4adb6-122">Nella prima fase della trama (fase 0), questo argomento è equivalente a D3DTA \_ DIFFUSE.</span><span class="sxs-lookup"><span data-stu-id="4adb6-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="4adb6-123">Se la fase di fusione precedente usa una trama della mappa di rilievo (operazione D3DTOP BUMPENVMAP), il sistema sceglie la trama dalla fase prima della trama della mappa di \_ rilievo.</span><span class="sxs-lookup"><span data-stu-id="4adb6-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="4adb6-124">Se s rappresenta la fase della trama corrente e s - 1 contiene una trama di mappa di rilievo, questo argomento diventa l'output del risultato dalla fase della trama s - 2.</span><span class="sxs-lookup"><span data-stu-id="4adb6-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="4adb6-125">Le autorizzazioni sono di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="4adb6-126">D3DTA \_ DIFFUSE</span><span class="sxs-lookup"><span data-stu-id="4adb6-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="4adb6-127">L'argomento texture è il colore diffuso interpolato dai componenti dei vertici durante l'ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="4adb6-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="4adb6-128">Se il vertice non contiene un colore diffuso, il colore predefinito è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="4adb6-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="4adb6-129">Le autorizzazioni sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4adb6-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="4adb6-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="4adb6-131">Mascherare il valore per tutti gli argomenti; non viene usato quando si impostano gli argomenti della trama.</span><span class="sxs-lookup"><span data-stu-id="4adb6-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="4adb6-132">D3DTA \_ SPECULAR</span><span class="sxs-lookup"><span data-stu-id="4adb6-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="4adb6-133">L'argomento texture è il colore speculare interpolato dai componenti dei vertici durante l'ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="4adb6-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="4adb6-134">Se il vertice non contiene un colore speculare, il colore predefinito è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="4adb6-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="4adb6-135">Le autorizzazioni sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4adb6-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="4adb6-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="4adb6-137">L'argomento texture è un colore di registro temporaneo per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="4adb6-138">D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ [D3DPMISCCAPS \_ TSSARGTEMP.](d3dpmisccaps.md)</span><span class="sxs-lookup"><span data-stu-id="4adb6-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="4adb6-139">Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0).</span><span class="sxs-lookup"><span data-stu-id="4adb6-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="4adb6-140">Le autorizzazioni sono di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="4adb6-141">TRAMA D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="4adb6-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="4adb6-142">L'argomento trama è il colore della trama per questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="4adb6-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="4adb6-143">Le autorizzazioni sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="4adb6-144">D3DTA \_ TFACTOR</span><span class="sxs-lookup"><span data-stu-id="4adb6-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="4adb6-145">L'argomento texture è il fattore di trama impostato in una chiamata precedente a [**SetRenderState**](/windows/desktop/api) con il valore dello stato di rendering [**\_ TEXTUREFACTOR D3DRS.**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="4adb6-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="4adb6-146">Le autorizzazioni sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="4adb6-147">Flag di modifica</span><span class="sxs-lookup"><span data-stu-id="4adb6-147">Modifier flags</span></span>

<span data-ttu-id="4adb6-148">Un flag di argomento può essere combinato con uno dei flag di modifica seguenti.</span><span class="sxs-lookup"><span data-stu-id="4adb6-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="4adb6-149">\#Definire</span><span class="sxs-lookup"><span data-stu-id="4adb6-149">\#define</span></span>              | <span data-ttu-id="4adb6-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4adb6-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adb6-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="4adb6-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="4adb6-152">Replicare le informazioni alfa in tutti i canali di colore prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4adb6-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="4adb6-153">Si tratta di un modificatore di lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-153">This is a read modifier.</span></span> |
| <span data-ttu-id="4adb6-154">COMPLEMENTO D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="4adb6-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="4adb6-155">Prendere il complemento dell'argomento x, (1.0 - x).</span><span class="sxs-lookup"><span data-stu-id="4adb6-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="4adb6-156">Si tratta di un modificatore di lettura.</span><span class="sxs-lookup"><span data-stu-id="4adb6-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="4adb6-157">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="4adb6-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="4adb6-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4adb6-158">Header</span></span>                   | <span data-ttu-id="4adb6-159">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="4adb6-159">d3d9types.h</span></span> |
| <span data-ttu-id="4adb6-160">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="4adb6-160">Minimum operating system</span></span> | <span data-ttu-id="4adb6-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4adb6-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="4adb6-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4adb6-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adb6-163">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="4adb6-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
