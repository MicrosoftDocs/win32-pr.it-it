---
title: Messaggio LVM_INSERTMARKHITTEST (COMmctrl. h)
description: Recupera il punto di inserimento più vicino a un punto specificato.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Controlli di Windows Message LVM_INSERTMARKHITTEST
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
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120970"
---
# <a name="lvm_insertmarkhittest-message"></a>\_Messaggio INSERTMARKHITTEST LVM

Recupera il punto di inserimento più vicino a un punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Puntatore a una struttura di **punti** che contiene le coordinate dell'hit test.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che specifica il punto di inserimento più vicino alle coordinate definite dal parametro *wParam* .</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario. Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.

## <a name="remarks"></a>Commenti

Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccole o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.

Se i punti di inserimento non sono validi per la vista, la struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene un valore-1 nel membro **iItem** .

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





