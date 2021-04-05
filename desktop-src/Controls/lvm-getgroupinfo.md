---
title: Messaggio LVM_GETGROUPINFO (COMmctrl. h)
description: Ottiene le informazioni sul gruppo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Controlli di Windows Message LVM_GETGROUPINFO
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048197"
---
# <a name="lvm_getgroupinfo-message"></a>\_Messaggio GETGROUPINFO LVM

Ottiene le informazioni sul gruppo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>ID che specifica il gruppo le cui informazioni vengono recuperate.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore A una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> che riceve le informazioni recuperate. Impostare il membro **cbSize** della struttura su sizeof (LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID del gruppo, se ha esito positivo, oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Prima di tentare di recuperare l'intestazione per un gruppo, verificare innanzitutto che il gruppo non abbia lo \_ stile NOheader LBGS.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





