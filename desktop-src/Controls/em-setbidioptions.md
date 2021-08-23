---
title: EM_SETBIDIOPTIONS messaggio (Richedit.h)
description: Il messaggio EM \_ SETBIDIOPTIONS imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22d03e1738fc688d34f55a6823f7ae95c2dfc41724e827cd31a184ac7cbdfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545021"
---
# <a name="em_setbidioptions-message"></a>Messaggio EM \_ SETBIDIOPTIONS

Il **messaggio EM \_ SETBIDIOPTIONS** imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che indica come impostare lo stato delle opzioni bidirezionali nel controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il controllo Rich Edit deve essere in modalità testo normale oppure **EM \_ SETBIDIOPTIONS** non farà nulla.

Nei controlli di testo **normale, EM \_ SETBIDIOPTIONS** determina automaticamente la direzione del paragrafo e/o l'allineamento in base alle regole di contesto. Queste regole specificano che la direzione e/o l'allineamento derivano dal primo carattere sicuro nel controllo. Un carattere sicuro è un carattere da cui è possibile determinare la direzione del testo (vedere Unicode Standard versione 2.0). La direzione e/o l'allineamento del paragrafo vengono applicati al formato predefinito.

**EM \_ SETBIDIOPTIONS imposta** il formato di paragrafo predefinito su RTL (da destra a sinistra) solo se trova un carattere RTL,

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**OPZIONI DI OFFERTA**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)
</dt> </dl>

 

 





