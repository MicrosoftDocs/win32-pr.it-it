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
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549777"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC struttura (directml.h)

Esegue una funzione di normalizzazione della varianza media sul tensore di input. Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione. Questo operatore esegue il calcolo seguente.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

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

Tensore contenente i dati di input. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .

`ScaleTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati di scalabilità.

Se **DML_FEATURE_LEVEL** è minore **di DML_FEATURE_LEVEL_4_0**, le dimensioni di questo tensore devono essere `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` . Le dimensioni ScaleBatchCount, ScaleHeight e ScaleWidth devono corrispondere a *InputTensor* o essere impostate su 1 per trasmettere automaticamente tali dimensioni nell'input.

Se **DML_FEATURE_LEVEL** è maggiore o uguale **a DML_FEATURE_LEVEL_4_0**, qualsiasi dimensione può essere impostata su 1 e trasmessa automaticamente in modo che corrisponda a *InputTensor*.

Questo tensore è necessario se *si usa BiasTensor.*

`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Tensore facoltativo contenente i dati di Bias.

Se **DML_FEATURE_LEVEL** è minore di **DML_FEATURE_LEVEL_4_0**, le dimensioni di questo tensore devono essere `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` . Le dimensioni BiasBatchCount, BiasHeight e BiasWidth devono corrispondere a *InputTensor* o essere impostate su 1 per trasmettere automaticamente tali dimensioni nell'input.

Se **DML_FEATURE_LEVEL** è maggiore o uguale **a DML_FEATURE_LEVEL_4_0**, qualsiasi dimensione può essere impostata su 1 ed essere trasmessa automaticamente in modo che corrisponda a *InputTensor*.

Questo tensore è obbligatorio se *si usa ScaleTensor.*

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Numero di assi. Questo campo determina le dimensioni della *matrice Axes.*

`Axes`

Tipo: \_ Dimensione \_ campo \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \*** 

Assi lungo i quali calcolare la media e la varianza.

`NormalizeVariance`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

**TRUE** se il livello di normalizzazione include Varianza nel calcolo della normalizzazione. In caso contrario, **FALSE.** Se **FALSE,** l'equazione di normalizzazione è `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .

`Epsilon`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Valore epsilon da utilizzare per evitare la divisione per zero. Il valore predefinito è 0,00001.

`FusedActivation`

Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Livello di attivazione fuso facoltativo da applicare dopo la normalizzazione.

## <a name="remarks"></a>Commenti
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** è un superset di funzionalità di [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). In questo caso, l'impostazione della matrice **Axes** su equivale all'impostazione di CrossChannel su FALSE in DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC , mentre l'impostazione della matrice Axes su equivale all'impostazione di `{ 0, 2, 3 }`     `{ 1, 2, 3 }` *CrossChannel* su **TRUE**.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore

*BiasTensor,* *InputTensor,* *OutputTensor* e *ScaleTensor* devono avere gli stessi *valori di DataType* *e DimensionCount.*

## <a name="tensor-support"></a>Supporto di Tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 e successive

| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Input facoltativo | Da 1 a 8 | FLOAT32, FLOAT16 |
| BiasTensor | Input facoltativo | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e successive

| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Input facoltativo | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Input facoltativo | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

[Uso di operatori fusibili per migliorare le prestazioni](../dml-fused-activations.md)