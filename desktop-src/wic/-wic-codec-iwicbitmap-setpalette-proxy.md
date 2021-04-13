---
description: Funzione proxy per il metodo sepalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Funzione IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525939"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a>\_Funzione proxy IWICBitmap Sepalette \_

Funzione proxy per il metodo [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _

Puntatore a questo oggetto [_ *IWICBitmap* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*pIPalette* \[ in\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Tavolozza da utilizzare per la conversione.

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



 

 




