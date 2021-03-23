---
title: DirectMLX
description: DirectMLX è una libreria helper solo per l'intestazione C++ per DirectML, progettata per semplificare la composizione dei singoli operatori nei grafici.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548911"
---
# <a name="directmlx"></a><span data-ttu-id="1144c-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="1144c-103">DirectMLX</span></span>

<span data-ttu-id="1144c-104">DirectMLX è una libreria helper solo per l'intestazione C++ per DirectML, progettata per semplificare la composizione dei singoli operatori nei grafici.</span><span class="sxs-lookup"><span data-stu-id="1144c-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="1144c-105">DirectMLX fornisce pratici wrapper per tutti i tipi di operatore DirectML (DML), nonché gli overload di operatore intuitivi, che rendono più semplice creare un'istanza degli operatori DML e concatenarli in grafici complessi.</span><span class="sxs-lookup"><span data-stu-id="1144c-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="1144c-106">Dove trovare `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="1144c-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="1144c-107">`DirectMLX.h` viene distribuito come software open source con la licenza MIT.</span><span class="sxs-lookup"><span data-stu-id="1144c-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="1144c-108">La versione più recente è disponibile in [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span><span class="sxs-lookup"><span data-stu-id="1144c-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1144c-109">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="1144c-109">Tensor constraints</span></span>

