---
title: Metodo IMsTscAxEvents OnRemoteDesktopSizeChange
description: Chiamato per indicare che le dimensioni del controllo client sul desktop remoto sono state modificate in risposta a un'operazione di controllo client.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Metodo OnRemoteDesktopSizeChange Servizi Desktop remoto
- Metodo OnRemoteDesktopSizeChange Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316b70c3405c13dd50c773d36c20f036c9e99aebeb3e5dedae692c2f9ad772fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125091"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>Metodo IMsTscAxEvents::OnRemoteDesktopSizeChange

Chiamato per indicare che le dimensioni del controllo client sul desktop remoto sono state modificate in risposta a un'operazione di controllo client.

## <a name="syntax"></a>Sintassi


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*width* \[ Pollici\]
</dt> <dd>

Larghezza, in pixel, del desktop remoto ridimensionato.

</dd> <dt>

*height* \[ Pollici\]
</dt> <dd>

Altezza, in pixel, del desktop remoto ridimensionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo evento consente al contenitore di determinare se deve essere ridimensionato in risposta a un'operazione di controllo client, il che potrebbe comportare dimensioni del desktop visualizzabili maggiori. Si noti che il controllo regola automaticamente le barre di scorrimento per le nuove dimensioni della sessione.

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

 

 





