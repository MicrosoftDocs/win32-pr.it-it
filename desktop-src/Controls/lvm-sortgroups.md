---
title: LVM_SORTGROUPS messaggio (Commctrl.h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo visualizzazione elenco.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS controlli Windows messaggio
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
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670785"
---
# <a name="lvm_sortgroups-message"></a>Messaggio \_ LVM SORTGROUPS

Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Puntatore a una funzione di confronto definita dall'applicazione, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare.</a></dd> <dt>

*lParam* 
</dt> <dd>Puntatore Void alle informazioni definite dall'applicazione.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 in caso di esito positivo oppure 0 in caso contrario.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto che Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

