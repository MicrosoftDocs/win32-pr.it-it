---
title: Enumerazione WMDM_FIND_SCOPE
description: Il \_ \_ tipo di enumerazione WMDM Find scope definisce l'ambito dell'oggetto di archiviazione.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Enumerazione WMDM_FIND_SCOPE Windows Media Gestione dispositivi
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
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325012"
---
# <a name="wmdm_find_scope-enumeration"></a>\_Enumerazione WMDM Find \_ scope

Il tipo di enumerazione **WMDM \_ Find \_ scope** definisce l'ambito dell'oggetto di archiviazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ trova \_ ambito \_ globale**
</dt> <dd>

Ricerca dell'oggetto corrispondente in qualsiasi punto del dispositivo.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ trova \_ ambito \_ elementi figlio immediati \_**
</dt> <dd>

Ricerca dell'oggetto corrispondente all'interno di questa risorsa di archiviazione e dei relativi elementi figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





