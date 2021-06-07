---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Riempie un tensore di output con bit generati in modo deterministico, pseudocasa e distribuiti in modo uniforme. Facoltativamente, questo operatore può anche ottenere uno stato del generatore interno aggiornato, che può essere usato durante le esecuzioni successive dell'operatore.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417457"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="61dfa-104">DML_RANDOM_GENERATOR_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="61dfa-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="61dfa-105">Riempie un tensore di output con bit generati in modo deterministico, pseudocasa e distribuiti in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="61dfa-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="61dfa-106">Facoltativamente, questo operatore può anche ottenere uno stato del generatore interno aggiornato, che può essere usato durante le esecuzioni successive dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="61dfa-107">Questo operatore è deterministico e si comporta come se fosse una funzione pura, cio' la sua esecuzione non produce effetti collaterali e non usa &mdash; alcuno stato globale.</span><span class="sxs-lookup"><span data-stu-id="61dfa-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="61dfa-108">L'output pseudo-casuale prodotto da questo operatore dipende esclusivamente dai valori forniti in *InputStateTensor.*</span><span class="sxs-lookup"><span data-stu-id="61dfa-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="61dfa-109">I generatori implementati da questo operatore non sono crittograficamente sicuri; Pertanto, questo operatore non deve essere usato per la crittografia, la generazione di chiavi o altre applicazioni che richiedono la generazione di numeri casuali crittograficamente sicuri.</span><span class="sxs-lookup"><span data-stu-id="61dfa-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61dfa-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="61dfa-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="61dfa-111">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="61dfa-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="61dfa-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61dfa-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="61dfa-113">Members</span><span class="sxs-lookup"><span data-stu-id="61dfa-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="61dfa-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="61dfa-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="61dfa-115">Tensore di input contenente lo stato interno del generatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="61dfa-116">Le dimensioni e il formato di questo tensore di input dipendono dal [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span><span class="sxs-lookup"><span data-stu-id="61dfa-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="61dfa-117">Per **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, questo tensore deve essere di tipo **UINT32** e avere dimensioni `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="61dfa-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="61dfa-118">I primi quattro valori a 32 bit contengono un contatore a 128 bit a incremento costante.</span><span class="sxs-lookup"><span data-stu-id="61dfa-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="61dfa-119">Gli ultimi due valori a 32 bit contengono il valore della chiave a 64 bit per il generatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="61dfa-120">Quando si inizializza lo stato di input del generatore per la prima volta, in genere il contatore a 128 bit (i primi quattro valori UINT32 a 32 bit) deve essere inizializzato su 0.</span><span class="sxs-lookup"><span data-stu-id="61dfa-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="61dfa-121">La chiave può essere scelta in modo arbitrario. valori di chiave diversi produrranno sequenze di numeri diverse.</span><span class="sxs-lookup"><span data-stu-id="61dfa-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="61dfa-122">Il valore della chiave viene in genere generato utilizzando un valore di seed *specificato dall'utente.*</span><span class="sxs-lookup"><span data-stu-id="61dfa-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="61dfa-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="61dfa-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="61dfa-124">Tensore di output che contiene i valori pseudocasy risultanti.</span><span class="sxs-lookup"><span data-stu-id="61dfa-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="61dfa-125">Questo tensore può essere di qualsiasi dimensione.</span><span class="sxs-lookup"><span data-stu-id="61dfa-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="61dfa-126">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="61dfa-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="61dfa-127">Tensore di output facoltativo che contiene lo stato del generatore interno aggiornato.</span><span class="sxs-lookup"><span data-stu-id="61dfa-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="61dfa-128">Se specificato, questo operatore usa *InputStateTensor* per calcolare uno stato del generatore aggiornato appropriato e scrive il risultato in *OutputStateTensor.*</span><span class="sxs-lookup"><span data-stu-id="61dfa-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="61dfa-129">In genere, i chiamanti salvano questo risultato e lo forniscono come stato di input in una successiva esecuzione di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="61dfa-130">Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="61dfa-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="61dfa-131">Uno dei valori [dell'enumerazione DML_RANDOM_GENERATOR_TYPE,](./ne-directml-dml_random_generator_type.md) che indica il tipo di generatore da usare.</span><span class="sxs-lookup"><span data-stu-id="61dfa-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="61dfa-132">Attualmente l'unico valore valido **è DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, che genera numeri pseudo-casuali in base all'algoritmo [Diox 4x32-10.](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)</span><span class="sxs-lookup"><span data-stu-id="61dfa-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="61dfa-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="61dfa-133">Remarks</span></span>
<span data-ttu-id="61dfa-134">A ogni esecuzione di questo operatore, il contatore a 128 bit deve essere incrementato.</span><span class="sxs-lookup"><span data-stu-id="61dfa-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="61dfa-135">Se viene *specificato OutputStateTensor,* questo operatore incrementa il contatore con il valore corretto per conto dell'utente e scrive il risultato in *OutputStateTensor.*</span><span class="sxs-lookup"><span data-stu-id="61dfa-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="61dfa-136">La quantità di cui deve essere incrementata dipende dal numero di elementi di output a 32 bit generati e dal tipo del generatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="61dfa-137">Per **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, il contatore a 128 bit deve essere incrementato di a ogni esecuzione, dove è il numero di elementi `ceil(outputSize / 4)` in `outputSize` *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="61dfa-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="61dfa-138">Si consideri un esempio in cui il valore del contatore a 128 bit è attualmente e la dimensione `0x48656c6c'6f46726f'6d536561'74746c65` di OutputTensor è `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="61dfa-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="61dfa-139">Dopo aver eseguito l'operatore una volta, il contatore deve essere incrementato di 324.855 (il numero di elementi di output generati diviso per 4, arrotondato per esecuzione) con conseguente valore del contatore pari a `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="61dfa-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="61dfa-140">Questo valore aggiornato deve quindi essere fornito come input per la successiva esecuzione di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="61dfa-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="61dfa-141">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="61dfa-141">Availability</span></span>
<span data-ttu-id="61dfa-142">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="61dfa-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="61dfa-143">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="61dfa-143">Tensor constraints</span></span>
<span data-ttu-id="61dfa-144">`InputStateTensor` e `OutputStateTensor` devono avere le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="61dfa-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="61dfa-145">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="61dfa-145">Tensor support</span></span>
| <span data-ttu-id="61dfa-146">Tensore</span><span class="sxs-lookup"><span data-stu-id="61dfa-146">Tensor</span></span> | <span data-ttu-id="61dfa-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="61dfa-147">Kind</span></span> | <span data-ttu-id="61dfa-148">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="61dfa-148">Dimensions</span></span> | <span data-ttu-id="61dfa-149">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="61dfa-149">Supported dimension counts</span></span> | <span data-ttu-id="61dfa-150">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="61dfa-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="61dfa-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="61dfa-151">InputStateTensor</span></span> | <span data-ttu-id="61dfa-152">Input</span><span class="sxs-lookup"><span data-stu-id="61dfa-152">Input</span></span> | <span data-ttu-id="61dfa-153">{ 1, 1, 1, 6 }</span><span class="sxs-lookup"><span data-stu-id="61dfa-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="61dfa-154">4</span><span class="sxs-lookup"><span data-stu-id="61dfa-154">4</span></span> | <span data-ttu-id="61dfa-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="61dfa-155">UINT32</span></span> |
| <span data-ttu-id="61dfa-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="61dfa-156">OutputTensor</span></span> | <span data-ttu-id="61dfa-157">Output</span><span class="sxs-lookup"><span data-stu-id="61dfa-157">Output</span></span> | <span data-ttu-id="61dfa-158">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="61dfa-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="61dfa-159">4</span><span class="sxs-lookup"><span data-stu-id="61dfa-159">4</span></span> | <span data-ttu-id="61dfa-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="61dfa-160">UINT32</span></span> |
| <span data-ttu-id="61dfa-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="61dfa-161">OutputStateTensor</span></span> | <span data-ttu-id="61dfa-162">Output facoltativo</span><span class="sxs-lookup"><span data-stu-id="61dfa-162">Optional output</span></span> | <span data-ttu-id="61dfa-163">{ 1, 1, 1, 6 }</span><span class="sxs-lookup"><span data-stu-id="61dfa-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="61dfa-164">4</span><span class="sxs-lookup"><span data-stu-id="61dfa-164">4</span></span> | <span data-ttu-id="61dfa-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="61dfa-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="61dfa-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61dfa-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="61dfa-167">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="61dfa-167">**Header**</span></span> | <span data-ttu-id="61dfa-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="61dfa-168">directml.h</span></span> |