---
title: Funzione FreeHelperAttributes (Ndattributils.h)
description: Dealloca la memoria allocata internamente a una matrice di strutture ATTRIBUTE \_ HELPER.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Funzione FreeHelperAttributes NDF
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
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802431"
---
# <a name="freehelperattributes-function"></a>Funzione FreeHelperAttributes

La **funzione FreeHelperAttributes** dealloca la memoria allocata internamente a una matrice di [**strutture HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Questa funzione chiama [**CoTaskMemFree per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) deallocare la memoria.

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

*pInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ATTRIBUTO \_ HELPER**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Matrice di strutture . Verrà liberata la memoria allocata a cui puntano queste strutture.

</dd> <dt>

*HelperAttributeCount* 
</dt> <dd>

Tipo: **ULONG**

Numero di strutture nella matrice a cui punta *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **BOOL**

True se è necessario eliminare anche la matrice di strutture. in caso contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ATTRIBUTO \_ HELPER**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

