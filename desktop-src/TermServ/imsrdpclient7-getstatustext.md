---
title: Metodo IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera il testo di stato per il codice di stato specificato.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo GetStatusText
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
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742143"
---
# <a name="imsrdpclient7getstatustext-method"></a>Metodo IMsRdpClient7:: GetStatusText

Recupera il testo di stato per il codice di stato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*statusCode* \[ in\]
</dt> <dd>

**Uint** che specifica il codice di stato per il quale recuperare il testo.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Indirizzo di un **BSTR** che riceve il testo dello stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>OpenService. h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638<br/>         |



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

 

 





