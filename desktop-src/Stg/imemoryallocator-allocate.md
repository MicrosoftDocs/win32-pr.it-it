---
title: Metodo allocate IMemoryAllocator
description: Il metodo allocate alloca memoria per la funzione StgConvertPropertyToVariant quando la funzione converte un tipo di dati SERIALIZEDPROPERTYVALUE in un tipo di dati PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Allocare l'archiviazione strutturata del metodo
- Allocare l'archiviazione strutturata del metodo, interfaccia IMemoryAllocator
- Archiviazione strutturata dell'interfaccia IMemoryAllocator, metodo allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300950"
---
# <a name="imemoryallocatorallocate-method"></a>Metodo IMemoryAllocator:: allocate

Il metodo **allocate** alloca memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando la funzione converte un tipo di dati **SERIALIZEDPROPERTYVALUE** in un tipo di dati **PROPVARIANT** .

## <a name="syntax"></a>Sintassi


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cbSize* \[ in\]
</dt> <dd>

Specifica le dimensioni della memoria da allocare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

