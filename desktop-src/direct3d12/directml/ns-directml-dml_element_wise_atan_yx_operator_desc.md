---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Calcola l'arcotangente a 2 argomenti per ogni elemento di *ATensor* e *BTensor*, dove *ATensor* è l'asse *Y* e *BTensor* è l'asse *X*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804499"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a>DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)

Calcola l'arcotangente a 2 argomenti per ogni elemento di *ATensor* e *BTensor*, dove *ATensor* è l'asse *Y* e *BTensor* è l'asse *X*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*. Questo operatore non è definito per l'origine, ovvero quando *ATensor* e *BTensor* sono entrambi 0 per gli elementi corrispondenti.

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

Questo operatore supporta l'esecuzione sul posto, vale a dire che al tensore di output è consentito l'alias *ATensor* o *BTensor* durante l'associazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Members

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di input da cui leggere i valori dell'asse Y.

`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di input da cui leggere i valori dell'asse X.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i risultati.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *datatype*, *DimensionCount* e *Sizes*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| BTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
