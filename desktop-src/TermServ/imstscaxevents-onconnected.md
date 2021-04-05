---
title: Metodo OnConnected IMsTscAxEvents
description: Chiamato quando il controllo client è in fase di creazione di una connessione con un server Host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Metodo OnConnected Servizi Desktop remoto
- Metodo OnConnected Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, Metodo OnConnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741322"
---
# <a name="imstscaxeventsonconnected-method"></a>Metodo IMsTscAxEvents:: OnConnected

Chiamato quando il controllo client è in fase di creazione di una connessione con un server Host sessione Desktop remoto (host sessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```C++
void OnConnected();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere una notifica che il controllo ha stabilito una connessione con un server Host sessione Desktop remoto.

Per ulteriori informazioni sulla chiamata a questo metodo, vedere l'evento [**IMsTscAxEvents:: OnLoginComplete**](imstscaxevents-onlogincomplete.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





