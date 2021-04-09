---
title: Messaggio LVM_SETITEMCOUNT (COMmctrl. h)
description: Consente al controllo di visualizzazione elenco di allocare memoria per il numero specificato di elementi o di impostare il numero virtuale di elementi in un controllo di visualizzazione elenco virtuale.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Controlli di Windows Message LVM_SETITEMCOUNT
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
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119334"
---
# <a name="lvm_setitemcount-message"></a>\_Messaggio SETITEMCOUNT LVM

Consente al controllo di visualizzazione elenco di allocare memoria per il numero specificato di elementi o di impostare il numero virtuale di elementi in un [controllo di visualizzazione elenco virtuale](list-view-controls-overview.md).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi che il controllo di visualizzazione elenco conterrà infine.

</dd> <dt>

*lParam* 
</dt> <dd>

[Versione 4,70](common-control-versions.md). Valori che specificano il comportamento del controllo visualizzazione elenco dopo la reimpostazione del numero di elementi. Questo valore può essere una combinazione dei seguenti elementi:



| Valore                                                                                                                                                                                    | Significato                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**\_NOINVALIDATEALL LVSICF**</dt> </dl> | Il controllo di visualizzazione elenco non verrà ridisegnato a meno che gli elementi interessati non siano attualmente in visualizzazione.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOscroll**</dt> </dl>                      | Il controllo elenco-visualizzazione non modifica la posizione di scorrimento quando cambia il numero di elementi.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

La modalità di allocazione della memoria dipende dal modo in cui è stato creato il controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare le macro [**ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) . Per ulteriori informazioni, vedere [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).

Se il controllo elenco-visualizzazione è stato creato senza lo stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) , l'invio di questo messaggio fa in modo che il controllo allochi le strutture di dati interne per il numero specificato di elementi. In questo modo si impedisce al controllo di allocare le strutture di dati ogni volta che viene aggiunto un elemento.

Se il controllo elenco-visualizzazione è stato creato con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) (visualizzazione elenco virtuale), l'invio di questo messaggio consente di impostare il numero virtuale di elementi contenuti nel controllo.

Il parametro *lParam* è destinato solo ai controlli visualizzazione elenco che usano gli stili [**LVS \_ OWNERDATA**](list-view-window-styles.md) e [**LVS \_ report**](list-view-window-styles.md) o [**LVS \_ List**](list-view-window-styles.md) .

Quando la visualizzazione elenco di controllo comune è una visualizzazione elenco virtualizzata ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), è presente un limite di 100 milioni elementi nella visualizzazione elenco. In questo scenario **LVM \_ SETITEMCOUNT** restituirà false se il valore di *wParam* è 100.000.001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

