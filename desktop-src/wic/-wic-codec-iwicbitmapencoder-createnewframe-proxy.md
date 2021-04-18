---
description: Funzione proxy per il metodo CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: Funzione IWICBitmapEncoder_CreateNewFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316817"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a>IWICBitmapEncoder \_ CreateNewFrame- \_ funzione proxy

Funzione proxy per il metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _

Puntatore a questo oggetto [_ *IWICBitmapEncoder* *](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .

</dd> <dt>

*ppIFrameEncode* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***

Puntatore che riceve un puntatore alla nuova istanza di un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).

</dd> <dt>

*ppIEncoderOptions* \[ in uscita\]
</dt> <dd>

Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***

Proprietà denominate da usare per l'inizializzazione del frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

