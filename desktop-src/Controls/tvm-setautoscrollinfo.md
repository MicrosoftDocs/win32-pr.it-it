---
title: Messaggio TVM_SETAUTOSCROLLINFO (COMmctrl. h)
description: Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetAutoScrollInfo di TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Controlli di Windows Message TVM_SETAUTOSCROLLINFO
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301394"
---
# <a name="tvm_setautoscrollinfo-message"></a>\_Messaggio SETAUTOSCROLLINFO TVM

Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetAutoScrollInfo di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Specifica i pixel al secondo. L'offset da scorrere è diviso per il *wParam* per determinare la durata totale dello scorrimento automatico.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Specifica l'intervallo di tempo di ridisegnato. Ricreare ogni intervallo di elasped fino a quando l'elemento non viene spostato nella visualizzazione. Dato *wParam*, viene calcolata la posizione dell'elemento e si verifica un ridisegno. Impostare questo valore per creare lo scorrimento uniforme.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

Le informazioni di scorrimento automatico vengono utilizzate per scorrere un elemento non visibile nella visualizzazione. Il controllo deve avere lo stile esteso [**\_ \_ AUTOHSCROLL TV ex**](tree-view-control-window-extended-styles.md) . Per informazioni sugli stili estesi, vedere Tree-View controllare gli stili estesi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





