---
description: Funzione proxy per il metodo GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: Funzione IWICPalette_GetType_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314888"
---
# <a name="iwicpalette_gettype_proxy-function"></a>\_Funzione proxy GetType IWICPalette \_

Funzione proxy per il metodo [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Puntatore a questo oggetto [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*pePaletteType* \[ out\]
</dt> <dd>

Tipo: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _

Puntatore che riceve il tipo di tavolozza di bimtap.

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



 

 




