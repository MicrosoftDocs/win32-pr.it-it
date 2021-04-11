---
title: Messaggio LVM_SETTILEINFO (COMmctrl. h)
description: Imposta le informazioni per un riquadro esistente di un controllo visualizzazione elenco.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Controlli di Windows Message LVM_SETTILEINFO
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119459"
---
# <a name="lvm_settileinfo-message"></a>\_Messaggio SETTILEINFO LVM

Imposta le informazioni per un riquadro esistente di un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> che contiene le informazioni da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

**LVM \_ SETTILEINFO** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





