---
description: Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente tramite la libreria matematica XNA alla libreria DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migrazione del codice dalla libreria matematica XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549963"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="7be5c-103">Migrazione del codice dalla libreria matematica XNA</span><span class="sxs-lookup"><span data-stu-id="7be5c-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="7be5c-104">Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente tramite la libreria matematica XNA alla libreria DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="7be5c-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="7be5c-105">Modifiche all'intestazione</span><span class="sxs-lookup"><span data-stu-id="7be5c-105">Header Changes</span></span>

<span data-ttu-id="7be5c-106">La libreria DirectXMath usa un nuovo set di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="7be5c-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="7be5c-107">Sostituire `xnamath.h` l'intestazione con `DirectXMath.h` e aggiungere per i tipi di `DirectXPackedVector.h` *GPU.*</span><span class="sxs-lookup"><span data-stu-id="7be5c-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="7be5c-108">I tipi di delimitazione dell'esempio Di collisione di DirectX SDK in fanno ora `xnacollision.h` parte della libreria DirectXMath in `DirectXCollision.h` .</span><span class="sxs-lookup"><span data-stu-id="7be5c-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="7be5c-109">Sono stati modificati per usare le classi C++ anziché un'API di tipo C.</span><span class="sxs-lookup"><span data-stu-id="7be5c-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="7be5c-110">Modifiche costanti</span><span class="sxs-lookup"><span data-stu-id="7be5c-110">Constant Changes</span></span>

<span data-ttu-id="7be5c-111">XNAMATH \_ VERSION (200, 201, 202, 203, 204 e così via) è stato sostituito con DIRECXTMATH \_ VERSION (300, 301, 302, 303 e così via).</span><span class="sxs-lookup"><span data-stu-id="7be5c-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="7be5c-112">DirectXMath 3.00 e 3.02 sono disponibili con versioni preliminari del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7be5c-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="7be5c-113">DirectXMath 3.03 è nella versione finale di Windows 8 SDK.</span><span class="sxs-lookup"><span data-stu-id="7be5c-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="7be5c-114">Spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="7be5c-114">Namespaces</span></span>

<span data-ttu-id="7be5c-115">La libreria DirectXMath usa gli spazi dei nomi C++ per organizzare i tipi.</span><span class="sxs-lookup"><span data-stu-id="7be5c-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="7be5c-116">XNA Math ha usato solo lo spazio dei nomi globale.</span><span class="sxs-lookup"><span data-stu-id="7be5c-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="7be5c-117">I tipi DirectXMath in comune con i calcoli matematici XNA sono nello spazio dei nomi **DirectX** **o DirectX::P ackedVector.**</span><span class="sxs-lookup"><span data-stu-id="7be5c-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="7be5c-118">Nei file di origine C++ una soluzione semplice consiste nell'aggiungere `using` istruzioni .</span><span class="sxs-lookup"><span data-stu-id="7be5c-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="7be5c-119">Per le intestazioni, non è consigliabile aggiungere istruzioni using.</span><span class="sxs-lookup"><span data-stu-id="7be5c-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="7be5c-120">Aggiungere invece spazi dei nomi completi.</span><span class="sxs-lookup"><span data-stu-id="7be5c-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="7be5c-121">Caricamenti parziali</span><span class="sxs-lookup"><span data-stu-id="7be5c-121">Partial Loads</span></span>

<span data-ttu-id="7be5c-122">Per varie funzioni che caricano meno di 4 elementi di un XMVECTOR, la libreria matematica XNA ha lasciato gli elementi aggiuntivi indefiniti.</span><span class="sxs-lookup"><span data-stu-id="7be5c-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="7be5c-123">DirectXMath riempirà sempre questi elementi aggiuntivi con 0.</span><span class="sxs-lookup"><span data-stu-id="7be5c-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="7be5c-124">Rimozione di Xbox 360 tipi specifici</span><span class="sxs-lookup"><span data-stu-id="7be5c-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="7be5c-125">I tipi, le funzioni e le costanti della libreria matematica XNA seguenti non sono disponibili in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="7be5c-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="7be5c-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="7be5c-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="7be5c-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="7be5c-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="7be5c-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="7be5c-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="7be5c-129">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="7be5c-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="7be5c-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="7be5c-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="7be5c-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="7be5c-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="7be5c-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="7be5c-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="7be5c-133">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="7be5c-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="7be5c-134">\_\_vector4i è deprecato.</span><span class="sxs-lookup"><span data-stu-id="7be5c-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="7be5c-135">Usare [**invece XMVECTORI32**](xmvectori32-data-type.md) [**o XMVECTORU32.**](xmvectoru32-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="7be5c-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="7be5c-136">Le funzioni e i tipi seguenti sono deprecati perché sono solo Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="7be5c-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="7be5c-137">Intrinseci ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="7be5c-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="7be5c-138">La dichiarazione di una costante di vettore con questo codice verrà compilata per XNA Math per SSE e NO-INTRINSICS, ma avrà esito negativo per DirectXMath tramite ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="7be5c-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="7be5c-139">In generale, non è consigliabile usare questo metodo di inizializzazione di [**XMVECTOR.**](xmvector-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="7be5c-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="7be5c-140">Tuttavia, se si vuole una costante vettore, la classe [**XMVECTORF32**](xmvectorf32-data-type.md) supporta questo stile di inizializzazione e restituisce automaticamente il tipo **XMVECTOR** in modo da poter usare **XMVECTORF32** nella maggior parte degli stessi contesti.</span><span class="sxs-lookup"><span data-stu-id="7be5c-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="7be5c-141">Per qualsiasi operazione di scrittura in **una classe XMVECTORF32** è necessario fare riferimento in modo esplicito al membro **XMVECTOR** .v.</span><span class="sxs-lookup"><span data-stu-id="7be5c-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="7be5c-142">Permuta</span><span class="sxs-lookup"><span data-stu-id="7be5c-142">Permute</span></span>

