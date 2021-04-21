---
title: Costanti DirectML
description: Le costanti seguenti vengono dichiarate in `DirectML.h` .
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
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803404"
---
# <a name="directml-constants"></a>Costanti DirectML

Le costanti seguenti vengono dichiarate in `DirectML.h` .

| Costante | Valore | Descrizione |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | I tensori DirectML supportano un massimo di 5 dimensioni per DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | I tensori DirectML supportano un massimo di 8 dimensioni per DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | I buffer temporanei e persistenti devono avere un indirizzo di base allineato a 256 byte. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | I buffer temporanei e persistenti devono avere un indirizzo di base allineato a 256 byte. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | I tensori del buffer hanno un requisito minimo di allineamento degli indirizzi di base di 16 byte. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | DirectML.h |

## <a name="see-also"></a>Vedi anche

* [Informazioni di riferimento su DirectML](direct3d-directml-reference.md)
* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
