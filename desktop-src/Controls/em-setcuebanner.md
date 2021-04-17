---
title: Messaggio EM_SETCUEBANNER (COMmctrl. h)
description: Imposta la cue testuale, o tip, visualizzata dal controllo di modifica per richiedere informazioni all'utente.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controlli di Windows Message EM_SETCUEBANNER
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478575"
---
# <a name="em_setcuebanner-message"></a>\_Messaggio SETCUEBANNER em

Imposta la cue testuale, o tip, visualizzata dal controllo di modifica per richiedere informazioni all'utente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**True** se il banner cue dovrebbe essere visualizzato anche quando il controllo di modifica ha lo stato attivo; in caso contrario, **false**. **False** è il comportamento predefinito. il banner di cue scompare quando l'utente fa clic nel controllo.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il testo da visualizzare come cue testuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **true**. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Un controllo di modifica usato per iniziare una ricerca può visualizzare "immettere la ricerca qui" in testo grigio come cue testuale. Quando l'utente fa clic sul testo, il testo viene allontanato e l'utente può digitare.

Non è possibile impostare un banner cue su un controllo di modifica su più righe o su un controllo Rich Edit.

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modifica \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





