---
title: Messaggio EM_GETCUEBANNER (COMmctrl. h)
description: Ottiene il testo visualizzato come cue testuale, o suggerimento, in un controllo di modifica.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Controlli di Windows Message EM_GETCUEBANNER
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964899"
---
# <a name="em_getcuebanner-message"></a>\_Messaggio GETCUEBANNER em

Ottiene il testo visualizzato come cue testuale, o suggerimento, in un controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Puntatore a un buffer Unicode che riceve il testo impostato come cue testuale. Il chiamante è responsabile dell'allocazione del buffer.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Dimensione del buffer a cui punta *wParam* in **WCHAR**, inclusa la terminazione **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modifica \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





