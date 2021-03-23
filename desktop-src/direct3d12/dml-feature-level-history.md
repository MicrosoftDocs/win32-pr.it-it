---
title: Cronologia a livello di funzionalità DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548914"
---
# <a name="directml-feature-level-history"></a>Cronologia a livello di funzionalità DirectML

Per informazioni generali sulla cronologia delle versioni di DirectML, vedere [cronologia delle versioni di DirectML](./dml-version-history.md).

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Introdotta in DirectML versione 1.4.0.

Aggiunta del supporto per gli operatori seguenti.

* [DML_OPERATOR_ELEMENT_WISE_BIT_AND](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Sono stati aggiunti i miglioramenti seguenti.

* Il numero massimo di dimensioni del tensore è stato aumentato da 5 a 8. Vedere [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* Per gli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di tipo Integer.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE** quando si utilizza **DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**
* Sono stati aggiunti i seguenti tipi di dati a 64 bit e sono supportati dagli operatori Select.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Funzionalità deprecata.

* **DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** sono stati deprecati. È preferibile usare la **DML_OPERATOR_ARGMIN** autonoma e gli operatori di **DML_OPERATOR_ARGMAX** nella propria posizione.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Introdotta in DirectML versione 1.2.0.

Sono state aggiunte le API seguenti.

* [Interfaccia IDMLDevice1](./directml/nn-directml-idmldevice1.md)
* Supporto dell'operatore Graph (vedere [IDMLDevice1:: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)

Aggiunta del supporto per gli operatori seguenti.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Sono stati aggiunti i miglioramenti seguenti.

* Per gli operatori seguenti è stato aggiunto il supporto aggiuntivo per i tipi di tipo Integer.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE** quando si utilizza una delle seguenti funzioni di riduzione.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Restrizioni di forma tensore rilassate per **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Introdotta in DirectML versione 1.1.0.

Sono state aggiunte le API seguenti.
* [Funzione DMLCreateDevice1](./directml/nf-directml-dmlcreatedevice1.md)
* [Enumerazione DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Query a livello di funzionalità (vedere [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Aggiunta del supporto per gli operatori seguenti.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Sono stati aggiunti i miglioramenti seguenti.

* Quando si associa una risorsa di input per l'invio di un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), è ora possibile fornire una risorsa con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (oltre al **D3D12_HEAP_TYPE_DEFAULT**), a condizione che vengano impostate anche le proprietà dell'heap appropriate. Vedere [Binding in DirectML](./dml-binding.md).
* Gli operatori booleani logici seguenti supportano ora i tensori di output **Uint8** , oltre al supporto esistente per **UInt32**.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* le funzioni di attivazione 5D supportano ora l'uso di stride nei propri tensori di input e di output.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Livello di funzionalità in cui è stato introdotto DirectML.

## <a name="see-also"></a>Vedi anche

Cronologia delle versioni di [DirectML](./dml-version-history.md) 
 [Enumerazione DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [DMLCreateDevice1 (funzione](./directml/nf-directml-dmlcreatedevice1.md) 
 ) [Struttura DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)