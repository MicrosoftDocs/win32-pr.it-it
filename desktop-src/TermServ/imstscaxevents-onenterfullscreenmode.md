---
title: Metodo IMsTscAxEvents OnEnterFullScreenMode
description: Chiamato quando il client entra in modalità schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL + ALT + INTERr).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnEnterFullScreenMode
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
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964420"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>Metodo IMsTscAxEvents:: OnEnterFullScreenMode

Chiamato quando il client entra in modalità schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).

## <a name="syntax"></a>Sintassi


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

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

 

 





