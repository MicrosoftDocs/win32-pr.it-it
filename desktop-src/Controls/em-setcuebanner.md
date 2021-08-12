---
title: EM_SETCUEBANNER messaggio (Commctrl.h)
description: Imposta il suggerimento testuale visualizzato dal controllo di modifica per richiedere informazioni all'utente.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER controlli Windows messaggio
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
ms.openlocfilehash: b08694d7368a994c639f236f18537e13d81f57083521599c23671941c74889bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673104"
---
# <a name="em_setcuebanner-message"></a>Messaggio \_ EM SETCUEBANNER

Imposta il suggerimento testuale visualizzato dal controllo di modifica per richiedere informazioni all'utente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

**TRUE** se il banner del segnale deve essere visualizzato anche quando il controllo di modifica ha lo stato attivo; in caso contrario, **FALSE.** **FALSE** è il comportamento predefinito che il banner del segnale scompare quando l'utente fa clic nel controllo.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il testo da visualizzare come segnale testuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **TRUE.** In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Un controllo di modifica usato per iniziare una ricerca può visualizzare "Immettere la ricerca qui" in testo grigio come segnale testuale. Quando l'utente fa clic sul testo, il testo non viene più visualizzato e l'utente può digitare.

Non è possibile impostare un banner cue in un controllo di modifica su più righe o in un controllo Rich Edit.

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modifica \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





