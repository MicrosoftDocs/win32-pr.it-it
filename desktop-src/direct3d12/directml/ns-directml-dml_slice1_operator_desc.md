---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Estrae una singola area secondaria ("slice") di un tensore di input.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320293"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>Struttura DML_SLICE1_OPERATOR_DESC (directml. h)
Estrae una singola area secondaria ("slice") di un tensore di input.

Nella *finestra input* vengono descritti i limiti del tensore di input da considerare nella sezione. La finestra viene definita utilizzando tre valori per ogni dimensione.

- L' *offset* contrassegna l' *inizio della finestra* in una dimensione.
- Le *dimensioni* contrassegnano l'extent della finestra in una dimensione. La *fine della finestra* in una dimensione è `offset + size - 1` .
- Lo *stride* indica come attraversare gli elementi di una dimensione.
  - La grandezza dello stride indica il numero di elementi da avanzare quando si esegue la copia all'interno della finestra.
  - Se uno stride è positivo, gli elementi vengono copiati a partire dall' *inizio* della finestra nella dimensione.
  - Se uno stride è negativo, gli elementi vengono copiati a partire dalla *fine* della finestra nella dimensione.

Nello pseudo-codice seguente viene illustrato il modo in cui gli elementi vengono copiati utilizzando la finestra input. Si noti come gli elementi di una dimensione vengono copiati dall'inizio alla fine con uno stride positivo e copiati da end per iniziare con un stride negativo.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

La finestra di input non deve essere vuota in nessuna dimensione e la finestra non deve estendersi oltre le dimensioni del tensore di input (le letture out-of-Bounds non sono consentite). Le dimensioni e gli stride della finestra limitano efficacemente il numero di elementi che possono essere copiati da ogni dimensione `i` del tensore di input.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Il tensore di output non è necessario per copiare tutti gli elementi raggiungibili nella finestra. La sezione è valida fino a quando `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore da cui estrarre le sezioni.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati dei dati sezionati.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di dimensioni. Questo campo determina la dimensione delle matrici *InputWindowOffsets*, *InputWindowSizes* e *InputWindowStrides* . Questo valore deve corrispondere a *DimensionCount* dei tensori di input e di output. Questo valore deve essere compreso tra 1 e 8, incluso, a partire da `DML_FEATURE_LEVEL_3_0` . i livelli di funzionalità precedenti richiedono un valore 4 o 5.


`InputWindowOffsets`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente l'inizio (in elementi) della finestra di input in ogni dimensione. I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente l'extent (in elementi) della finestra di input in ogni dimensione. I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente lo stride della sezione lungo ogni dimensione del tensore di input, in elementi. La grandezza dello stride indica il numero di elementi da avanzare quando si esegue la copia all'interno della finestra di input. Il segno dello stride determina se gli elementi vengono copiati a partire dall'inizio della finestra (stride positivo) o dalla fine della finestra (stride negativo). Gli stride non possono essere 0.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene usato questo stesso tensore di input.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Esempio 1. Sezione con stride con stride positivi

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Gli elementi copiati vengono calcolati come indicato di seguito. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Esempio 2. Sezione con stride con stride negativi

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Tenere presente che le dimensioni con stride della finestra negativa iniziano a eseguire la copia alla fine della finestra di input per la dimensione; Questa operazione viene eseguita aggiungendo `InputWindowSize[i] - 1` all'offset della finestra. Le dimensioni con uno stride positivo iniziano semplicemente da `InputWindowOffset[i]` .
- L'asse 0 ( `+1` stride finestra) inizia la copia in `InputWindowOffsets[0] = 0` . 
- AXIS 1 ( `+1` stride finestra) inizia la copia in `InputWindowOffsets[1] = 0` . 
- Axis 2 ( `-2` stride finestra) inizia la copia in `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- Axis 3 ( `+2` stride finestra) inizia la copia in `InputWindowOffsets[3] = 1` . 

Gli elementi copiati vengono calcolati come indicato di seguito. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Commenti
Questo operatore è simile a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), ma è diverso in due modi importanti.

- Gli stride della sezione possono essere negativi, che consentono di invertire i valori lungo le dimensioni.
- Le dimensioni della finestra di input non sono necessariamente le stesse delle dimensioni del tensore di output.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati e *DimensionCount*.

## <a name="tensor-support"></a>Supporto tensore
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |