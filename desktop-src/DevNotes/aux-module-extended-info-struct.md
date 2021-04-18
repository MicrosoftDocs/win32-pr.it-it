---
description: Contiene informazioni estese sul modulo.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Struttura AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331719"
---
# <a name="aux_module_extended_info-structure"></a>\_Struttura di \_ informazioni estese del modulo aux \_

Contiene informazioni estese sul modulo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**BasicInfo**
</dt> <dd>

Struttura [**di \_ \_ \_ informazioni di base del modulo aux**](aux-module-basic-info-struct.md) .

</dd> <dt>

**ImageSize**
</dt> <dd>

Dimensione, in byte, del modulo caricato.

</dd> <dt>

**FileNameOffset**
</dt> <dd>

Offset del nome file all'interno del buffer **FullPathName** .

</dd> <dt>

**FullPathName**
</dt> <dd>

Percorso completo del modulo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Libreria API ausiliaria Windows versione 1,0 o successiva<br/>                          |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**\_informazioni di \_ base sul modulo aux \_**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




