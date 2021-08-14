---
title: Funzione FreeUiInfo (Ndattributils.h)
description: Dealloca la memoria allocata internamente a una struttura UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- Funzione FreeUiInfo NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e2008ddabdb412c117a3cfac5f2eb5ebf1e722f5f3729fb7c8b2ee0c394c454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939048"
---
# <a name="freeuiinfo-function"></a>Funzione FreeUiInfo

La **funzione FreeUiInfo** dealloca la memoria allocata internamente a una [**struttura UiInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) Questa funzione chiama [**CoTaskMemFree per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\***

Struttura . La memoria allocata a cui punta questa struttura verrà liberata.

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

[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

