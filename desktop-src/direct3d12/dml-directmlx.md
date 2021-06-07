---
title: DirectMLX
description: DirectMLX è una libreria helper solo intestazione C++ per DirectML, progettata per semplificare la composizione di singoli operatori in grafi.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521188"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX è una libreria helper solo intestazione C++ per DirectML, progettata per semplificare la composizione di singoli operatori in grafi.

DirectMLX offre wrapper pratici per tutti i tipi di operatore DirectML (DML), nonché overload intuitivi degli operatori, che semplificano l'istanza degli operatori DML e la concatenazione in grafici complessi.

## <a name="where-to-find-directmlxh"></a>Dove trovare `DirectMLX.h`

`DirectMLX.h` viene distribuito come software open source con la licenza MIT. La versione più recente è disponibile in [GitHub DirectML.](https://github.com/microsoft/DirectML/tree/master/Libraries)

## <a name="tensor-constraints"></a>Vincoli tensore

DirectMLX richiede DirectML versione 1.4.0 o successiva (vedere Cronologia [delle versioni di DirectML](dml-version-history.md#version-table)). Le versioni precedenti di DirectML non sono supportate.

DirectMLX.h richiede un compilatore con supporto C++11, che include (ma non solo):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Si noti che un compilatore C++17 (o versione più recente) è l'opzione consigliata. La compilazione per C++11 è possibile, ma richiede l'uso di librerie di terze parti ( ad esempio [GSL](https://github.com/microsoft/GSL) e [Abseil](https://github.com/abseil/abseil-cpp)) per sostituire la funzionalità della libreria standard mancante.

Se si dispone di una configurazione che non riesce a compilare `DirectMLX.h` , [compilare un problema in GitHub.](https://github.com/microsoft/DirectML/issues)

## <a name="basic-usage"></a>Uso di base

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

Ecco un altro esempio, che crea un grafo DirectML in grado di calcolare la [formula quadratica](https://en.wikipedia.org/wiki/Quadratic_formula).

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

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>Altri esempi

Esempi completi con DirectMLX sono disponibili nel [repository GitHub di DirectML.](https://github.com/microsoft/DirectML/tree/master/Samples)

## <a name="compile-time-options"></a>Opzioni in fase di compilazione

DirectMLX supporta la compilazione in #define per personalizzare varie parti dell'intestazione.

|Opzione|Descrizione|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Se #define, gli errori generano una chiamata a anziché `std::abort` generare un'eccezione. Questa opzione viene definita per impostazione predefinita se le eccezioni non sono disponibili, ad esempio se le eccezioni sono state disabilitate nelle opzioni del compilatore.|
|**DMLX_USE_WIL**|Se #define, le eccezioni vengono generate usando i tipi di eccezione della libreria di implementazione di [Windows.](https://github.com/microsoft/wil) In caso contrario, vengono usati i tipi di eccezione standard ( `std::runtime_error` ad esempio ). Questa opzione non ha alcun effetto **se DMLX_NO_EXCEPTIONS** definito.|
|**DMLX_USE_ABSEIL**|Se #define, usa [Abseil](https://github.com/abseil/abseil-cpp) come sostituzione dell'elenco a discesa per i tipi di libreria standard non disponibili in C++11. Questi tipi includono `absl::optional` (al posto di `std::optional` ), `absl::Span` (al posto di `std::span` ) e `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Controlla se usare [GSL](https://github.com/microsoft/GSL) come sostituzione di `std::span` . Se #define, gli usi di `std::span` vengono sostituiti da `gsl::span` nei compilatori senza `std::span` implementazioni native. In caso contrario, viene invece fornita un'implementazione dell'elenco a discesa inline. Si noti che questa opzione viene usata solo quando si esegue la compilazione in un compilatore pre-C++20 senza supporto per e quando non è in uso alcuna altra sostituzione della libreria standard a discesa (ad esempio `std::span` Abseil).|

## <a name="controlling-tensor-layout"></a>Controllo del layout dei tensore

Per la maggior parte degli operatori, DirectMLX calcola le proprietà dei tensori di output dell'operatore per conto dell'utente. Ad esempio, quando si esegue un tra assi con un tensore di input di dimensioni `dml::Reduce` `{ 0, 2, 3 }` , `{ 3, 4, 5, 6 }` DirectMLX calcola automaticamente le proprietà del tensore di output, inclusa la forma corretta di `{ 1, 4, 1, 1 }` .

Tuttavia, le altre proprietà di un tensore di output includono *Strides*, *TotalTensorSizeInBytes* e *GuaranteedBaseOffsetAlignment*. Per impostazione predefinita, DirectMLX imposta queste proprietà in modo che il tensore non abbia un allineamento di offset di base garantito e una dimensione totale del tensore in byte calcolata da [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

DirectMLX supporta la possibilità di personalizzare queste proprietà del tensore di output, usando oggetti noti come *criteri tensore.* **TensorPolicy** è un callback personalizzabile richiamato da DirectMLX e restituisce le proprietà del tensore di output in base al tipo di dati, ai flag e alle dimensioni calcolati di un tensore.

I criteri tensor possono essere impostati **nell'oggetto dml::Graph** e verranno usati per tutti gli operatori successivi in tale grafico. I criteri tensor possono anche essere impostati direttamente durante la costruzione di **un oggetto TensorDesc**.

Il layout dei tensori prodotti da DirectMLX può quindi essere controllato impostando **un oggetto TensorPolicy** che imposta i passi appropriati sui tensori.

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

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Esempio 2

DirectMLX offre anche alcuni criteri tensore alternativi predefiniti. Il **criterio InterleavedChannel,** ad esempio, viene fornito per praticità e può essere usato per produrre tensori con passi in modo che siano scritti in ordine NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Vedi anche

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Esempio di Yolov4 DirectMLX](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Uso di stride per esprimere spaziatura interna e layout di memoria](./dml-strides.md)
* [DML_GRAPH_DESC struttura](/windows/win32/api/directml/ns-directml-dml_graph_desc)