---
title: Costanti DirectML
description: Le costanti seguenti sono dichiarate in `DirectML.h` .
keywords:
- Costanti
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322164"
---
# <a name="directml-constants"></a>Costanti DirectML

Le costanti seguenti sono dichiarate in `DirectML.h` .

| Costante | Valore | Descrizione |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | I tensori DirectML supportano un massimo di 5 dimensioni per DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | I tensori DirectML supportano un massimo di 8 dimensioni per DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | I buffer temporanei e permanenti devono avere un indirizzo di base allineato a 256 byte. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | I buffer temporanei e permanenti devono avere un indirizzo di base allineato a 256 byte. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | I tempi di risoluzione del buffer hanno un requisito minimo di allineamento degli indirizzi di base di 16 byte. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | D3D12. h |

## <a name="see-also"></a>Vedi anche

* [Riferimento a DirectML](direct3d-directml-reference.md)
* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
