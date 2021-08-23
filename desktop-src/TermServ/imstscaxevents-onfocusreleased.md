---
title: Metodo IMsTscAxEvents OnFocusReleased
description: Chiamato quando viene premuta la combinazione di tasti rilascia lo stato attivo. Ad esempio, questo evento viene chiamato quando l'utente preme CTRL+ALT+FRECCIA SINISTRA o la combinazione di tasti CTRL+ALT+FRECCIA DESTRA.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Metodo OnFocusReleased Servizi Desktop remoto
- Metodo OnFocusReleased Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673916c3a538f21ceea5b0b7578bb9e8f225ec2a349e38015eab0b50d73935aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512341"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>Metodo IMsTscAxEvents::OnFocusReleased

Chiamato quando viene premuta la combinazione di tasti rilascia lo stato attivo. Ad esempio, questo evento viene chiamato quando l'utente preme CTRL+ALT+FRECCIA SINISTRA o la combinazione di tasti CTRL+ALT+FRECCIA DESTRA.

Questo evento consente al ActiveX contenitore di controlli di portare via il controllo dal ActiveX controllo. Ad esempio, ciò è utile in uno scenario in cui non si dispone di un mouse e le combinazioni di tasti speciali, ad esempio ALT+TAB, vengono reindirizzate al server. In questo caso, non è possibile ripristinare lo stato attivo della tastiera sul desktop locale. Tuttavia, con la combinazione di tasti CTRL+ALT+FRECCIA SINISTRA o CTRL+ALT+FRECCIA DESTRA, il contenitore ActiveX può restare in ascolto di questo evento e rispondere allontanando lo stato attivo dal controllo ActiveX.

## <a name="syntax"></a>Sintassi


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iDirection* \[ Pollici\]
</dt> <dd>

Il parametro direction di 1 (CTRL+ALT+FRECCIA DESTRA) o 1 (CTRL+ALT+FRECCIA SINISTRA).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo evento è disponibile quando Connessione Desktop remoto 6.0 viene usato nel client.

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

 

 





