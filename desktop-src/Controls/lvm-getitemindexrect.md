---
title: LVM_GETITEMINDEXRECT messaggio (Commctrl.h)
description: Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetItemIndexRect.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3e6d0420bfddb974d13f210c84241cefc5d79f0ee5a82920bdc2961879dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770371"
---
# <a name="lvm_getitemindexrect-message"></a>Messaggio LVM \_ GETITEMINDEXRECT

Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetItemIndexRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento padre dell'elemento secondario. Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri. *wParam* non deve essere **NULL.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate. Il processo chiamante è responsabile dell'allocazione di questa struttura. *lParam* non deve essere **NULL.** Impostare il **primo membro** sull'indice dell'elemento secondario. Impostare il **membro** sinistro su uno dei valori seguenti, che indica la parte dell'elemento secondario per cui recuperare il rettangolo di delimitazione.



| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LIMITI DI \_ LVIR**</dt> </dl> | Restituisce il rettangolo di delimitazione dell'intero elemento secondario, incluse l'icona e l'etichetta.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ICONA \_ LVIR**</dt> </dl>       | Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola dell'elemento secondario.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**ETICHETTA \_ LVIR**</dt> </dl>    | Restituisce il rettangolo di delimitazione del testo dell'elemento secondario.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

