---
title: Messaggio LVM_SETGROUPINFO (COMmctrl. h)
description: Imposta le informazioni sul gruppo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Controlli di Windows Message LVM_SETGROUPINFO
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
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047854"
---
# <a name="lvm_setgroupinfo-message"></a>\_Messaggio SETGROUPINFO LVM

Imposta le informazioni sul gruppo. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetGroupInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>ID che specifica il gruppo di cui è necessario impostare le informazioni.</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>Puntatore a una struttura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) che contiene le informazioni da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID del gruppo, se ha esito positivo, oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Per modificare l'ID di un gruppo esistente, aggiungere <b>LVGF_GROUPID</b> a <b>LVGROUP. mask</b> e impostare <b>LVGROUP. iGroupId</b> sul nuovo ID. La chiamata avrà esito negativo se <b>LVGROUP. iGroupId</b> contiene l'ID di un gruppo esistente.

Per aggiornare altre proprietà di un gruppo esistente (ad esempio, aggiornare un allineamento del testo dell'intestazione o del piè di pagina per il gruppo, <b>uAlign</b>) <b>LVGROUP. mask</b> non deve contenere <b>LVGF_GROUPID</b>. in caso contrario, l'aggiornamento avrà esito negativo.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





