---
title: Metodo di riconnessione IMsRdpClient8
description: Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Metodo di riconnessione Servizi Desktop remoto
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo di riconnessione
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo di riconnessione
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo di riconnessione
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519246"
---
# <a name="imsrdpclient8reconnect-method"></a>Metodo IMsRdpClient8:: Reconnect

Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop. Il controllo deve essere già connesso a una sessione remota affinché questo metodo abbia esito positivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulWidth* \[ in\]
</dt> <dd>

Tipo: **ULONG**

La nuova larghezza del desktop, in pixel. Per le restrizioni relative ai valori, vedere la proprietà [**DesktopWidth**](imstscax-desktopwidth.md) .

</dd> <dt>

*ulHeight* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Nuova altezza del desktop, in pixel. Per le restrizioni relative ai valori, vedere la proprietà [**DesktopHeight**](imstscax-desktopheight.md) .

</dd> <dt>

*pReconnectStatus* \[ out, retval\]
</dt> <dd>

Tipo: **[**ControlReconnectStatus**](controlreconnectstatus.md) \** _

Puntatore a una variabile [_ *ControlReconnectStatus* *](controlreconnectstatus.md) che riceve lo stato dell'operazione di riconnessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 è definito come 4247E044-9271-43a9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**ControlReconnectStatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





