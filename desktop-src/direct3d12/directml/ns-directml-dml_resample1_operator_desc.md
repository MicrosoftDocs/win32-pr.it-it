---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Ricampiona gli elementi dall'origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione. È possibile usare una modalità di interpolazione lineare o vicina.
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
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320360"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>Struttura DML_RESAMPLE1_OPERATOR_DESC (directml. h)
Ricampiona gli elementi dall'origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione. È possibile usare una modalità di interpolazione lineare o vicina. L'operatore supporta l'interpolazione tra più dimensioni, non solo 2D. Quindi, è possibile garantire la stessa dimensione spaziale, ma interpolare tra canali o tra batch. Di seguito è riportata la relazione tra le coordinate di input e di output.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Il tensore contenente i dati di input.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i dati di output.


`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Questo campo determina il tipo di interpolazione usato per scegliere i pixel di output.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Usa l'algoritmo *adiacente più vicino* , che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.

- **DML_INTERPOLATION_MODE_LINEAR**. Usa l'algoritmo *Quadrilinear* , che calcola l'elemento output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per ogni dimensione. Poiché tutte le 4 dimensioni possono essere ricampionate, la media ponderata viene calcolata su un totale di 16 elementi di input per ogni elemento di output.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di valori nelle matrici con *scalabilità*, *InputPixelOffsets* e *OutputPixelOffsets* che puntano a. Questo valore deve corrispondere al numero di dimensioni di *InputTensor* e *OutputTensor*, che deve essere 4.


`Scales`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Scale da applicare quando si ricampionano i dati di input, in cui scale > 1 aumentano l'immagine e si ridimensiona < 1 si ridimensiona l'immagine per tale dimensione. Si noti che non è necessario che le scale siano esatte `OutputSize / InputSize` . Se l'input dopo la scalabilità è maggiore del limite di output, viene ritagliato fino alla dimensione di output. D'altra parte, se l'input dopo la scalabilità è inferiore al limite di output, i bordi di output vengono bloccati.


`InputPixelOffsets`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Offset da applicare ai pixel di input prima del ricampionamento. Quando questo valore è `0` , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non fornisce il risultato previsto. Per ricampionare l'immagine usando il centro dei pixel e per ottenere lo stesso comportamento di [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), questo valore deve essere `0.5` .


`OutputPixelOffsets`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Offset da applicare ai pixel di output dopo il ricampionamento. Quando questo valore è `0` , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non fornisce il risultato previsto. Per ricampionare l'immagine usando il centro dei pixel e per ottenere lo stesso comportamento di [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), questo valore deve essere `-0.5` .


## <a name="remarks"></a>Commenti
Quando *InputPixelOffsets* sono impostati su 0,5 e *OutputPixelOffsets* sono impostati su-0,5, questo operatore equivale a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |