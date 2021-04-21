---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Esegue la funzione di attivazione celu (Exponential Linear Unit) continuamente differenziabile su ogni elemento in *InputTensor,* inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803729"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a>DML_ACTIVATION_CELU_OPERATOR_DESC struttura (directml.h)

Esegue la funzione di attivazione celu (Exponential Linear Unit) continuamente differenziabile su ogni elemento in *InputTensor,* inserendo il risultato nell'elemento corrispondente di *OutputTensor*.

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

Dove:
* exp(x) è la funzione di esponente naturale
* max(a,b) restituisce il valore più grande dei due valori a,b
* min(a,b) restituisce il valore più piccolo dei due valori a,b

Questo operatore supporta l'esecuzione sul posto, vale a dire che al tensore di output è consentito l'alias *InputTensor* durante l'associazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di input da cui leggere.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i risultati.

`Alpha`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Coefficiente alfa. Un valore predefinito tipico per questo valore è 1.0.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere gli stessi *datatype*, *DimensionCount* e *Sizes*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |