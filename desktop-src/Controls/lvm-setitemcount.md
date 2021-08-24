---
title: LVM_SETITEMCOUNT messaggio (Commctrl.h)
description: Fa in modo che il controllo visualizzazione elenco alloca memoria per il numero specificato di elementi o imposta il numero virtuale di elementi in un controllo di visualizzazione elenco virtuale.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6b35b38c65663d9811a27341cf10d668a9e045641a8ff0871f6b49fe8bcdbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656281"
---
# <a name="lvm_setitemcount-message"></a>Messaggio LVM \_ SETITEMCOUNT

Fa in modo che il controllo visualizzazione elenco alloca memoria per il numero specificato di elementi o imposta il numero virtuale di elementi in un [controllo di visualizzazione elenco virtuale.](list-view-controls-overview.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi che il controllo di visualizzazione elenco conterrà.

</dd> <dt>

*lParam* 
</dt> <dd>

[Versione 4.70.](common-control-versions.md) Valori che specificano il comportamento del controllo visualizzazione elenco dopo la reimpostazione del conteggio degli elementi. Questo valore può essere una combinazione degli elementi seguenti:



| Valore                                                                                                                                                                                    | Significato                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | Il controllo visualizzazione elenco non verrà ridisegnato a meno che gli elementi interessati non siano attualmente visualizzati.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOSCROLL**</dt> </dl>                      | Il controllo visualizzazione elenco non modifica la posizione di scorrimento quando cambia il conteggio degli elementi.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

La modalità di allocazione della memoria dipende dalla modalità di creazione del controllo visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare le macro [**\_ ListView SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**\_ ListView SetItemCountEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) Per altre informazioni, vedere [Stile List-View virtuale.](/windows/desktop/Controls/list-view-controls-overview)

Se il controllo visualizzazione elenco è stato creato senza lo stile [**LVS \_ OWNERDATA,**](list-view-window-styles.md) l'invio di questo messaggio fa sì che il controllo alloca le strutture di dati interne per il numero specificato di elementi. In questo modo il controllo non deve allocare le strutture di dati ogni volta che viene aggiunto un elemento.

Se il controllo visualizzazione elenco è stato creato con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) (visualizzazione elenco virtuale), l'invio di questo messaggio imposta il numero virtuale di elementi contenuti nel controllo.

Il *parametro lParam* è destinato solo ai controlli di visualizzazione elenco che usano gli stili [**LVS \_ OWNERDATA**](list-view-window-styles.md) e [**LVS \_ REPORT**](list-view-window-styles.md) [**o LVS \_ LIST.**](list-view-window-styles.md)

Quando la visualizzazione elenco dei controlli comuni è una visualizzazione elenco virtualizzata [**(LVS \_ OWNERDATA),**](list-view-window-styles.md)è previsto un limite di 100.000.000 di elementi nella visualizzazione elenco. In questo scenario **LVM \_ SETITEMCOUNT** restituirà FALSE quando ha *wParam* di 100.000.001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

