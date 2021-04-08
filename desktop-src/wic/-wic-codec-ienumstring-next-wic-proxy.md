---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Next.'
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: Funzione IEnumString_Next_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049457"
---
# <a name="ienumstring_next_wic_proxy-function"></a>\_ \_ Funzione proxy WIC successiva IEnumString \_

Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Next.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **IEnumString \** _

PARAMDESC

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