<span data-ttu-id="1144c-110">DirectMLX richiede DirectML versione 1.4.0 o successive (vedere la [cronologia delle versioni di DirectML](dml-version-history.md#version-table)).</span><span class="sxs-lookup"><span data-stu-id="1144c-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="1144c-111">Le versioni precedenti di DirectML non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="1144c-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="1144c-112">DirectMLX. h richiede un compilatore che supporta C + 11, tra cui:</span><span class="sxs-lookup"><span data-stu-id="1144c-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="1144c-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="1144c-113">Visual Studio 2017</span></span>
* <span data-ttu-id="1144c-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="1144c-114">Visual Studio 2019</span></span>
* <span data-ttu-id="1144c-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="1144c-115">Clang 10</span></span>

<span data-ttu-id="1144c-116">Si noti che un compilatore C++ 17 (o versione successiva) è l'opzione consigliata.</span><span class="sxs-lookup"><span data-stu-id="1144c-116">Note that a C++17 (or newer) compiler is options that we recommend.</span></span> <span data-ttu-id="1144c-117">La compilazione per C++ 11 è possibile, ma richiede l'uso di librerie di terze parti, ad esempio [GSL](https://github.com/microsoft/GSL) e [calata](https://github.com/abseil/abseil-cpp), per sostituire le funzionalità della libreria standard mancanti.</span><span class="sxs-lookup"><span data-stu-id="1144c-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="1144c-118">Se si ha una configurazione che non viene compilata correttamente `DirectMLX.h` , inviare [un problema in GitHub](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="1144c-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="1144c-119">Utilizzo di base</span><span class="sxs-lookup"><span data-stu-id="1144c-119">Basic Usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="1144c-120">Di seguito è riportato un altro esempio in cui viene creato un grafo DirectML in grado di calcolare la [Formula quadratica](https://en.wikipedia.org/wiki/Quadratic_formula).</span><span class="sxs-lookup"><span data-stu-id="1144c-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="1144c-121">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="1144c-121">More examples</span></span>

<span data-ttu-id="1144c-122">Gli esempi completi che usano DirectMLX sono disponibili nel [repository GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).</span><span class="sxs-lookup"><span data-stu-id="1144c-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="1144c-123">Opzioni di Compile-Time</span><span class="sxs-lookup"><span data-stu-id="1144c-123">Compile-Time Options</span></span>

<span data-ttu-id="1144c-124">DirectMLX supporta la #define in fase di compilazione per personalizzare le varie parti dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="1144c-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="1144c-125">Opzione</span><span class="sxs-lookup"><span data-stu-id="1144c-125">Option</span></span>|<span data-ttu-id="1144c-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1144c-126">Description</span></span>|
|-|-|
|<span data-ttu-id="1144c-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="1144c-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="1144c-128">Se #define, fa in modo che gli errori provochino una chiamata a `std::abort` anziché generare un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="1144c-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="1144c-129">Questa impostazione viene definita per impostazione predefinita se le eccezioni non sono disponibili, ad esempio se le eccezioni sono state disabilitate nelle opzioni del compilatore.</span><span class="sxs-lookup"><span data-stu-id="1144c-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="1144c-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="1144c-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="1144c-131">Se #define, le eccezioni vengono generate utilizzando i tipi di eccezione della [libreria di implementazione di Windows](https://github.com/microsoft/wil) .</span><span class="sxs-lookup"><span data-stu-id="1144c-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="1144c-132">In caso contrario, vengono utilizzati i tipi di eccezione standard (ad esempio `std::runtime_error` ).</span><span class="sxs-lookup"><span data-stu-id="1144c-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="1144c-133">Questa opzione non ha alcun effetto se **DMLX_NO_EXCEPTIONS** è definito.</span><span class="sxs-lookup"><span data-stu-id="1144c-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="1144c-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="1144c-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="1144c-135">Se #define, USA [calata](https://github.com/abseil/abseil-cpp) come sostituzioni per i tipi di libreria standard non disponibili in c++ 11.</span><span class="sxs-lookup"><span data-stu-id="1144c-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="1144c-136">Questi tipi includono `absl::optional` (al posto di `std::optional` ), `absl::Span` (al posto di `std::span` ) e `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="1144c-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="1144c-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="1144c-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="1144c-138">Controlla se usare [GSL](https://github.com/microsoft/GSL) come sostituzione per `std::span` .</span><span class="sxs-lookup"><span data-stu-id="1144c-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="1144c-139">Se #define, gli utilizzi di `std::span` vengono sostituiti da `gsl::span` nei compilatori senza `std::span` implementazioni native.</span><span class="sxs-lookup"><span data-stu-id="1144c-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="1144c-140">In caso contrario, viene invece fornita un'implementazione inline a discesa.</span><span class="sxs-lookup"><span data-stu-id="1144c-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="1144c-141">Si noti che questa opzione viene usata solo quando si esegue la compilazione in un compilatore precedente a C + + 20 senza supporto per `std::span` e quando non è in uso nessun altro rimpiazzo della libreria standard (come calata).</span><span class="sxs-lookup"><span data-stu-id="1144c-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="1144c-142">Controllo del layout del tensore</span><span class="sxs-lookup"><span data-stu-id="1144c-142">Controlling Tensor Layout</span></span>

<span data-ttu-id="1144c-143">Per la maggior parte degli operatori, DirectMLX calcola le proprietà dei tempi di output dell'operatore per conto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1144c-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="1144c-144">Ad esempio, quando si esegue una `dml::Reduce` su più assi `{ 0, 2, 3 }` con un tensore di input di dimensioni `{ 3, 4, 5, 6 }` , DirectMLX calcolerà automaticamente le proprietà del tensore di output, inclusa la forma corretta di `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="1144c-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="1144c-145">Tuttavia, le altre proprietà di un tensore di output includono *Strides*, *TotalTensorSizeInBytes* e *GuaranteedBaseOffsetAlignment*.</span><span class="sxs-lookup"><span data-stu-id="1144c-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="1144c-146">Per impostazione predefinita, DirectMLX imposta queste proprietà in modo che il tensore non abbia grandi passi, nessun allineamento di offset di base garantito e una dimensione del tensore totale in byte calcolata da [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span><span class="sxs-lookup"><span data-stu-id="1144c-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="1144c-147">DirectMLX supporta la possibilità di personalizzare queste proprietà del tensore di output, usando oggetti noti come *criteri Tensor*.</span><span class="sxs-lookup"><span data-stu-id="1144c-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="1144c-148">Un **TensorPolicy** è un callback personalizzabile che viene richiamato da DirectMLX e restituisce le proprietà del tensore di output, date le dimensioni, i flag e il tipo di dati calcolati del tensore.</span><span class="sxs-lookup"><span data-stu-id="1144c-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="1144c-149">I criteri di tensore possono essere impostati sull'oggetto **DML:: scope** e verranno usati per tutti gli operatori successivi del grafo.</span><span class="sxs-lookup"><span data-stu-id="1144c-149">Tensor policies can be set on the **dml::Scope** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="1144c-150">I criteri di tensore possono anche essere impostati direttamente quando si costruisce un **TensorDesc**.</span><span class="sxs-lookup"><span data-stu-id="1144c-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="1144c-151">Il layout dei tensori prodotti da DirectMLX può pertanto essere controllato impostando un **TensorPolicy** che imposta gli stride appropriati nei propri tensori.</span><span class="sxs-lookup"><span data-stu-id="1144c-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="1144c-152">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1144c-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="1144c-153">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1144c-153">Example 2</span></span>

<span data-ttu-id="1144c-154">DirectMLX fornisce anche alcuni criteri di tensore alternativi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="1144c-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="1144c-155">Il criterio **InterleavedChannel** , ad esempio, viene fornito per praticità e può essere usato per produrre i tensori con stride in modo che vengano scritti in ordine NHWC.</span><span class="sxs-lookup"><span data-stu-id="1144c-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="1144c-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1144c-156">See also</span></span>

* [<span data-ttu-id="1144c-157">GitHub DirectML</span><span class="sxs-lookup"><span data-stu-id="1144c-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="1144c-158">Esempio DirectMLX yolov4</span><span class="sxs-lookup"><span data-stu-id="1144c-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="1144c-159">Uso di stride per esprimere il layout di riempimento e memoria</span><span class="sxs-lookup"><span data-stu-id="1144c-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="1144c-160">Struttura DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="1144c-160">DML_GRAPH_DESC structure</span></span>](./directml/ns-directml-dml_graph_desc.md)