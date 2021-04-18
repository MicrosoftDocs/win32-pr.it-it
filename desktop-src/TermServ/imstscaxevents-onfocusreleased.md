---
title: Metodo IMsTscAxEvents OnFocusReleased
description: Chiamato quando viene premuta la combinazione di tasti di attivazione della versione. Questo evento, ad esempio, viene chiamato quando l'utente preme CTRL + ALT + freccia sinistra o la combinazione di tasti CTRL + ALT + freccia destra.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnFocusReleased
- Metodo OnFocusReleased Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnFocusReleased
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
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301879"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>Metodo IMsTscAxEvents:: OnFocusReleased

Chiamato quando viene premuta la combinazione di tasti di attivazione della versione. Questo evento, ad esempio, viene chiamato quando l'utente preme CTRL + ALT + freccia sinistra o la combinazione di tasti CTRL + ALT + freccia destra.

Questo evento consente al contenitore di controlli ActiveX di prendere il controllo dal controllo ActiveX. Questo, ad esempio, è utile in uno scenario in cui non è presente un mouse e le combinazioni di tasti speciali, ad esempio ALT + TAB, vengono reindirizzate al server. In questo caso, non è possibile riportare lo stato attivo alla tastiera sul desktop locale. Tuttavia, con la combinazione di tasti CTRL + ALT + freccia sinistra o CTRL + ALT + freccia destra, il contenitore ActiveX può restare in ascolto di questo evento e rispondere spostando lo stato attivo dal controllo ActiveX.

## <a name="syntax"></a>Sintassi


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iDirection* \[ in\]
</dt> <dd>

Il parametro direction di 1 (CTRL + ALT + freccia destra) o 1 (CTRL + ALT + freccia sinistra).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo evento è disponibile quando nel client viene usato Connessione Desktop remoto 6,0.

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

 

 





