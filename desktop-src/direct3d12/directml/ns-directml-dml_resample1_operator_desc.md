---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Ricampiona gli elementi dall'origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione. È possibile usare una modalità di interpolazione lineare o più vicina.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417801"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC struttura (directml.h)
Ricampiona gli elementi dall'origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione. È possibile usare una modalità di interpolazione lineare o più vicina. L'operatore supporta l'interpolazione tra più dimensioni, non solo 2D. È quindi possibile mantenere le stesse dimensioni spaziali, ma eseguire l'interpolazione tra canali o tra batch. La relazione tra le coordinate di input e di output è la seguente.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i dati di output.


`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Questo campo determina il tipo di interpolazione usata per scegliere i pixel di output.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Usa *l'algoritmo Nearest Neighbor,* che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.

- **DML_INTERPOLATION_MODE_LINEAR**. Usa *l'algoritmo Quadrilineare,* che calcola l'elemento di output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per ogni dimensione. Poiché è possibile ricampionare tutte e 4 le dimensioni, la media ponderata viene calcolata su un totale di 16 elementi di input per ogni elemento di output.


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di valori nelle matrici a cui puntano *Scales,* *InputPixelOffsets* e *OutputPixelOffsets.* Questo valore deve corrispondere al numero di dimensioni *di InputTensor* e *OutputTensor*, che deve essere 4.


`Scales`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Le scale da applicare quando si ricampiona l'input, in cui le scale > 1 ridimensionano l'immagine e < 1 ridimensionano l'immagine per tale dimensione. Si noti che le scale non devono essere esattamente `OutputSize / InputSize` . Se l'input dopo il ridimensionamento è maggiore del limite di output, viene ritagliato in base alle dimensioni di output. D'altra parte, se l'input dopo il ridimensionamento è più piccolo del limite di output, i bordi di output sono vincolati.


`InputPixelOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Offset da applicare ai pixel di input prima del ricampionamento. Quando questo valore è , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non dà `0` il risultato previsto. Per ricampionare l'immagine usando il centro dei pixel e ottenere lo stesso comportamento DML_RESAMPLE_OPERATOR_DESC [,](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)questo valore deve essere `0.5` .


`OutputPixelOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Offset da applicare ai pixel di output dopo il ricampionamento. Quando questo valore è , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non dà `0` il risultato previsto. Per ricampionare l'immagine usando il centro dei pixel e ottenere lo stesso comportamento DML_RESAMPLE_OPERATOR_DESC [,](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)questo valore deve essere `-0.5` .


## <a name="remarks"></a>Commenti
Quando *InputPixelOffsets* è impostato su 0,5 e *OutputPixelOffsets* è impostato su -0,5, questo operatore equivale a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere lo stesso *Tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |