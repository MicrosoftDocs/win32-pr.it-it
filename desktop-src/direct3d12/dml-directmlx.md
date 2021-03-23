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
# <a name="directmlx"></a>DirectMLX

DirectMLX è una libreria helper solo per l'intestazione C++ per DirectML, progettata per semplificare la composizione dei singoli operatori nei grafici.

DirectMLX fornisce pratici wrapper per tutti i tipi di operatore DirectML (DML), nonché gli overload di operatore intuitivi, che rendono più semplice creare un'istanza degli operatori DML e concatenarli in grafici complessi.

## <a name="where-to-find-directmlxh"></a>Dove trovare `DirectMLX.h`

`DirectMLX.h` viene distribuito come software open source con la licenza MIT. La versione più recente è disponibile in [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).

## <a name="tensor-constraints"></a>Vincoli tensore

DirectMLX richiede DirectML versione 1.4.0 o successive (vedere la [cronologia delle versioni di DirectML](dml-version-history.md#version-table)). Le versioni precedenti di DirectML non sono supportate.

DirectMLX. h richiede un compilatore che supporta C + 11, tra cui:

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Si noti che un compilatore C++ 17 (o versione successiva) è l'opzione consigliata. La compilazione per C++ 11 è possibile, ma richiede l'uso di librerie di terze parti, ad esempio [GSL](https://github.com/microsoft/GSL) e [calata](https://github.com/abseil/abseil-cpp), per sostituire le funzionalità della libreria standard mancanti.

Se si ha una configurazione che non viene compilata correttamente `DirectMLX.h` , inviare [un problema in GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Utilizzo di base

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

Di seguito è riportato un altro esempio in cui viene creato un grafo DirectML in grado di calcolare la [Formula quadratica](https://en.wikipedia.org/wiki/Quadratic_formula).

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

## <a name="more-examples"></a>Altri esempi

Gli esempi completi che usano DirectMLX sono disponibili nel [repository GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).

## <a name="compile-time-options"></a>Opzioni di Compile-Time

DirectMLX supporta la #define in fase di compilazione per personalizzare le varie parti dell'intestazione.

|Opzione|Descrizione|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Se #define, fa in modo che gli errori provochino una chiamata a `std::abort` anziché generare un'eccezione. Questa impostazione viene definita per impostazione predefinita se le eccezioni non sono disponibili, ad esempio se le eccezioni sono state disabilitate nelle opzioni del compilatore.|
|**DMLX_USE_WIL**|Se #define, le eccezioni vengono generate utilizzando i tipi di eccezione della [libreria di implementazione di Windows](https://github.com/microsoft/wil) . In caso contrario, vengono utilizzati i tipi di eccezione standard (ad esempio `std::runtime_error` ). Questa opzione non ha alcun effetto se **DMLX_NO_EXCEPTIONS** è definito.|
|**DMLX_USE_ABSEIL**|Se #define, USA [calata](https://github.com/abseil/abseil-cpp) come sostituzioni per i tipi di libreria standard non disponibili in c++ 11. Questi tipi includono `absl::optional` (al posto di `std::optional` ), `absl::Span` (al posto di `std::span` ) e `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Controlla se usare [GSL](https://github.com/microsoft/GSL) come sostituzione per `std::span` . Se #define, gli utilizzi di `std::span` vengono sostituiti da `gsl::span` nei compilatori senza `std::span` implementazioni native. In caso contrario, viene invece fornita un'implementazione inline a discesa. Si noti che questa opzione viene usata solo quando si esegue la compilazione in un compilatore precedente a C + + 20 senza supporto per `std::span` e quando non è in uso nessun altro rimpiazzo della libreria standard (come calata).|

## <a name="controlling-tensor-layout"></a>Controllo del layout del tensore

Per la maggior parte degli operatori, DirectMLX calcola le proprietà dei tempi di output dell'operatore per conto dell'utente. Ad esempio, quando si esegue una `dml::Reduce` su più assi `{ 0, 2, 3 }` con un tensore di input di dimensioni `{ 3, 4, 5, 6 }` , DirectMLX calcolerà automaticamente le proprietà del tensore di output, inclusa la forma corretta di `{ 1, 4, 1, 1 }` .

Tuttavia, le altre proprietà di un tensore di output includono *Strides*, *TotalTensorSizeInBytes* e *GuaranteedBaseOffsetAlignment*. Per impostazione predefinita, DirectMLX imposta queste proprietà in modo che il tensore non abbia grandi passi, nessun allineamento di offset di base garantito e una dimensione del tensore totale in byte calcolata da [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

DirectMLX supporta la possibilità di personalizzare queste proprietà del tensore di output, usando oggetti noti come *criteri Tensor*. Un **TensorPolicy** è un callback personalizzabile che viene richiamato da DirectMLX e restituisce le proprietà del tensore di output, date le dimensioni, i flag e il tipo di dati calcolati del tensore.

I criteri di tensore possono essere impostati sull'oggetto **DML:: scope** e verranno usati per tutti gli operatori successivi del grafo. I criteri di tensore possono anche essere impostati direttamente quando si costruisce un **TensorDesc**.

Il layout dei tensori prodotti da DirectMLX può pertanto essere controllato impostando un **TensorPolicy** che imposta gli stride appropriati nei propri tensori.

### <a name="example-1"></a>Esempio 1

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

### <a name="example-2"></a>Esempio 2

DirectMLX fornisce anche alcuni criteri di tensore alternativi predefiniti. Il criterio **InterleavedChannel** , ad esempio, viene fornito per praticità e può essere usato per produrre i tensori con stride in modo che vengano scritti in ordine NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Vedi anche

* [GitHub DirectML](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Esempio DirectMLX yolov4](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Uso di stride per esprimere il layout di riempimento e memoria](./dml-strides.md)
* [Struttura DML_GRAPH_DESC](./directml/ns-directml-dml_graph_desc.md)