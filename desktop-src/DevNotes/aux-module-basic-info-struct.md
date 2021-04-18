---
description: Contiene informazioni di base sul modulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Struttura AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330559"
---
# <a name="aux_module_basic_info-structure"></a>\_Struttura delle \_ informazioni di base del modulo aux \_

Contiene informazioni di base sul modulo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ImageBase sul**
</dt> <dd>

Indirizzo di base del modulo nello spazio degli indirizzi del kernel.

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
</dt> </dl>

 

 




