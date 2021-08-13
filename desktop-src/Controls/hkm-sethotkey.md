---
title: HKM_SETHOTKEY messaggio (Commctrl.h)
description: Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta rapida.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae397e3034e917eec85a6b56397cbac8b14a59af03aca6ebee08fec89cf6b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672259"
---
# <a name="hkm_sethotkey-message"></a>Messaggio HKM \_ SETHOTKEY

Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**IL LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta rapida. [**L'HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) di **LOWORD** è il modificatore di tasto che indica i tasti che definiscono una combinazione di tasti di scelta rapida. Per un elenco dei valori del flag di modifica, vedere la descrizione del [**messaggio \_ GETHOTKEY HKM.**](hkm-gethotkey.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

