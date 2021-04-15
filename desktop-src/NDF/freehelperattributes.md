---
title: Funzione FreeHelperAttributes (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una matrice di \_ strutture di attributi helper.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes funzione NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475988"
---
# <a name="freehelperattributes-function"></a>FreeHelperAttributes (funzione)

La funzione **FreeHelperAttributes** consente di deallocare la memoria allocata internamente a una matrice di strutture di [**\_ attributi Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ in\]
</dt> <dd>

Tipo: **\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _

Matrice di strutture. La memoria allocata a cui fanno riferimento queste strutture verrà liberata.

</dd> <dt>

_HelperAttributeCount * 
</dt> <dd>

Tipo: **ULONG**

Numero di strutture nella matrice a cui punta *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **bool**

True se è necessario eliminare anche la matrice di strutture. in caso contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Helper ( \_ attributo)**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

