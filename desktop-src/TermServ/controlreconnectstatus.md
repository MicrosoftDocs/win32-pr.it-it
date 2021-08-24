---
title: Enumerazione ControlReconnectStatus
description: Specifica il risultato del metodo di riconnessione IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Enumerazione ControlReconnectStatus Servizi Desktop remoto
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635adbcafd5180dad967e2488b793f6907fd38cc848935a088bee59aad536354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738081"
---
# <a name="controlreconnectstatus-enumeration"></a>Enumerazione ControlReconnectStatus

Specifica il risultato del metodo [**IMsRdpClient8::Reconnect.**](imsrdpclient8-reconnect.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**
</dt> <dd>

L'operazione di riconnessione è stata avviata.

</dd> <dt>

<span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**
</dt> <dd>

Impossibile iniziare l'operazione di riconnessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





