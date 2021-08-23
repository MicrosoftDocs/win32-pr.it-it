---
title: Metodo IMsTscAxEvents OnEnterFullScreenMode
description: Chiamato quando il client entra in modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL+ALT+INTERR).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Metodo OnEnterFullScreenMode Servizi Desktop remoto
- Metodo OnEnterFullScreenMode Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e40da93f0e29fb183cea540b0f195d61c4969d65c2b7829bf86d8e3c8eba81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512401"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>Metodo IMsTscAxEvents::OnEnterFullScreenMode

Chiamato quando il client entra in modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL+ALT+INTERR). [](terminal-services-shortcut-keys.md)

## <a name="syntax"></a>Sintassi


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





