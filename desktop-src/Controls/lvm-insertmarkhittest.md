---
title: LVM_INSERTMARKHITTEST messaggio (Commctrl.h)
description: Recupera il punto di inserimento più vicino a un punto specificato.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250585fea10846e10238132c5150f5ace9f8e00c474e763023c36c8566fbc752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919981"
---
# <a name="lvm_insertmarkhittest-message"></a>Messaggio LVM \_ INSERTMARKHITTEST

Recupera il punto di inserimento più vicino a un punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Puntatore a una **struttura POINT** che contiene le coordinate dell'hit test.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">struttura LVINSERTMARK</a> che specifica il punto di inserimento più vicino alle coordinate definite dal *parametro wParam.*</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario. **Viene** restituito FALSE se le dimensioni nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non sono uguali alle dimensioni effettive della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.

## <a name="remarks"></a>Commenti

Un punto di inserimento può essere visualizzato solo se il controllo visualizzazione elenco si trova nella visualizzazione icona, nella visualizzazione icona piccola o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.

Se i punti di inserimento non si applicano alla vista, la struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene -1 nel **membro iItem.**

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





