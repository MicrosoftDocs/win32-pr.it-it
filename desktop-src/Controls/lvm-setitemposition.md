---
title: Messaggio LVM_SETITEMPOSITION (COMmctrl. h)
description: Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola). È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemPosition di ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Controlli di Windows Message LVM_SETITEMPOSITION
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873894"
---
# <a name="lvm_setitemposition-message"></a>\_Messaggio SETITEMPOSITION LVM

Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola). È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemPosition di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la nuova posizione x dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la nuova posizione y dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ AutoArrange**](list-view-window-styles.md) , gli elementi nel controllo elenco-visualizzazione vengono disposti dopo l'impostazione della posizione dell'elemento.

In Windows Vista, l'invio di questo messaggio a un controllo di visualizzazione elenco con lo stile [**LVS \_ AutoArrange**](list-view-window-styles.md) non esegue alcuna operazione e il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

