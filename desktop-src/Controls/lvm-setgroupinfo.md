---
title: LVM_SETGROUPINFO messaggio (Commctrl.h)
description: Imposta le informazioni sul gruppo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553a81c3cfe962ae6daf5ae4c988964028554bc662cec08df40c16fd8b4eb43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077271"
---
# <a name="lvm_setgroupinfo-message"></a>Messaggio LVM \_ SETGROUPINFO

Imposta le informazioni sul gruppo. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView SetGroupInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>ID che specifica il gruppo di cui devono essere impostate le informazioni.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntatore a [**una struttura LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) che contiene le informazioni da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID del gruppo in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Per modificare un ID gruppo di un gruppo <b>esistente,</b> aggiungere LVGF_GROUPID a <b>LVGROUP.mask</b> e impostare <b>LVGROUP.iGroupId</b> sul nuovo ID. La chiamata avrà esito negativo <b>se LVGROUP.iGroupId</b> contiene l'ID di un gruppo esistente.

Per aggiornare altre proprietà di un gruppo esistente(ad esempio, aggiornare un allineamento del testo dell'intestazione o del piè di pagina per il gruppo, <b>uAlign</b>) <b>LVGROUP.mask</b> non deve contenere LVGF_GROUPID , <b>altrimenti</b>l'aggiornamento avrà esito negativo.

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





