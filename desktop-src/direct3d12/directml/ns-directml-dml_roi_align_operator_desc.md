---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Esegue un'operazione di allineamento del ROI, come descritto nel [documento Mask R-CNN](https://arxiv.org/abs/1703.06870). In breve, l'operazione estrae le colture dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando il *InterpolationMode* specificato.
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
ms.openlocfilehash: 987aef7d7002892b8af3167fb8da2b74dc80a12e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320330"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>Struttura DML_ROI_ALIGN_OPERATOR_DESC (directml. h)

Esegue un'operazione di allineamento del ROI, come descritto nel [documento Mask R-CNN](https://arxiv.org/abs/1703.06870). In breve, l'operazione estrae le colture dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando il *InterpolationMode* specificato.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Un tensore contenente i dati di input con dimensioni `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente le aree di interesse (ROI) dati. Le dimensioni consentite di `ROITensor` sono `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` o `{ 1, 1, NumROIs, 4 }` . Per ogni ROI, i valori saranno le coordinate degli angoli superiore sinistro e inferiore destro nell'ordine `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente gli indici di batch per estrarre il ROIs da. Le dimensioni consentite di `BatchIndicesTensor` sono `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` o `{ 1, 1, 1, NumROIs }` . Ogni valore è l'indice di un batch da *InputTensor*. Il comportamento non è definito se i valori non sono compresi nell'intervallo [0, BatchCount).

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati di output. Le dimensioni previste di *OutputTensor* sono `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Funzione di riduzione da usare quando si riducono tutti gli esempi di input che contribuiscono a un elemento di output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) o **DML_REDUCE_FUNCTION_MAX**). Il numero di campioni di input da ridurre in è limitato da *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

`InterpolationMode`

Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Modalità di interpolazione da utilizzare quando si ridimensionano le aree.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Usa l'algoritmo *adiacente più vicino* , che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.
- **DML_INTERPOLATION_MODE_LINEAR**. Usa l'algoritmo *bilineare* , che calcola l'elemento output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per ogni dimensione. Poiché vengono ridimensionate solo 2 dimensioni, la media ponderata viene calcolata su un totale di 4 elementi di input per ogni elemento di output.

`SpatialScaleX`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Componente X (o larghezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per renderle proporzionali a *InputHeight* e *InputWidth*. Se, ad esempio, *ROITensor* contiene Coordinate normalizzate (valori compresi nell'intervallo [0.. 1]), *SpatialScaleX* di solito avrà lo stesso valore di *InputWidth*.

`SpatialScaleY`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Componente Y (o altezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per renderle proporzionali a *InputHeight* e *InputWidth*. Se, ad esempio, *ROITensor* contiene Coordinate normalizzate (valori compresi nell'intervallo [0.. 1]), *SpatialScaleY* genererà lo stesso valore di *InputHeight*.

`OutOfBoundsInputValue`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Valore da leggere da *InputTensor* quando l'oggetto Rois è esterno ai limiti di *InputTensor*. Questo problema può verificarsi quando i valori ottenuti dopo la scalabilità di *ROITensor* da *SpatialScaleX* e *SpatialScaleY* sono maggiori di *InputWidth* e *InputHeight*.

`MinimumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Numero minimo di campioni di input da utilizzare per ogni elemento di output. L'operatore calcolerà il numero di campioni di input eseguendo `ScaledCropSize / OutputSize` , quindi lo clamperà su *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Numero massimo di campioni di input da utilizzare per ogni elemento di output. L'operatore calcolerà il numero di campioni di input eseguendo `ScaledCropSize / OutputSize` , quindi lo clamperà su *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor*, *OutputTensor* e *ROITensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ROITensor | Input | da 2 a 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Input | da 1 a 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |