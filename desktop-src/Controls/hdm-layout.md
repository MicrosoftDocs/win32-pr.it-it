---
title: HDM_LAYOUT messaggio (Commctrl.h)
description: Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Layout intestazione.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435931"
---
# <a name="hdm_layout-message"></a>Messaggio LAYOUT HDM \_

Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Layout intestazione.**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura HDLAYOUT.**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) Il **membro prc** specifica le coordinate di un rettangolo e il membro **pwpos** riceve le dimensioni e la posizione del controllo intestazione all'interno del rettangolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il **membro pwpos** della struttura *lParam* riceve i valori di dimensione e posizione appropriati per il posizionamento del controllo lungo la parte superiore del rettangolo specificato. Il valore di altezza è la somma delle altezze dei bordi orizzontali del controllo e dell'altezza media dei caratteri nel tipo di carattere attualmente selezionato nel contesto di dispositivo del controllo.

Per usare **HDM \_ LAYOUT** per impostare le dimensioni iniziali e la posizione di un controllo intestazione, impostare lo stato di visibilità iniziale del controllo in modo che sia nascosto. Dopo aver **inviato HDM \_ LAYOUT** per recuperare i valori di dimensione e posizione, usare la [**funzione SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare le nuove dimensioni, posizione e stato di visibilità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

