---
description: Tipo portabile usato per rappresentare un vettore di componenti a virgola mobile o Integer a 4 32 bit, ognuno allineato in modo ottimale e mappato a un registro di vettori hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo di dati XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324359"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="ce002-103">Tipo di dati XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="ce002-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="ce002-104">Tipo portabile usato per rappresentare un vettore di componenti a virgola mobile o Integer a 4 32 bit, ognuno allineato in modo ottimale e mappato a un registro di vettori hardware.</span><span class="sxs-lookup"><span data-stu-id="ce002-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce002-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce002-105">Remarks</span></span>

<span data-ttu-id="ce002-106">Per un elenco di funzionalità aggiuntive, ad esempio costruttori e operatori, disponibili con `XMVECTOR` durante la programmazione in C++, vedere [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ce002-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="ce002-107">Nella libreria DirectXMath, per supportare completamente la portabilità e l'ottimizzazione, `XMVECTOR` è, per progettazione, un tipo opaco.</span><span class="sxs-lookup"><span data-stu-id="ce002-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="ce002-108">L'implementazione effettiva di `XMVECTOR` è dipendente dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ce002-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="ce002-109">In generale, il codice non deve basarsi sulle specifiche di una determinata implementazione specifica della piattaforma `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="ce002-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="ce002-110">Le implementazioni specifiche della piattaforma hanno queste caratteristiche:</span><span class="sxs-lookup"><span data-stu-id="ce002-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="ce002-111">Non sono portabili.</span><span class="sxs-lookup"><span data-stu-id="ce002-111">They are not portable.</span></span>
-   <span data-ttu-id="ce002-112">Potrebbero variare tra le versioni.</span><span class="sxs-lookup"><span data-stu-id="ce002-112">They may change between releases.</span></span>
-   <span data-ttu-id="ce002-113">L'uso incauto dei dettagli dell'implementazione potrebbe non essere ottimale.</span><span class="sxs-lookup"><span data-stu-id="ce002-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="ce002-114">Gli sviluppatori devono usare le funzioni di [accesso](ovw-xnamath-reference-functions-accessors.md), [caricamento](ovw-xnamath-reference-functions-load.md)e [archiviazione](ovw-xnamath-reference-functions-storage.md) della libreria DirectXMath per ottenere e impostare i vettori e le [funzioni di vettore 4D della libreria DirectXMath](ovw-xnamath-reference-functions-vector4.md) per modificarle.</span><span class="sxs-lookup"><span data-stu-id="ce002-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="ce002-115">Per i progetti che richiedono informazioni dettagliate su come implementare `XMVECTOR` su piattaforme diverse, vedere elementi [interni della libreria](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="ce002-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="ce002-116">Alias del compilatore</span><span class="sxs-lookup"><span data-stu-id="ce002-116">Compiler Aliases</span></span>

<span data-ttu-id="ce002-117">Il file di intestazione DirectXMath. h usa alias per l' `XMVECTOR` oggetto, in particolare **CXMVECTOR** e **FXMVECTOR**.</span><span class="sxs-lookup"><span data-stu-id="ce002-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="ce002-118">L'intestazione utilizza questi alias per conformarsi alle convenzioni di chiamata inline ottimali di compilatori diversi.</span><span class="sxs-lookup"><span data-stu-id="ce002-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="ce002-119">Per la maggior parte dei progetti che usano DirectXMath è sufficiente considerare questi tipi come un alias esatto a `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="ce002-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="ce002-120">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="ce002-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="ce002-121">Per i progetti che richiedono informazioni dettagliate su come diverse piattaforme gestiscono le convenzioni di chiamata, vedere elementi [interni della libreria](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="ce002-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="ce002-122">Per XNAMATH 2. x, il `XMVECTOR` tipo di dati include i membri dell'elemento. x,. y,. z,. e. w, che in genere provocano una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ce002-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="ce002-123">L'uso del tipo XM \_ strict \_ VECTOR4 fornisce un consenso esplicito per la definizione DirectXMath di un tipo di dati opaco.</span><span class="sxs-lookup"><span data-stu-id="ce002-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="ce002-124">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="ce002-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ce002-125">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="ce002-125">Platform Requirements</span></span>

<span data-ttu-id="ce002-126">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce002-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ce002-127">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ce002-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce002-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce002-128">Requirements</span></span>



| <span data-ttu-id="ce002-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce002-129">Requirement</span></span> | <span data-ttu-id="ce002-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ce002-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce002-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce002-131">Header</span></span><br/> | <dl> <span data-ttu-id="ce002-132"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce002-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce002-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce002-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce002-134">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ce002-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="ce002-135">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="ce002-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ce002-136">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="ce002-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ce002-137">**Tipo di dati XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="ce002-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ce002-138">**Tipo di dati XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="ce002-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="ce002-139">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="ce002-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




