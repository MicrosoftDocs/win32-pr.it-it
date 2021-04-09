---
title: Messaggio LVM_SORTGROUPS (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo di visualizzazione elenco.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Controlli di Windows Message LVM_SORTGROUPS
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120958"
---
# <a name="lvm_sortgroups-message"></a>\_Messaggio SORTGROUPS LVM

Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo di visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Puntatore a una funzione di confronto definita dall'applicazione, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore void alle informazioni definite dall'applicazione.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se ha esito positivo oppure 0 in caso contrario.

## <a name="remarks"></a>Commenti

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

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

