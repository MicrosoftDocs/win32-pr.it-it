---
title: LVM_SETIMAGELIST messaggio (Commctrl.h)
description: Assegna un elenco di immagini a un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView SetImageList.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151f7d6e3736e6fe28faa28bc258fb4f85bfb57622b1ec77c02ed83ea187941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919961"
---
# <a name="lvm_setimagelist-message"></a>Messaggio LVM \_ SETIMAGELIST

Assegna un elenco di immagini a un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ NORMAL**</dt> </dl>                | Elenco di immagini con icone grandi.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | Elenco di immagini con icone piccole.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**STATO \_ LVSIL**</dt> </dl>                   | Elenco di immagini con immagini di stato.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Elenco di immagini per l'intestazione del gruppo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle all'elenco di immagini da assegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini associato in precedenza al controllo in caso di esito positivo oppure NULL in caso **contrario.**

## <a name="remarks"></a>Commenti

L'elenco di immagini corrente verrà eliminato automaticamente quando il controllo di visualizzazione elenco viene eliminato a meno che non sia impostato lo stile [**LVS \_ SHAREIMAGELISTS.**](list-view-window-styles.md) Se si usa questo messaggio per sostituire un elenco di immagini con un altro, l'applicazione deve eliminare in modo esplicito tutti gli elenchi di immagini diversi da quello corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





