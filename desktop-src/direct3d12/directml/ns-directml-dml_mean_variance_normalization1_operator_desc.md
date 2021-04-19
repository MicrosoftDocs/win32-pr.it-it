---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Esegue una funzione di normalizzazione della varianza media sul tensore di input. Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320368"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Struttura DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)
Esegue una funzione di normalizzazione della varianza media sul tensore di input. Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione. Questo operatore esegue il calcolo seguente.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati di input. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .


`ScaleTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo che contiene i dati della scala. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` . Qualsiasi dimensione può essere sostituita da 1 per la trasmissione in tale dimensione. Questo tensore è obbligatorio se viene usato *BiasTensor* .


`BiasTensor`

Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati di distorsione. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` . Qualsiasi dimensione può essere sostituita da 1 per la trasmissione in tale dimensione. Questo tensore è obbligatorio se viene usato *ScaleTensor* .


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, Height, Width }` .


`AxisCount`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Numero di assi. Questo campo determina la dimensione della matrice di *assi* .


`Axes`

Tipo: \_ \_ Dimensione campo \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \*** 

Assi lungo i quali calcolare la media e la varianza.


`NormalizeVariance`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b>

**True** se il livello di normalizzazione include la varianza nel calcolo di normalizzazione. In caso contrario, **false**. Se **false**, l'equazione di normalizzazione è `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .


`Epsilon`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Valore Epsilon da usare per evitare la divisione per zero. Per impostazione predefinita, è consigliato un valore di 0,00001.


`FusedActivation`

Tipo: \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Livello di attivazione con fusibile facoltativo da applicare dopo la normalizzazione.


## <a name="remarks"></a>Commenti
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** è un superset della funzionalità di [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). In questo caso, l'impostazione della matrice degli **assi** su `{ 0, 2, 3 }` è equivalente all'impostazione di *CrossChannel* su **false** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; durante l'impostazione della matrice degli **assi** su `{ 1, 2, 3 }` è equivalente all'impostazione di *Crosschannel* su **true**.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor* e *OutputTensor* devono avere le stesse *dimensioni*.
* *BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | {BatchCount, ChannelCount, Height, Width} | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Input facoltativo | {ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth} | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Input facoltativo | { BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | {BatchCount, ChannelCount, Height, Width} | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |

## <a name="see-also"></a>Vedi anche

[Utilizzo di operatori con fusibile per migliorare le prestazioni](../dml-fused-activations.md)