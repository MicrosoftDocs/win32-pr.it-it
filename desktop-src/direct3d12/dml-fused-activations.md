---
title: Uso di operatori fuse per migliorare le prestazioni
description: Alcuni operatori DirectML supportano un concetto noto come *fusion.* L'operatore fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che siano eseguiti insieme senza richiedere un roundtrip in memoria.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803993"
---
# <a name="using-fused-operators-to-improve-performance"></a>Uso di operatori fuse per migliorare le prestazioni

Alcuni operatori DirectML supportano un concetto noto come *fusion.* Operator Fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che siano eseguiti insieme senza richiedere un roundtrip in memoria.

## <a name="when-to-fuse-activations"></a>Quando unire le attivazioni

Le attivazioni fuse sono un'ottimizzazione delle prestazioni. Uno scenario estremamente comune in molti modelli di Machine Learning (ML) consiste nell'applicare una non lineare (una funzione di attivazione) all'output di ogni livello nel modello.

In genere, questa operazione richiede un roundtrip alla memoria grafica. Ad esempio, se una convoluzione è seguita da un'attivazione Relu non fusa, la GPU deve attendere che i risultati della convoluzione siano scritti nella memoria GPU prima di poter iniziare a calcolare il livello di attivazione di Relu. Poiché il carico di lavoro di calcolo della maggior parte delle funzioni di attivazione tende a essere ridotto, questo roundtrip alla memoria grafica può essere un collo di bottiglia delle prestazioni.

L'operatore fusion consente di eseguire la funzione di attivazione (Relu nell'esempio precedente) come parte dell'operatore precedente (ad esempio Convolution). Ciò consente alla GPU di calcolare la funzione di attivazione senza attendere che i risultati dell'operatore precedente siano scritti in memoria e che migliora &mdash; le prestazioni.

Poiché le attivazioni fuse producono lo stesso risultato, ma in molti casi sono più veloci, è consigliabile eliminare i livelli di attivazione fusandoli nell'operatore precedente, laddove possibile.

## <a name="how-to-fuse-activations"></a>Come unire le attivazioni

Gli operatori che supportano le attivazioni fuse hanno un parametro facoltativo aggiuntivo nello struct dell'operatore, `const DML_OPERATOR_DESC* FusedActivation` . La convoluzione, ad esempio, supporta l'attivazione fusa e ha *un fusedActivation* corrispondente nella descrizione dell'operatore [(vedere DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Per unire un'attivazione, costruire [un DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) che descrive il tipo di attivazione da unire. Ad esempio, per unire una funzione Relu, il tipo di operatore corretto sarà [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Quando si costruisce la descrizione dell'operatore per la funzione di attivazione, è necessario impostare i parametri *InputTensor* e *OutputTensor* per la funzione di attivazione su **NULL.**

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

Per un esempio completo, [l'esempio DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) usa attivazioni fuse per migliorare le prestazioni.

## <a name="operators-that-support-fused-activation"></a>Operatori che supportano l'attivazione fusa

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** e **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Attivazioni supportate per fusion

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

Gli operatori non presenti in questo elenco non sono supportati per l'attivazione fusa.

## <a name="see-also"></a>Vedi anche

* [Esempio directMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
