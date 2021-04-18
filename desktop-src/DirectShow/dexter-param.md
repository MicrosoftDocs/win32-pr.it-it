---
description: Specifica il valore che una proprietà presuppone in un determinato momento.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Struttura DEXTER_PARAM (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329147"
---
# <a name="dexter_param-structure"></a>\_Struttura param di Dexter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Specifica il valore che una proprietà presuppone in un determinato momento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Nome della proprietà.

</dd> <dt>

**dispID**
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

**nValori**
</dt> <dd>

Numero di valori assunti dalla proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto deve supportare l'interfaccia **IDispatch** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**\_valore Dexter**](dexter-value.md)
</dt> </dl>

 

 




