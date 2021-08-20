---
title: Classe IMemoryAllocator
description: Implementato dall'allocatore di memoria per la funzione StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Classe IMemoryAllocator structured Archiviazione
- Descrizione della classe Structured Archiviazione IMemoryAllocator
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
ms.openlocfilehash: d3a92cb2fa31b937a86acd80d2e7be9c83fb1d01476a2f50a856494d8f2a0d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961756"
---
# <a name="imemoryallocator-class"></a>Classe IMemoryAllocator

La **classe IMemoryAllocator** viene implementata dall'allocatore di memoria per [**la funzione StgConvertPropertyToVariant.**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)

## <a name="methods"></a>Metodi



| Nome                                                     | Descrizione                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Allocare**](imemoryallocator-allocate.md)<br/> | Alloca memoria per la [**funzione StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando la funzione converte un tipo di dati **SERIALIZEDPROPERTYVALUE** in un tipo di dati **PROPVARIANT.**<br/> |
| [**Gratuito**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libera la memoria allocata dal [**metodo Allocate.**](imemoryallocator-allocate.md)<br/>                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Questa classe viene usata solo dalla [**funzione StgConvertPropertyToVariant.**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

