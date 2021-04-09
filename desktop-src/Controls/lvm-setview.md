---
title: Messaggio LVM_SETVIEW (COMmctrl. h)
description: Imposta la visualizzazione di un controllo visualizzazione elenco.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Controlli di Windows Message LVM_SETVIEW
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120959"
---
# <a name="lvm_setview-message"></a>Messaggio di visualizzazione a LVM \_

Imposta la visualizzazione di un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** che specifica la visualizzazione.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se ha esito positivo oppure-1 in caso contrario. Se, ad esempio, la vista non è valida, viene restituito-1.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori per le visualizzazioni.

-   \_dettagli vista \_ LV
-   \_icona di visualizzazione LV \_
-   \_elenco viste \_ LV
-   \_SMALLICON vista \_ LV
-   \_riquadro Vista \_ LV

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comctl32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





