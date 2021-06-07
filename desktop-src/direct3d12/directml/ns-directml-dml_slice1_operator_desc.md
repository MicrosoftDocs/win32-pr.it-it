---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Estrae una singola sottoarea (una "sezione") di un tensore di input.
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
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417456"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC struttura (directml.h)
Estrae una singola sottoarea (una "sezione") di un tensore di input.

La *finestra di input* descrive i limiti del tensore di input da considerare nella sezione. La finestra viene definita usando tre valori per ogni dimensione.

- *L'offset* *contrassegna l'inizio della finestra* in una dimensione.
- Le *dimensioni* contrassegnano l'estensione della finestra in una dimensione. La *fine della finestra in* una dimensione è `offset + size - 1` .
- Lo *stride* indica come attraversare gli elementi in una dimensione.
  - La grandezza dello stride indica il numero di elementi da avanzare durante la copia all'interno della finestra.
  - Se uno stride è positivo, gli  elementi vengono copiati a partire dall'inizio della finestra nella dimensione.
  - Se uno stride è negativo, gli elementi vengono copiati a partire dalla *fine* della finestra nella dimensione.

Lo pseudocodice seguente illustra come vengono copiati gli elementi usando la finestra di input. Si noti come gli elementi di una dimensione vengono copiati dall'inizio alla fine con uno stride positivo e copiati dall'inizio all'inizio con uno stride negativo.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

La finestra di input non deve essere vuota in nessuna dimensione e la finestra non deve estendersi oltre le dimensioni del tensore di input (non sono consentite le operazioni di lettura fuori limite). Le dimensioni e gli stride della finestra limitano in modo efficace il numero di elementi che possono essere copiati da ogni dimensione `i` del tensore di input.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Il tensore di output non è necessario per copiare tutti gli elementi raggiungibili all'interno della finestra. La sezione è valida purché `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

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

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di dimensioni. Questo campo determina le dimensioni delle matrici *InputWindowOffsets,* *InputWindowSizes* e *InputWindowStrides.* Questo valore deve corrispondere a *DimensionCount* dei tensori di input e output. Questo valore deve essere compreso tra 1 e 8, in modo inclusivo, a partire da . I livelli di funzionalità precedenti richiedono un valore `DML_FEATURE_LEVEL_3_0` pari a 4 o 5.


`InputWindowOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente l'inizio (in elementi) della finestra di input in ogni dimensione. I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente l'extent (in elementi) della finestra di input in ogni dimensione. I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matrice contenente lo stride della sezione lungo ogni dimensione del tensore di input, in elementi. La grandezza dello stride indica il numero di elementi da avanzare durante la copia all'interno della finestra di input. Il segno dello stride determina se gli elementi vengono copiati a partire dall'inizio della finestra (stride positivo) o dalla fine della finestra (stride negativo). Gli stride non possono essere 0.

## <a name="examples"></a>Esempio

Gli esempi seguenti usano lo stesso tensore di input.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Esempio 1. Sezione strided con passi positivi

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Gli elementi copiati vengono calcolati nel modo seguente. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Esempio 2. Sezione strided con passi negativi

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Tenere conto che le dimensioni con gli stride della finestra negativi iniziano a copiare alla fine della finestra di input per tale dimensione; Questa operazione viene eseguita aggiungendo `InputWindowSize[i] - 1` all'offset della finestra. Le dimensioni con uno stride positivo iniziano semplicemente da `InputWindowOffset[i]` .
- L'asse 0 `+1` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[0] = 0` . 
- L'asse 1 `+1` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[1] = 0` . 
- L'asse 2 `-2` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- L'asse 3 `+2` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[3] = 1` . 

Gli elementi copiati vengono calcolati nel modo seguente. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Commenti
Questo operatore è simile [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), ma differisce in due modi importanti.

- Gli stride delle sezioni possono essere negativi, che consentono di invertire i valori lungo le dimensioni.
- Le dimensioni della finestra di input non corrispondono necessariamente alle dimensioni dei tensore di output.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere gli stessi *DataType* *e DimensionCount*.

## <a name="tensor-support"></a>Supporto di Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e successive
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e successive
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | Da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |