---
title: Funzione FreeUiInfo (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una struttura UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo funzione NDF
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
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119391"
---
# <a name="freeuiinfo-function"></a>FreeUiInfo (funzione)

La funzione **FreeUiInfo** consente di deallocare la memoria allocata internamente a una struttura [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) . Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ in\]
</dt> <dd>

Tipo: **[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _

Struttura. La memoria allocata a cui fa riferimento questa struttura verrà liberata.

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

[_ *UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

