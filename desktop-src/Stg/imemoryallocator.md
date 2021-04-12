---
title: Classe IMemoryAllocator
description: Implementato dall'allocatore di memoria per la funzione StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Archiviazione strutturata della classe IMemoryAllocator
- Archiviazione strutturata della classe IMemoryAllocator, descritta
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400677"
---
# <a name="imemoryallocator-class"></a>Classe IMemoryAllocator

La classe **IMemoryAllocator** viene implementata dall'allocatore di memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="methods"></a>Metodi



| Nome                                                     | Descrizione                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Allocare**](imemoryallocator-allocate.md)<br/> | Alloca memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando la funzione converte un tipo di dati **SERIALIZEDPROPERTYVALUE** in un tipo di dati **PROPVARIANT** .<br/> |
| [**Gratuito**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libera la memoria allocata dal metodo [**allocate**](imemoryallocator-allocate.md) .<br/>                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Questa classe viene utilizzata solo dalla funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

