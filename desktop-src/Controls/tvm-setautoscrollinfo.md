---
title: TVM_SETAUTOSCROLLINFO messaggio (Commctrl.h)
description: Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetAutoScrollInfo.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO di controllo Windows messaggio
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
ms.openlocfilehash: d8840045900fdbd63930219d199889cde018406779426cd767b49ab41a399efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060161"
---
# <a name="tvm_setautoscrollinfo-message"></a>Messaggio \_ TVM SETAUTOSCROLLINFO

Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetAutoScrollInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Specifica i pixel al secondo. L'offset per lo scorrimento è diviso per *wParam* per determinare la durata totale dello scorrimento automatico.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Specifica l'intervallo di tempo di ridisegno. Ridisegna a ogni intervallo di tempo, fino a quando non viene fatto scorrere l'elemento nella visualizzazione. Dato *wParam*, la posizione dell'elemento viene calcolata e viene eseguito un ridisegno. Impostare questo valore per creare uno scorrimento uniforme.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Le informazioni di scorrimento automatico vengono usate per scorrere un elemento non visibile nella visualizzazione. Il controllo deve avere lo [**stile esteso TVS \_ EX \_ AUTOHSCROLL.**](tree-view-control-window-extended-styles.md) Per informazioni sugli stili estesi, vedere Tree-View degli stili estesi del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





