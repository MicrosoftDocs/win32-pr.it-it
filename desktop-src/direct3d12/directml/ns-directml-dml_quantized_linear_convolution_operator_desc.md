---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, alla evoluzione e alla quantificazione dell'output.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803881"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC struttura (directml.h)
Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, alla evoluzione e alla quantificazione dell'output. 

Le funzioni lineari quantizzanti usate da questo operatore sono le funzioni di quantizzazione lineare

### <a name="dequantize-function"></a>Funzione Dequantize

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Funzione Quantize

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input. Le dimensioni previste di *InputTensor* sono `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati della scala di input. Le dimensioni previste di `InputScaleTensor` sono `{ 1, 1, 1, 1 }` . Questo valore di scala viene usato per dequantizzare i valori di input.


`InputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del punto zero di input. Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` . Questo valore del punto zero viene usato per dequantizzare i valori di input.


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati del filtro. Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati della scala del filtro. Le dimensioni previste di sono `FilterScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, OutputChannelCount, 1, 1 }` se è necessaria la quantizzazione per canale. Questo valore di scala viene usato per dequantizzare i valori di filtro.


`FilterZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del punto zero del filtro. Le dimensioni previste di *FilterZeroPointTensor* sono se è necessaria la quantizzazione per tensore o se `{ 1, 1, 1, 1 }` è necessaria la `{ 1, OutputChannelCount, 1, 1 }` quantizzazione per canale. Questo valore del punto zero viene usato per dequantizzare i valori di filtro.


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di distorsione. Il tensore di distorsione è un tensore contenente dati che vengono trasmessi attraverso il tensore di output alla fine della convoluzione che viene aggiunto al risultato. Le dimensioni previste di BiasTensor sono `{ 1, OutputChannelCount, 1, 1 }` per 4D.


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati della scala di output. Le dimensioni previste di OutputScaleTensor sono `{ 1, 1, 1, 1 }` . Questo valore di scala di input viene usato per quantificare i valori di output della convoluzione.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del filtro zero punti. Le dimensioni previste di OutputZeroPointTensor sono `{ 1, 1, 1, 1 }` . Questo valore del punto zero di input viene usato per quantificare la convoluzione dei valori di output.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni previste di OutputTensor sono `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di dimensioni spaziali per l'operazione di convoluzione. Le dimensioni spaziali sono le dimensioni inferiori del tensore filtro convoluzione *FilterTensor*. Questo valore determina anche le dimensioni delle matrici *Strides,* *Dilations,* *StartPadding* ed *EndPadding.* È supportato solo il valore 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Passi dell'operazione di convoluzione. Questi passi vengono applicati al filtro di convoluzione. Sono separati dai passi del tensore inclusi in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Dilations dell'operazione di convoluzione. Le dilazioni sono stride applicati agli elementi del kernel di filtro. Ciò ha l'effetto di simulare un kernel di filtro più grande tramite il riempimento degli elementi interni del kernel del filtro con zeri.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Valori di riempimento da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Valori di riempimento da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.


`GroupCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di gruppi in cui dividere l'operazione di convoluzione. *GroupCount* può essere usato per ottenere una convoluzione per profondità impostando *GroupCount* su uguale al numero di canali di input. In questo modo la convoluzione viene suddivisa in una convoluzione separata per canale di input. 

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo di dati*.
* *InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo di dati*.
* *OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *datatype*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | INT8, UINT8 |
| InputScaleTensor | Input | 4 | FLOAT32 |
| InputZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| FilterTensor | Input | 4 | INT8, UINT8 |
| FilterScaleTensor | Input | 4 | FLOAT32 |
| FilterZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| BiasTensor | Input facoltativo | 4 | INT32 |
| OutputScaleTensor | Input | 4 | FLOAT32 |
| OutputZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |