---
title: Accesso alle risorse
description: Sono disponibili diversi modi per accedere alle risorse.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993496"
---
# <a name="accessing-resources"></a><span data-ttu-id="9f91d-103">Accesso alle risorse</span><span class="sxs-lookup"><span data-stu-id="9f91d-103">Accessing Resources</span></span>

<span data-ttu-id="9f91d-104">Sono disponibili diversi modi per accedere alle [risorse](overviews-direct3d-11-resources-types.md).</span><span class="sxs-lookup"><span data-stu-id="9f91d-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="9f91d-105">Indipendentemente da Direct3D, Direct3D garantisce che restituisca zero per tutte le risorse a cui si accede fuori limite.</span><span class="sxs-lookup"><span data-stu-id="9f91d-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="9f91d-106">Accesso per offset di byte</span><span class="sxs-lookup"><span data-stu-id="9f91d-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="9f91d-107">Accesso in base all'indice</span><span class="sxs-lookup"><span data-stu-id="9f91d-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="9f91d-108">Accesso per metodo MIPS</span><span class="sxs-lookup"><span data-stu-id="9f91d-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="9f91d-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f91d-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="9f91d-110">Accesso per offset di byte</span><span class="sxs-lookup"><span data-stu-id="9f91d-110">Access By Byte Offset</span></span>

<span data-ttu-id="9f91d-111">È possibile accedere a due nuovi tipi di buffer usando un offset di byte:</span><span class="sxs-lookup"><span data-stu-id="9f91d-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="9f91d-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) è un buffer di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9f91d-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="9f91d-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) è un buffer di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="9f91d-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="9f91d-114">Accesso in base all'indice</span><span class="sxs-lookup"><span data-stu-id="9f91d-114">Access By Index</span></span>

<span data-ttu-id="9f91d-115">I tipi di risorse possono usare un indice per fare riferimento a una posizione specifica nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f91d-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="9f91d-116">Prendere in considerazione questo esempio:</span><span class="sxs-lookup"><span data-stu-id="9f91d-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="9f91d-117">Questo esempio Mostra come assegnare i 4 valori float archiviati in Texel che si trova nella posizione *pos* nella risorsa trama *2D texture alla variabile* *myvar* .</span><span class="sxs-lookup"><span data-stu-id="9f91d-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="9f91d-118">Il valore predefinito per l'accesso a una trama in questo modo è mipmap livello zero (il livello più dettagliato).</span><span class="sxs-lookup"><span data-stu-id="9f91d-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="9f91d-119">La riga "float4 myVar = texture \[ POS \] ;" è equivalente a "float4 myvar = texture. Load (uint3 (POS, 0));".</span><span class="sxs-lookup"><span data-stu-id="9f91d-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="9f91d-120">L'accesso in base all'indice è un nuovo miglioramento della sintassi di HLSL.</span><span class="sxs-lookup"><span data-stu-id="9f91d-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f91d-121">Il compilatore nella versione di giugno 2010 di DirectX SDK e versioni successive consente di indicizzare tutti i tipi di risorse ad eccezione dei [buffer degli indirizzi byte](direct3d-11-advanced-stages-cs-resources.md).</span><span class="sxs-lookup"><span data-stu-id="9f91d-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="9f91d-122">Il compilatore di giugno 2010 e versioni successive consente di dichiarare le variabili di risorse locali.</span><span class="sxs-lookup"><span data-stu-id="9f91d-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="9f91d-123">È possibile assegnare le risorse definite a livello globale (ad esempio, la *trama*) a queste variabili e usarle allo stesso modo delle rispettive controparti globali.</span><span class="sxs-lookup"><span data-stu-id="9f91d-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="9f91d-124">Accesso per metodo MIPS</span><span class="sxs-lookup"><span data-stu-id="9f91d-124">Access By Mips Method</span></span>

<span data-ttu-id="9f91d-125">Gli oggetti texture hanno un metodo **MIPS** , ad esempio [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85)), che è possibile usare per specificare il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="9f91d-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="9f91d-126">Questo esempio legge il colore archiviato in (7, 16) in mipmap livello 2 in una trama 2D:</span><span class="sxs-lookup"><span data-stu-id="9f91d-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="9f91d-127">Si tratta di un miglioramento del compilatore di giugno 2010 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9f91d-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="9f91d-128">L'espressione "texture. MIPS \[ 2 \] \[ uint2 (x, y) \] " equivale a "texture. Load (uint3 (x, y, 2))".</span><span class="sxs-lookup"><span data-stu-id="9f91d-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f91d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f91d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f91d-130">Panoramica di Compute Shader</span><span class="sxs-lookup"><span data-stu-id="9f91d-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 