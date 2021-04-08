---
title: Messaggio LVM_INSERTGROUPSORTED (COMmctrl. h)
description: Inserisce un gruppo in un elenco ordinato di gruppi.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Controlli di Windows Message LVM_INSERTGROUPSORTED
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874310"
---
# <a name="lvm_insertgroupsorted-message"></a>\_Messaggio INSERTGROUPSORTED LVM

Inserisce un gruppo in un elenco ordinato di gruppi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> contenente il gruppo da inserire.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere **null**.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

L'ordinamento dell'elenco è basato sull'ID del gruppo. L'ordine viene definito dalla funzione di ordinamento definita dall'applicazione, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), che viene passata nella struttura [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) dal parametro *wParam* .

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

