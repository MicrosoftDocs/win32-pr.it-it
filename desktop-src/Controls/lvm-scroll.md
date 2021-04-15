---
title: Messaggio LVM_SCROLL (COMmctrl. h)
description: Scorre il contenuto di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di scorrimento ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Controlli di Windows Message LVM_SCROLL
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477560"
---
# <a name="lvm_scroll-message"></a>\_Messaggio di scorrimento LVM

Scorre il contenuto di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ scorrimento ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica la quantità di scorrimento orizzontale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco. Se il controllo visualizzazione elenco è in visualizzazione elenco, questo valore viene arrotondato per eccesso al numero di pixel più vicino che formano una colonna intera.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che specifica la quantità di scorrimento verticale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Quando il controllo elenco-visualizzazione è in visualizzazione report, è possibile scorrere il controllo verticalmente solo in incrementi di riga interi. Pertanto, il parametro *lParam* verrà arrotondato al numero di pixel più vicino che formano un incremento di riga intero. Se, ad esempio, l'altezza di una linea è 16 pixel e 8 viene passato per *lParam*, l'elenco verrà spostato di 16 pixel (1 riga). Se viene passato 7 per *lParam*, l'elenco verrà spostato di 0 pixel (0 righe).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





