---
title: Messaggio HDM_LAYOUT (COMmctrl. h)
description: Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre. È possibile inviare questo messaggio in modo esplicito o usare la macro del layout dell'intestazione \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Controlli di Windows Message HDM_LAYOUT
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
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048394"
---
# <a name="hdm_layout-message"></a>\_Messaggio layout HDM

Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre. È possibile inviare questo messaggio in modo esplicito o usare la macro del [**\_ layout dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) . Il membro **PRC** specifica le coordinate di un rettangolo e il membro **pwpos** riceve le dimensioni e la posizione del controllo intestazione all'interno del rettangolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il membro **pwpos** della struttura *lParam* riceve i valori di dimensioni e posizioni appropriati per posizionare il controllo lungo la parte superiore del rettangolo specificato. Il valore altezza è la somma delle altezze dei bordi orizzontali del controllo e l'altezza media dei caratteri nel tipo di carattere attualmente selezionato nel contesto di dispositivo del controllo.

Per usare **il \_ layout HDM** per impostare le dimensioni iniziali e la posizione di un controllo intestazione, impostare lo stato di visibilità iniziale del controllo in modo che sia nascosto. Dopo aver inviato il **\_ layout HDM** per recuperare i valori di dimensioni e posizione, usare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare la nuova dimensione, la posizione e lo stato di visibilità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

