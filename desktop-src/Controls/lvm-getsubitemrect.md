---
title: LVM_GETSUBITEMRECT messaggio (Commctrl.h)
description: Recupera informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651be72c23113940fc30adb2e7a9de581289a8f4ddf580f27d01e2edf337c053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293891"
---
# <a name="lvm_getsubitemrect-message"></a>Messaggio LVM \_ GETSUBITEMRECT

Recupera informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (scelta consigliata). Questo messaggio deve essere usato solo con i controlli visualizzazione elenco che usano lo stile [**\_ LVS REPORT.**](list-view-window-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento padre dell'elemento secondario.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul rettangolo di delimitazione dell'elemento secondario. I membri devono essere inizializzati in base alle relazioni membro/valore seguenti:



| Valore                                                                                                                             | Significato                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**In alto**</dt> </dl>    | Indice in base uno dell'elemento secondario.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Sinistra**</dt> </dl> | Valore del flag (vedere le osservazioni). Indica la parte dell'elemento secondario della visualizzazione elenco per cui recuperare il rettangolo di delimitazione.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori del flag che possono essere impostati.



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valore flag** | **Significato**                                                                                                         |
| LIMITI \_ LVIR   | Restituisce il rettangolo di delimitazione dell'intero elemento, incluse l'icona e l'etichetta.                                    |
| ICONA \_ LVIR     | Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola.                                                           |
| ETICHETTA \_ LVIR    | Restituisce il rettangolo di delimitazione dell'intero elemento, incluse l'icona e l'etichetta. È identico a LVIR \_ BOUNDS. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

