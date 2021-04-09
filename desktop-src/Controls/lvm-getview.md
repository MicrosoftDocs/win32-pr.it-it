---
title: Messaggio LVM_GETVIEW (COMmctrl. h)
description: Recupera la visualizzazione corrente di un controllo visualizzazione elenco.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Controlli di Windows Message LVM_GETVIEW
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120974"
---
# <a name="lvm_getview-message"></a>\_Messaggio LVM GETview

Recupera la visualizzazione corrente di un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che specifica la visualizzazione corrente.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori per le visualizzazioni.

-   \_dettagli vista \_ LV
-   \_icona di visualizzazione LV \_
-   \_elenco viste \_ LV
-   \_SMALLICON vista \_ LV
-   \_riquadro Vista \_ LV

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





