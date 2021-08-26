---
title: LVM_SETINFOTIP messaggio (Commctrl.h)
description: Imposta il testo della descrizione comando in risposta ritardata alla \_ notifica LVN GETINFOTIP.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef739535e399550911adfbe86d7376d3efeb77cd797ba807b24ee682d1f3fe3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919901"
---
# <a name="lvm_setinfotip-message"></a>Messaggio \_ LVM SETINFOTIP

Imposta il testo della descrizione comando in risposta ritardata alla [ \_ notifica LVN GETINFOTIP.](lvn-getinfotip.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">una struttura LVSETINFOTIP</a> che contiene le informazioni da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il testo della descrizione comando è impostato correttamente oppure FALSE in **caso** contrario.

## <a name="remarks"></a>Commenti

Il **messaggio \_ LVM SETINFOTIP** consente a un'applicazione di calcolare le descrizioni comandi in background seguendo questa procedura:

1.  In risposta alla notifica [LVN \_ GETINFOTIP,](lvn-getinfotip.md) impostare il membro **pszText** della [**struttura NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) su una stringa vuota e restituire 0.
2.  In background, calcolare la descrizione comando.
3.  Dopo aver calcolato la descrizione comandi, inviare il messaggio **LVM \_ SETINFOTIP,** impostando il membro **pszText** della struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sulla descrizione comandi e i **membri iItem** e **iSubItem** all'elemento e alla sottoelemento a cui si applica la descrizione comandi.

Il testo passato al messaggio **LVM \_ SETINFOTIP** viene visualizzato solo se l'elemento e l'elemento secondario descritti dalla struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sono ancora in uno stato che richiede una descrizione comandi

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





