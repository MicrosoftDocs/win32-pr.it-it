---
title: Metodo IMsRdpClient9 SyncSessionDisplaySettings
description: Sincronizza le impostazioni di visualizzazione della sessione.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Metodo SyncSessionDisplaySettings Servizi Desktop remoto
- Metodo SyncSessionDisplaySettings Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SyncSessionDisplaySettings
- Metodo SyncSessionDisplaySettings Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a8021c4e0b7af0de000b96d5b2b094f5894b84746dedf98f699a693a6bddd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990371"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a>Metodo IMsRdpClient9::SyncSessionDisplaySettings

Sincronizza le impostazioni di visualizzazione della sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                                                                                                                                                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID \_ IMsRdpClient9 è definito come 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





