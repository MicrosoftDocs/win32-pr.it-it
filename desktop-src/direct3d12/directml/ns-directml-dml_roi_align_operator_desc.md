---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Esegue un'operazione di allineamento ROI, come descritto nel [documento Mascherare R-CNN.](https://arxiv.org/abs/1703.06870) In breve, l'operazione estrae le piante dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando l'oggetto *InterpolationMode specificato.*
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417513"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC struttura (directml.h)

Esegue un'operazione di allineamento ROI, come descritto nel [documento Mascherare R-CNN.](https://arxiv.org/abs/1703.06870) In breve, l'operazione estrae le piante dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando l'oggetto *InterpolationMode specificato.*

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input con dimensioni `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati delle aree di interesse. Le dimensioni `ROITensor` consentite di `{ NumROIs, 4 }` sono `{ 1, NumROIs, 4 }` , o `{ 1, 1, NumROIs, 4 }` . Per ogni ROI, i valori saranno le coordinate degli angoli superiore sinistro e inferiore destro nell'ordine `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente gli indici batch da cui estrarre i ROI. Le dimensioni `BatchIndicesTensor` consentite di `{ NumROIs }` sono , , o `{ 1, NumROIs }` `{ 1, 1, NumROIs }` `{ 1, 1, 1, NumROIs }` . Ogni valore è l'indice di un batch da *InputTensor*. Il comportamento non è definito se i valori non sono nell'intervallo [0, BatchCount).

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di output. Le dimensioni previste di *OutputTensor* sono `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Funzione di riduzione da usare per la riduzione di tutti i campioni di input che contribuiscono a un elemento di output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) o **DML_REDUCE_FUNCTION_MAX**). Il numero di campioni di input da ridurre è limitato da *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput.*

`InterpolationMode`

Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Modalità di interpolazione da usare per il ridimensionamento delle aree.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Usa *l'algoritmo Nearest Neighbor,* che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.
- **DML_INTERPOLATION_MODE_LINEAR**. Usa *l'algoritmo Bilineare,* che calcola l'elemento di output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per dimensione. Poiché vengono ridimensionate solo 2 dimensioni, la media ponderata viene calcolata su un totale di 4 elementi di input per ogni elemento di output.

`SpatialScaleX`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Componente X (o larghezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per per renderle proporzionali a *InputHeight* *e InputWidth.* Ad esempio, se *ROITensor* contiene coordinate normalizzate (valori nell'intervallo [0..1]), *SpatialScaleX* avrebbe in genere lo stesso valore di *InputWidth*.

`SpatialScaleY`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Componente Y (o altezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per per renderle proporzionali a *InputHeight* *e InputWidth.* Ad esempio, se *ROITensor* contiene coordinate normalizzate (valori nell'intervallo [0..1]), *SpatialScaleY* avrebbe in genere lo stesso valore di *InputHeight*.

`OutOfBoundsInputValue`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Valore da leggere da *InputTensor* quando i ROI sono esterni ai limiti di *InputTensor.* Ciò può verificarsi quando i valori ottenuti dopo il *ridimensionamento roITensor* di *SpatialScaleX* e *SpatialScaleY* sono maggiori di *InputWidth* e *InputHeight.*

`MinimumSamplesPerOutput`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Numero minimo di campioni di input da usare per ogni elemento di output. L'operatore calcolerà il numero di campioni di input eseguendo , quindi lo stringerà a `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* *e MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Numero massimo di campioni di input da usare per ogni elemento di output. L'operatore calcolerà il numero di campioni di input eseguendo , quindi lo stringerà a `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* *e MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor,* *OutputTensor* e *ROITensor* devono avere lo stesso *tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ROITensor | Input | Da 2 a 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Input | Da 1 a 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |