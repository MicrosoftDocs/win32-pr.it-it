---
title: WMDM_FIND_SCOPE enumerazione
description: Il tipo di enumerazione FIND SCOPE di WMDM \_ \_ definisce l'ambito dell'oggetto di archiviazione.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE enumerazione Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb7d4902b1acd4223f25bdc5e8a7ca76d4495b5f465687a56b295ad2d5fbfa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863011"
---
# <a name="wmdm_find_scope-enumeration"></a>Enumerazione \_ FIND SCOPE di WMDM \_

Il **tipo di enumerazione FIND \_ \_ SCOPE di WMDM** definisce l'ambito dell'oggetto di archiviazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ FIND \_ SCOPE \_ GLOBAL**
</dt> <dd>

Ricerca dell'oggetto corrispondente in qualsiasi punto del dispositivo.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**ELEMENTI FIGLIO \_ \_ IMMEDIATI \_ DELL'AMBITO FIND WMDM \_**
</dt> <dd>

Ricerca dell'oggetto corrispondente all'interno di questa archiviazione e dei relativi elementi figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





