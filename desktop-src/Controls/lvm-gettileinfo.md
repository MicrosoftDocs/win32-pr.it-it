---
title: Messaggio LVM_GETTILEINFO (COMmctrl. h)
description: Recupera le informazioni su un riquadro in un controllo visualizzazione elenco.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Controlli di Windows Message LVM_GETTILEINFO
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048643"
---
# <a name="lvm_gettileinfo-message"></a>\_Messaggio GETTILEINFO LVM

Recupera le informazioni su un riquadro in un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> che riceve le informazioni recuperate.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

Visualizzazione affiancata è un nuovo modo per organizzare e visualizzare gli elementi in un controllo visualizzazione elenco. Le altre viste sono Icon, Small Icon, Details ed List.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





