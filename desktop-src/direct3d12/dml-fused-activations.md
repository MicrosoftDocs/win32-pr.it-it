---
title: Utilizzo di operatori con fusibile per migliorare le prestazioni
description: Alcuni operatori DirectML supportano un concetto noto come *Fusion*. Operator Fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che vengano eseguiti insieme senza richiedere un round trip alla memoria.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548912"
---
# <a name="using-fused-operators-to-improve-performance"></a>Utilizzo di operatori con fusibile per migliorare le prestazioni

Alcuni operatori DirectML supportano un concetto noto come *Fusion*. Operator Fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che vengano eseguiti insieme senza richiedere un round trip alla memoria.

## <a name="when-to-fuse-activations"></a>Quando è possibile fondere le attivazioni

Le attivazioni fuse sono un'ottimizzazione delle prestazioni. Uno scenario estremamente comune in molti modelli di Machine Learning (ML) consiste nell'applicare una non linearità (funzione di attivazione) all'output di ogni livello nel modello.

In genere, è necessario un round trip alla memoria grafica. Se, ad esempio, una convoluzione è seguita da un'attivazione relu non fusa, la GPU deve attendere che i risultati della convoluzione vengano scritti nella memoria GPU prima di poter iniziare a calcolare il livello di attivazione di relu. Poiché il carico di lavoro di calcolo della maggior parte delle funzioni di attivazione tende a essere ridotto, questo round trip alla memoria grafica può costituire un collo di bottiglia delle prestazioni.

Operator Fusion consente la funzione di attivazione (relu nell'esempio precedente) da eseguire come parte dell'operatore precedente (ad esempio, convoluzione). Questo consente alla GPU di calcolare la funzione di attivazione senza attendere che i risultati dell'operatore precedente vengano scritti in memoria &mdash; e che migliorino le prestazioni.

Poiché le attivazioni fuse producono lo stesso risultato, ma sono più veloci in molti casi, è consigliabile eliminare i livelli di attivazione fondendoli nell'operatore precedente laddove possibile.

## <a name="how-to-fuse-activations"></a>Come fondere le attivazioni

Gli operatori che supportano le attivazioni fuse hanno un parametro facoltativo aggiuntivo nel rispettivo struct operator, `const DML_OPERATOR_DESC* FusedActivation` . La convoluzione, ad esempio, supporta l'attivazione con fusibile e un *FusedActivation* corrispondente nella descrizione dell'operatore (vedere [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

Per fondere un'attivazione, costruire un [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) che descriva il tipo di attivazione da fondere. Ad esempio, per fondere una funzione Relu, il tipo di operatore corretto verrebbe [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Quando si crea la descrizione dell'operatore per la funzione di attivazione, è necessario impostare i parametri *InputTensor* e *OutputTensor* per la funzione Activation su **null**.

## <a name="example"></a>Esempio

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

Per un esempio completo, l'esempio [DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) usa attivazioni fuse per migliorare le prestazioni.

## <a name="operators-that-support-fused-activation"></a>Operatori che supportano l'attivazione con fusibile

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** e **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Attivazioni supportate per Fusion

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Gli operatori non inclusi nell'elenco non sono supportati per l'attivazione con fusione.

## <a name="see-also"></a>Vedi anche

[Esempio DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
