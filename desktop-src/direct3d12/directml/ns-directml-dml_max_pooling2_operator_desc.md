---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcola il valore massimo tra gli elementi all'interno della finestra scorrevole sul tensore di input e restituisce facoltativamente gli indici dei valori massimi selezionati.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417594"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC struttura (directml.h)
Calcola il valore massimo tra gli elementi all'interno della finestra scorrevole sul tensore di input e restituisce facoltativamente gli indici dei valori massimi selezionati.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di input *di Dimensioni* `{ BatchCount, ChannelCount, Height, Width }` se *InputTensor.DimensionCount* è 4 e `{ BatchCount, ChannelCount, Depth, Height, Weight } ` se *InputTensor.DimensionCount* è 5.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i risultati. Le dimensioni del tensore di output possono essere calcolate come indicato di seguito.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output facoltativo di indici al tensore *input InputTensor* dei valori massimi prodotti e archiviati in *OutputTensor*. Questi valori di indice sono in base zero e trattano il tensore di input come una matrice unidimensionale contigua. Quando più elementi all'interno della finestra scorrevole hanno lo stesso valore, i valori uguali successivi vengono ignorati e l'indice punta al primo valore rilevato. Sia *OutputTensor* che *OutputIndicesTensor* hanno le stesse dimensioni del tensore.


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di dimensioni spaziali del tensore di input *InputTensor*, che corrisponde anche al numero di dimensioni della finestra scorrevole *WindowSize.* Questo valore determina anche le dimensioni delle matrici *Strides,* *StartPadding* ed *EndPadding.* Deve essere impostato su 2 quando *InputTensor* è 4D e 3 quando è un tensore 5D.


`Strides`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Passi per le dimensioni della finestra scorrevole delle dimensioni `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` su 3.


`WindowSize`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Dimensioni della finestra scorrevole in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` su 3.


`StartPadding`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Numero di elementi di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del tensore *input InputTensor*. I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


`EndPadding`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Numero di elementi di spaziatura interna da applicare alla fine di ogni dimensione spaziale del tensore *input InputTensor*. I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


`Dilations`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Valori per ogni dimensione spaziale del tensore di input *InputTensor* in base al quale un elemento all'interno della finestra scorrevole viene selezionato per ogni elemento di tale valore. I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


## <a name="remarks"></a>Commenti
**DML_MAX_POOLING2_OPERATOR_DESC** sostituisce la versione precedente DML_MAX_POOLING_OPERATOR1_DESC [con](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) una matrice costante aggiuntiva *Dilations*. Le due versioni sono equivalenti quando *Dilations* è impostato su per `{ 1,1 }` l'input 4D o per le funzionalità di input `{ 1,1,1 }` 5D.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor,* *OutputIndicesTensor* e *OutputTensor* devono avere lo stesso *dimensioncount.*
* *InputTensor* e *OutputTensor* devono avere lo stesso *Tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e successive
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Output | Da 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Output facoltativo | Da 4 a 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e successive
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 4 a 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | Da 4 a 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Output facoltativo | Da 4 a 5 | UINT32 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10 versione 2004 (10.0; Build 19041) |
| **Server minimo supportato** | Windows Server versione 2004 (10.0; Build 19041) |
| **Intestazione** | directml.h |