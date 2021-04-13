---
description: Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente usando la libreria Math XNA alla libreria DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migrazione del codice dalla libreria Math XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528039"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="03dd4-103">Migrazione del codice dalla libreria Math XNA</span><span class="sxs-lookup"><span data-stu-id="03dd4-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="03dd4-104">Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente usando la libreria Math XNA alla libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="03dd4-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="03dd4-105">Modifiche all'intestazione</span><span class="sxs-lookup"><span data-stu-id="03dd4-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="03dd4-106">Modifiche costanti</span><span class="sxs-lookup"><span data-stu-id="03dd4-106">Constant Changes</span></span>](#constant-changes)
-   <span data-ttu-id="03dd4-107">[Namespaces](#namespaces) (Spazi dei nomi)</span><span class="sxs-lookup"><span data-stu-id="03dd4-107">[Namespaces](#namespaces)</span></span>
-   [<span data-ttu-id="03dd4-108">Caricamenti parziali</span><span class="sxs-lookup"><span data-stu-id="03dd4-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="03dd4-109">Rimozione dei tipi specifici di Xbox 360</span><span class="sxs-lookup"><span data-stu-id="03dd4-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="03dd4-110">Intrinseci ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="03dd4-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="03dd4-111">Permute</span><span class="sxs-lookup"><span data-stu-id="03dd4-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="03dd4-112">Moduli modello</span><span class="sxs-lookup"><span data-stu-id="03dd4-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="03dd4-113">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="03dd4-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="03dd4-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03dd4-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="03dd4-115">Modifiche all'intestazione</span><span class="sxs-lookup"><span data-stu-id="03dd4-115">Header Changes</span></span>

<span data-ttu-id="03dd4-116">La libreria DirectXMath usa un nuovo set di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="03dd4-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="03dd4-117">Sostituire l'intestazione XNAMath. h con DirectXMath. h e aggiungere DirectXPackedVector. h per i tipi "GPU compressi".</span><span class="sxs-lookup"><span data-stu-id="03dd4-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="03dd4-118">I tipi di delimitazione dall'esempio di conflitto DirectX SDK in xnacollision. h fanno ora parte della libreria DirectXMath in DirectXCollision. h.</span><span class="sxs-lookup"><span data-stu-id="03dd4-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="03dd4-119">Questi sono stati modificati per usare le classi C++ anziché un'API di tipo C.</span><span class="sxs-lookup"><span data-stu-id="03dd4-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="03dd4-120">Modifiche costanti</span><span class="sxs-lookup"><span data-stu-id="03dd4-120">Constant Changes</span></span>

<span data-ttu-id="03dd4-121">\_La versione di XNAMATH (200, 201, 202, 203, 204 e così via) è stata sostituita dalla \_ versione DIRECXTMATH (300, 301, 302, 303 e così via).</span><span class="sxs-lookup"><span data-stu-id="03dd4-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="03dd4-122">DirectXMath 3,00 e 3,02 forniti con le versioni preliminari del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="03dd4-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="03dd4-123">DirectXMath 3,03 è la versione finale di Windows 8 SDK.</span><span class="sxs-lookup"><span data-stu-id="03dd4-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="03dd4-124">Spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="03dd4-124">Namespaces</span></span>

<span data-ttu-id="03dd4-125">La libreria DirectXMath usa gli spazi dei nomi C++ per organizzare i tipi.</span><span class="sxs-lookup"><span data-stu-id="03dd4-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="03dd4-126">XNA Math usava solo lo spazio dei nomi globale.</span><span class="sxs-lookup"><span data-stu-id="03dd4-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="03dd4-127">I tipi DirectXMath in comune con XNA Math si trovano nello spazio dei nomi "DirectX" o "DirectX::P ackedVector".</span><span class="sxs-lookup"><span data-stu-id="03dd4-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="03dd4-128">Nei file di origine C++, una soluzione semplice consiste nell'aggiungere istruzioni ' using ':</span><span class="sxs-lookup"><span data-stu-id="03dd4-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="03dd4-129">Per le intestazioni, non viene considerata una procedura consigliata per aggiungere istruzioni using.</span><span class="sxs-lookup"><span data-stu-id="03dd4-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="03dd4-130">Aggiungere invece spazi dei nomi completi:</span><span class="sxs-lookup"><span data-stu-id="03dd4-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="03dd4-131">Caricamenti parziali</span><span class="sxs-lookup"><span data-stu-id="03dd4-131">Partial Loads</span></span>

<span data-ttu-id="03dd4-132">Per le varie funzioni che caricano meno di 4 elementi di un XMVECTOR, la libreria Math XNA lascia gli elementi aggiuntivi indefiniti.</span><span class="sxs-lookup"><span data-stu-id="03dd4-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="03dd4-133">DirectXMath riempirà sempre questi elementi aggiuntivi con 0.</span><span class="sxs-lookup"><span data-stu-id="03dd4-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="03dd4-134">Rimozione dei tipi specifici di Xbox 360</span><span class="sxs-lookup"><span data-stu-id="03dd4-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="03dd4-135">I tipi, le funzioni e le costanti di libreria Math XNA seguenti non sono disponibili in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="03dd4-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="03dd4-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="03dd4-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="03dd4-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="03dd4-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="03dd4-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="03dd4-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="03dd4-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ \_ \_ \_ XMMulHenD3, g XMMulDHen3, g XMXorHenD3, g XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="03dd4-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="03dd4-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="03dd4-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="03dd4-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="03dd4-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="03dd4-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="03dd4-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="03dd4-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g XMAddIco4, \_ g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="03dd4-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="03dd4-144">\_\_Vector4 è deprecato.</span><span class="sxs-lookup"><span data-stu-id="03dd4-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="03dd4-145">In alternativa, utilizzare [**XMVECTORI32**](xmvectori32-data-type.md) o [**XMVECTORU32**](xmvectoru32-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="03dd4-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="03dd4-146">Le funzioni e i tipi seguenti sono deprecati perché sono solo Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="03dd4-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="03dd4-147">Intrinseci ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="03dd4-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="03dd4-148">La dichiarazione di una costante di vettore con questo codice verrà compilata per il calcolo XNA per SSE e nessun INTRINSECo, ma avrà esito negativo per DirectXMath con ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="03dd4-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="03dd4-149">In generale, questo metodo di inizializzazione di un [**XMVECTOR**](xmvector-data-type.md)non è consigliato.</span><span class="sxs-lookup"><span data-stu-id="03dd4-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="03dd4-150">Tuttavia, se si desidera una costante Vector, la classe [**XMVECTORF32**](xmvectorf32-data-type.md) supporta questo stile di inizializzazione e restituisce automaticamente il tipo **XMVECTOR** in modo da poter utilizzare **XMVECTORF32** nella maggior parte degli stessi contesti.</span><span class="sxs-lookup"><span data-stu-id="03dd4-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="03dd4-151">Qualsiasi operazione di scrittura in una classe **XMVECTORF32** richiede il riferimento esplicito al membro **XMVECTOR** . v.</span><span class="sxs-lookup"><span data-stu-id="03dd4-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="03dd4-152">Permute</span><span class="sxs-lookup"><span data-stu-id="03dd4-152">Permute</span></span>

<span data-ttu-id="03dd4-153">La libreria Math di XNA ha il formato seguente per il vettore generale permute:</span><span class="sxs-lookup"><span data-stu-id="03dd4-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="03dd4-154">Per DirectXMath, **XMVectorPermuteControl** è stato eliminato e il \_ permute XM \_ 0x..</span><span class="sxs-lookup"><span data-stu-id="03dd4-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="03dd4-155">Le \_ \_ costanti 1z di permute XM sono state ridefinite come semplici indici 0-7.</span><span class="sxs-lookup"><span data-stu-id="03dd4-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="03dd4-156">Ecco la nuova firma per [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="03dd4-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="03dd4-157">Invece di una parola di controllo, questa funzione accetta direttamente i 4 indici come parametri, che lo rendono analogo alla funzione [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando il nuovo XM \_ SWIZZLE \_ X.</span><span class="sxs-lookup"><span data-stu-id="03dd4-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="03dd4-158">\_Costanti XM SWIZZLE \_ W definite come semplici indici 0-3.</span><span class="sxs-lookup"><span data-stu-id="03dd4-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="03dd4-159">Per i valori costanti, è disponibile un modo molto più efficiente per implementare permute.</span><span class="sxs-lookup"><span data-stu-id="03dd4-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="03dd4-160">Anziché utilizzare il formato di funzione di [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), utilizzare il formato del **modello** :</span><span class="sxs-lookup"><span data-stu-id="03dd4-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="03dd4-161">Moduli modello</span><span class="sxs-lookup"><span data-stu-id="03dd4-161">Template Forms</span></span>
>
> <span data-ttu-id="03dd4-162">In generale, l'uso di un form modello su una forma di funzione delle funzioni seguenti è molto più efficiente e consente alla libreria di eseguire ottimizzazioni specifiche della piattaforma tramite la specializzazione del modello.</span><span class="sxs-lookup"><span data-stu-id="03dd4-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="03dd4-163">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="03dd4-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="03dd4-164">Funzione eliminata</span><span class="sxs-lookup"><span data-stu-id="03dd4-164">Eliminated Function</span></span>        | <span data-ttu-id="03dd4-165">Sostituzione</span><span class="sxs-lookup"><span data-stu-id="03dd4-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="03dd4-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="03dd4-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="03dd4-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="03dd4-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="03dd4-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="03dd4-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="03dd4-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="03dd4-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="03dd4-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="03dd4-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="03dd4-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="03dd4-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="03dd4-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="03dd4-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="03dd4-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="03dd4-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="03dd4-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="03dd4-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="03dd4-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="03dd4-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="03dd4-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="03dd4-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="03dd4-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="03dd4-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="03dd4-178">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="03dd4-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="03dd4-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="03dd4-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="03dd4-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="03dd4-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="03dd4-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="03dd4-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="03dd4-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="03dd4-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="03dd4-183">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="03dd4-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="03dd4-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="03dd4-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="03dd4-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="03dd4-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="03dd4-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="03dd4-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="03dd4-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="03dd4-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="03dd4-188">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="03dd4-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="03dd4-189">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="03dd4-190">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="03dd4-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="03dd4-191">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="03dd4-192">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="03dd4-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="03dd4-193">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="03dd4-194">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="03dd4-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="03dd4-195">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="03dd4-196">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="03dd4-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="03dd4-197">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="03dd4-198">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="03dd4-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="03dd4-199">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="03dd4-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="03dd4-200">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="03dd4-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="03dd4-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03dd4-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="03dd4-202">Guida alla programmazione di DirectXMath</span><span class="sxs-lookup"><span data-stu-id="03dd4-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
