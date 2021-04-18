---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti su dati Integer.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320381"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>Struttura DML_CONVOLUTION_INTEGER_OPERATOR_DESC (directml. h)

Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti su dati Integer. I tensori di punti zero facoltativi possono essere usati anche per sottrarre i valori del punto zero dal tensore di input e filtro.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
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

Un tensore contenente i dati di input. Le dimensioni previste di *InputTensor* sono `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero di input. Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati del filtro. Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero del filtro. Le dimensioni previste di *FilterZeroPointTensor* sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, OutputChannelCount, 1, 1 }` se è richiesta la quantizzazione per canale.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni previste di *OutputTensor* sono `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di dimensioni spaziali per l'operazione di convoluzione. Le dimensioni spaziali sono le dimensioni inferiori del *FilterTensor* di convoluzione. Questo valore determina anche le dimensioni delle matrici *Strides*, *dilatations*, *StartPadding* e *EndPadding* . È supportato solo il valore 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Matrice contenente gli stride dell'operazione di convoluzione. Questi stride vengono applicati al filtro di convoluzione. Sono separate dagli stride di tensori inclusi nel [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Matrice contenente le dilatazioni dell'operazione di convoluzione. Le dilatazioni sono gli stride applicati agli elementi del kernel del filtro. Questo ha l'effetto di simulare un kernel di filtro di dimensioni maggiori riempiendo gli elementi del kernel di filtro interni con zeri.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Matrice contenente i valori di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Matrice contenente i valori di spaziatura interna da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.


`GroupCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di gruppi in cui dividere l'operazione di convoluzione. *GroupCount* può essere usato per ottenere una convoluzione a livello di profondità impostando *GroupCount* uguale al numero di canali di input. Questa operazione divide la convoluzione in una convoluzione separata per ogni canale di input.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo* di dati.
* *InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | {BatchCount, InputChannelCount, InputHeight, InputWidth} | 4 | INT8, UINT8 |
| InputZeroPointTensor | Input facoltativo | {1, 1, 1, 1} | 4 | INT8, UINT8 |
| FilterTensor | Input | { FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth } | 4 | INT8, UINT8 |
| FilterZeroPointTensor | Input facoltativo | {1, FilterZeroPointChannelCount, 1, 1} | 4 | INT8, UINT8 |
| OutputTensor | Output | {BatchCount, OutputChannelCount, OutputHeight, OutputWidth} | 4 | INT32 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |