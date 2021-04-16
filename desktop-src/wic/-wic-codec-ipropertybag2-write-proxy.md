---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: Funzione IPropertyBag2_Write_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343251"
---
# <a name="ipropertybag2_write_proxy-function"></a>\_Funzione proxy di scrittura IPropertyBag2 \_

Funzione proxy di Windows Imaging Component (WIC) per IPropertyBag2:: Write.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _

PARAMDESC

</dd> <dt>

_cProperties * \[ in\]
</dt> <dd>

Tipo: **ULONG**

</dd> <dt>

*ppropBag* \[ in\]
</dt> <dd>

Tipo: **[Campo PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _

</dd> <dt>

_pvarValue * \[ in\]
</dt> <dd>

Tipo: **Variant \** _

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



 