<span data-ttu-id="7be5c-143">La libreria matematica XNA aveva il formato seguente per la permuta vettore generale:</span><span class="sxs-lookup"><span data-stu-id="7be5c-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="7be5c-144">Per DirectXMath, **XMVectorPermuteControl** è stato eliminato e XM \_ PERMUTE \_ 0X .</span><span class="sxs-lookup"><span data-stu-id="7be5c-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="7be5c-145">Le costanti \_ XM PERMUTE 1Z sono state ridefinite in modo da \_ essere semplici indici 0-7.</span><span class="sxs-lookup"><span data-stu-id="7be5c-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="7be5c-146">Ecco la nuova firma per [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)</span><span class="sxs-lookup"><span data-stu-id="7be5c-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="7be5c-147">Anziché una parola di controllo, questa funzione accetta direttamente i 4 indici come parametri, il che lo rende analogo alla funzione [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando il nuovo XM \_ SWIZZLE \_ X .</span><span class="sxs-lookup"><span data-stu-id="7be5c-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="7be5c-148">Costanti \_ XM SWIZZLE \_ W definite come indici 0-3 semplici.</span><span class="sxs-lookup"><span data-stu-id="7be5c-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="7be5c-149">Per i valori costanti, esiste un modo molto più efficiente per implementare permute.</span><span class="sxs-lookup"><span data-stu-id="7be5c-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="7be5c-150">Invece di usare il formato di funzione [**di XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)usare il **formato modello:**</span><span class="sxs-lookup"><span data-stu-id="7be5c-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="7be5c-151">Moduli modello</span><span class="sxs-lookup"><span data-stu-id="7be5c-151">Template Forms</span></span>

<span data-ttu-id="7be5c-152">In generale, l'uso di un modulo modello su una forma di funzione delle funzioni seguenti è molto più efficiente e consente alla libreria di eseguire ottimizzazioni specifiche della piattaforma tramite la specializzazione dei modelli.</span><span class="sxs-lookup"><span data-stu-id="7be5c-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a><span data-ttu-id="7be5c-153">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="7be5c-153">Eliminated Functions</span></span>

| <span data-ttu-id="7be5c-154">Funzione eliminata</span><span class="sxs-lookup"><span data-stu-id="7be5c-154">Eliminated Function</span></span>        | <span data-ttu-id="7be5c-155">Sostituzione</span><span class="sxs-lookup"><span data-stu-id="7be5c-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be5c-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="7be5c-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="7be5c-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="7be5c-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="7be5c-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="7be5c-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="7be5c-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="7be5c-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="7be5c-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="7be5c-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="7be5c-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="7be5c-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="7be5c-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="7be5c-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="7be5c-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="7be5c-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="7be5c-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="7be5c-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="7be5c-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="7be5c-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="7be5c-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="7be5c-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="7be5c-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="7be5c-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="7be5c-168">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="7be5c-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="7be5c-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="7be5c-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="7be5c-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="7be5c-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="7be5c-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="7be5c-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="7be5c-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="7be5c-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="7be5c-173">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="7be5c-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="7be5c-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="7be5c-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="7be5c-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="7be5c-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="7be5c-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="7be5c-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="7be5c-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="7be5c-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="7be5c-178">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="7be5c-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="7be5c-179">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="7be5c-180">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="7be5c-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="7be5c-181">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="7be5c-182">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="7be5c-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="7be5c-183">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="7be5c-184">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="7be5c-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="7be5c-185">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="7be5c-186">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="7be5c-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="7be5c-187">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="7be5c-188">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="7be5c-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="7be5c-189">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="7be5c-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="7be5c-190">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="7be5c-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="7be5c-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7be5c-191">Related topics</span></span>

[<span data-ttu-id="7be5c-192">Guida per programmatori DirectXMath</span><span class="sxs-lookup"><span data-stu-id="7be5c-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
