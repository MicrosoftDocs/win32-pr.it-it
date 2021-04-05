---
title: Messaggio LVM_DELETECOLUMN (COMmctrl. h)
description: Rimuove una colonna da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteColumn di ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Controlli di Windows Message LVM_DELETECOLUMN
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739970"
---
# <a name="lvm_deletecolumn-message"></a>\_Messaggio DELETECOLUMN LVM

Rimuove una colonna da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna da eliminare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

L'eliminazione della colonna zero di un controllo visualizzazione elenco è supportata solo in ComCtl32.dll versione 6 e successive. La versione 5 supporta anche l'eliminazione della colonna zero, ma solo dopo l'uso di [**CCM \_ Subversion**](ccm-setversion.md) per impostare la versione su 5 o versioni successive. Nelle versioni precedenti alla 5, se è necessario eliminare la colonna zero, inserire una colonna fittizia di lunghezza zero di zero ed eliminare la colonna uno e versioni successive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





