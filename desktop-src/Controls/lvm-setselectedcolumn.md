---
title: Messaggio LVM_SETSELECTEDCOLUMN (COMmctrl. h)
description: Imposta l'indice della colonna selezionata.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Controlli di Windows Message LVM_SETSELECTEDCOLUMN
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874714"
---
# <a name="lvm_setselectedcolumn-message"></a>\_Messaggio SETSELECTEDCOLUMN LVM

Imposta l'indice della colonna selezionata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Valore di tipo **int** che specifica l'indice di colonna.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

Gli indici di colonna vengono archiviati in una matrice **int** . Vedere il membro **puColumns** di [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





