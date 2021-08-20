---
title: LVM_GETGROUPRECT messaggio (Commctrl.h)
description: Ottiene il rettangolo per un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetGroupRect.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89340015972799b059e4568b5e87be511b7fc3718e7e7494d1bf46296886f030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540921"
---
# <a name="lvm_getgrouprect-message"></a>Messaggio LVM \_ GETGROUPRECT

Ottiene il rettangolo per un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetGroupRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Specifica il gruppo in base **a iGroupId** (vedere [**struttura LVGROUP).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per ricevere informazioni sul gruppo specificato da *wParam.* Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.

Il processo chiamante è responsabile dell'allocazione della memoria per la struttura . Impostare il **membro** superiore di [**RECT**](/previous-versions//dd162897(v=vs.85)) su uno dei flag seguenti per specificare le coordinate del rettangolo da ottenere.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**GRUPPO \_ LVGGR**</dt> </dl>                | Coordinate dell'intero gruppo espanso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**INTESTAZIONE \_ LVGGR**</dt> </dl>             | Coordinate solo dell'intestazione (gruppo compresso).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**ETICHETTA \_ LVGGR**</dt> </dl>                | Coordinate solo dell'etichetta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Coordinate solo del collegamento del subset (subset di markup). Un controllo visualizzazione elenco può limitare il numero di elementi visibili visualizzati in ogni gruppo. Viene visualizzato un collegamento all'utente per consentire all'utente di espandere il gruppo. Questo flag restituirà il rettangolo di delimitazione del collegamento del subset se il gruppo è un subset (stato del gruppo di LVGS SUBSETED, vedere la struttura \_ [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), stato **membro**). Questo flag viene fornito in modo che le applicazioni di accessibilità possano trovare il collegamento.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

