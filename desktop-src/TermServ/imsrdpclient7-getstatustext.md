---
title: Metodo GetStatusText IMsRdpClient7 (Openservice.h)
description: Recupera il testo dello stato per il codice di stato specificato.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Metodo GetStatusText Servizi Desktop remoto
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto metodo , GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto metodo , GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto metodo , GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto metodo , GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285191"
---
# <a name="imsrdpclient7getstatustext-method"></a>Metodo IMsRdpClient7::GetStatusText

Recupera il testo dello stato per il codice di stato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*statusCode* \[ Pollici\]
</dt> <dd>

UINT **che** specifica il codice di stato per cui recuperare il testo.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Indirizzo di un **BSTR che** riceve il testo di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Openservice.h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClient7 IID è definito come \_ b2a5b5ce-3461-444a-91d4-add26d070638<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





