---
title: Metodo di connessione IMsTscAx
description: Avvia una connessione utilizzando le proprietà attualmente impostate nel controllo.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Metodo Connect Servizi Desktop remoto
- Metodo Connect Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963965"
---
# <a name="imstscaxconnect-method"></a>Metodo IMsTscAx:: Connect

Avvia una connessione utilizzando le proprietà attualmente impostate nel controllo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

L'unica proprietà obbligatoria è il nome del server. Fare riferimento alla proprietà [**Server**](imstscax-server.md) .

Il controllo si connette in modo asincrono, quindi un ritorno da una chiamata Connect indica solo che la connessione è stata avviata correttamente, non che è stata completata. È necessario rispondere agli eventi sull'interfaccia [**IMsTscAxEvents**](imstscaxevents-interface.md) per determinare quando il controllo è stato connesso correttamente o è stato disconnesso.

Questo metodo restituisce **E ha \_ esito negativo** se viene chiamato quando il controllo è già connesso o nello stato di connessione.

Una volta chiamata la **connessione** , la maggior parte delle proprietà del controllo non può più essere impostata finché il controllo non torna allo stato disconnesso.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Disconnetti**](imstscax-disconnect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





