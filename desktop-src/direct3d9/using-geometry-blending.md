---
description: La struttura definita dall'utente seguente può essere usata per i vertici che verranno combinati tra due matrici.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Uso della combinazione di geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303797"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="0caf1-103">Uso della combinazione di geometria (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0caf1-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="0caf1-104">La struttura definita dall'utente seguente può essere usata per i vertici che verranno combinati tra due matrici.</span><span class="sxs-lookup"><span data-stu-id="0caf1-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="0caf1-105">Il peso della Blend deve essere visualizzato dopo i dati position e RHW in FVF e prima della normale del vertice.</span><span class="sxs-lookup"><span data-stu-id="0caf1-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="0caf1-106">Si noti che il formato Vertex precedente contiene solo un valore di peso di fusione.</span><span class="sxs-lookup"><span data-stu-id="0caf1-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="0caf1-107">Ciò è dovuto al fatto che saranno presenti due matrici internazionali, definite negli Stati di trasformazione [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) e **D3DTS \_ WORLDMATRIX**(1).</span><span class="sxs-lookup"><span data-stu-id="0caf1-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="0caf1-108">Il sistema combina ogni vertice tra queste due matrici usando il valore del peso singolo.</span><span class="sxs-lookup"><span data-stu-id="0caf1-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="0caf1-109">Per tre matrici sono necessari solo due pesi e così via.</span><span class="sxs-lookup"><span data-stu-id="0caf1-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="0caf1-110">La definizione di pesi dell'interfaccia è facile.</span><span class="sxs-lookup"><span data-stu-id="0caf1-110">Defining skin weights is easy.</span></span> <span data-ttu-id="0caf1-111">L'uso di una funzione lineare della distanza tra le giunzioni è un inizio positivo, ma una funzione Sigma più liscia sembra migliore.</span><span class="sxs-lookup"><span data-stu-id="0caf1-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="0caf1-112">La scelta di una funzione di distribuzione di peso cutaneo può comportare grinze acute alle articolazioni, se lo si desidera, usando una variazione grande del peso della pelle per una breve distanza.</span><span class="sxs-lookup"><span data-stu-id="0caf1-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="0caf1-113">Impostazione di matrici di Blend</span><span class="sxs-lookup"><span data-stu-id="0caf1-113">Setting Blending Matrices</span></span>

<span data-ttu-id="0caf1-114">È possibile impostare le matrici di trasformazione tra le quali il sistema esegue la fusione chiamando il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0caf1-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0caf1-115">Impostare il primo parametro su un valore definito dalla macro [**\_ WORLDMATRIX D3DTS**](d3dts-worldmatrix.md) e impostare il secondo parametro sull'indirizzo della matrice da impostare.</span><span class="sxs-lookup"><span data-stu-id="0caf1-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="0caf1-116">Nell'esempio di codice C++ riportato di seguito vengono impostate due matrici internazionali, tra cui la geometria viene fusa per creare l'illusione di un ARM combinato.</span><span class="sxs-lookup"><span data-stu-id="0caf1-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="0caf1-117">Impostando una matrice di Blend, il sistema memorizza nella cache la matrice per un uso successivo. non indica al sistema di iniziare la fusione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="0caf1-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="0caf1-118">Abilitazione della fusione Geometry</span><span class="sxs-lookup"><span data-stu-id="0caf1-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="0caf1-119">Per impostazione predefinita, la combinazione di geometria è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0caf1-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="0caf1-120">Per abilitare la combinazione di geometria, chiamare il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) per impostare lo \_ stato di rendering VERTEXBLEND di D3DRS su un valore del tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0caf1-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="0caf1-121">Nell'esempio di codice seguente viene illustrato l'aspetto di questa chiamata quando si imposta lo stato di rendering di una blend tra due matrici internazionali.</span><span class="sxs-lookup"><span data-stu-id="0caf1-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="0caf1-122">Quando D3DRS \_ VERTEXBLEND è impostato su un valore diverso da D3DVBF \_ Disable, il sistema presuppone che il numero appropriato di pesi di fusione venga incluso nel formato del vertice.</span><span class="sxs-lookup"><span data-stu-id="0caf1-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="0caf1-123">È responsabilità dell'utente fornire un formato di vertice conforme e fornire una descrizione corretta del formato ai metodi di rendering Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0caf1-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="0caf1-124">Se abilitata, il sistema esegue la fusione geometrica per tutti gli oggetti sottoposti a rendering dai metodi di rendering DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="0caf1-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="0caf1-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0caf1-125">See Also</span></span>

[<span data-ttu-id="0caf1-126">Codici FVF della funzione fissa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0caf1-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="0caf1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0caf1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0caf1-128">Blending Geometry</span><span class="sxs-lookup"><span data-stu-id="0caf1-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
