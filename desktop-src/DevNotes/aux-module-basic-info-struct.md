---
description: Contiene informazioni di base sul modulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO struttura (Aux \_ klib.h)
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
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956150"
---
# <a name="aux_module_basic_info-structure"></a>Struttura DELLE INFORMAZIONI \_ \_ DI BASE DEL \_ MODULO AUX

Contiene informazioni di base sul modulo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ImageBase**
</dt> <dd>

Indirizzo di base del modulo all'interno dello spazio indirizzi del kernel.

</dd> </dl>

## <a name="remarks"></a>Commenti

La libreria di oggetti che implementa questa API può essere scaricata da [qui.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria API ausiliaria versione 1.0 o successiva<br/>                          |
| Intestazione<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




