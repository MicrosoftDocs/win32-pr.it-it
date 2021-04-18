---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcola il valore massimo tra gli elementi all'interno della finestra temporale scorrevole sul tensore di input e, facoltativamente, restituisce gli indici dei valori massimi selezionati.
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
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320404"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>Struttura DML_MAX_POOLING2_OPERATOR_DESC (directml. h)
Calcola il valore massimo tra gli elementi all'interno della finestra temporale scorrevole sul tensore di input e, facoltativamente, restituisce gli indici dei valori massimi selezionati.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Un tensore di input di *dimensioni* `{ BatchCount, ChannelCount, Height, Width }` se *InputTensor. DimensionCount* è 4 e `{ BatchCount, ChannelCount, Depth, Height, Weight } ` se *InputTensor. DimensionCount* è 5.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output in cui scrivere i risultati. Le dimensioni del tensore di output possono essere calcolate come indicato di seguito.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output facoltativo di indici al tensore di input *InputTensor* dei valori massimi prodotti e archiviati in *OutputTensor*. Questi valori di indice sono in base zero e considerano il tensore di input come matrice unidimensionale contigua. Quando più elementi all'interno della finestra temporale scorrevole hanno lo stesso valore, i valori uguali successivi vengono ignorati e l'indice punta al primo valore rilevato. Sia *OutputTensor* che *OutputIndicesTensor* hanno le stesse dimensioni del tensore.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni spaziali del tensore di input *InputTensor*, che corrisponde anche al numero di dimensioni della finestra temporale scorrevole *WindowSize*. Questo valore determina anche le dimensioni delle matrici *Strides*, *StartPadding* e *EndPadding* . Deve essere impostato su 2 quando *InputTensor* è 4D e 3 quando si tratta di un tensore 5D.


`Strides`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Stride per le dimensioni della finestra temporale scorrevole delle dimensioni `{ Height, Width }` quando *DimensionCount* è impostato su 2 o quando è `{ Depth, Height, Width }` impostato su 3.


`WindowSize`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Dimensioni della finestra temporale scorrevole in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o quando è `{ Depth, Height, Width }` impostato su 3.


`StartPadding`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Numero di elementi di riempimento da applicare all'inizio di ogni dimensione spaziale del tensore di input *InputTensor*. I valori si trovano in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


`EndPadding`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Numero di elementi di riempimento da applicare alla fine di ogni dimensione spaziale del tensore di input *InputTensor*. I valori si trovano in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


`Dilations`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Valori per ogni dimensione spaziale del tensore di input *InputTensor* in base al quale viene selezionato un elemento nella finestra temporale scorrevole per ogni elemento di tale valore. I valori si trovano in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.


## <a name="remarks"></a>Commenti
**DML_MAX_POOLING2_OPERATOR_DESC** sostituisce la versione precedente [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) con ulteriori *dilatazioni* di matrici costanti. Le due versioni sono equivalenti quando le *dilatazioni* sono impostate su `{ 1,1 }` per l'input 4D o `{ 1,1,1 }` per le funzionalità di input 5D.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor*, *OutputIndicesTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.
* *InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Output | da 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Output facoltativo | da 4 a 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 4 a 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | da 4 a 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Output facoltativo | da 4 a 5 | UINT32 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, versione 2004 (10,0; Compilazione 19041) |
| **Server minimo supportato** | Windows Server, versione 2004 (10,0; Compilazione 19041) |
| **Intestazione** | directml. h |