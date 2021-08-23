---
title: EM_GETCUEBANNER messaggio (Commctrl.h)
description: Ottiene il testo visualizzato come suggerimento testuale in un controllo di modifica.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5a47811adcd13c0f2531bd645a9ea607dd68c4dd2c1154f226a54cf108b291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019719"
---
# <a name="em_getcuebanner-message"></a>Messaggio \_ EM GETCUEBANNER

Ottiene il testo visualizzato come suggerimento testuale in un controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer Unicode che riceve il set di testo come segnale testuale. Il chiamante è responsabile dell'allocazione del buffer.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Dimensione del buffer a cui punta *wParam* nei **WCHAR,** inclusa la **terminazione NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modificare \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





