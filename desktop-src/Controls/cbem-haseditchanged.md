---
title: CBEM_HASEDITCHANGED messaggio (Commctrl.h)
description: Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5949827dbabf962ec9a9e9bd9d3b6d27d09a3b7e62f7fc71f2c4343e8ce370
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528041"
---
# <a name="cbem_haseditchanged-message"></a>Messaggio CBEM \_ HASEDITCHANGED

Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il testo nella casella di modifica del controllo è stato modificato oppure FALSE in **caso contrario.**

## <a name="remarks"></a>Commenti

Un controllo ComboBoxEx usa un controllo casella di modifica quando è impostato sullo [**stile CBS \_ DROPDOWN.**](combo-box-styles.md) È possibile recuperare l'handle della finestra del controllo casella di modifica inviando un [**messaggio \_ GETEDITCONTROL CBEM.**](cbem-geteditcontrol.md)

Quando l'utente inizia la modifica, si riceverà una notifica [CBEN \_ BEGINEDIT.](cben-beginedit.md) Al termine della modifica o quando lo stato attivo cambia, si riceverà una notifica [CBEN \_ ENDEDIT.](cben-endedit.md) Il **messaggio CBEM \_ HASEDITCHANGED** è utile solo per determinare se il testo è stato modificato se viene inviato prima della notifica \_ ENDEDIT CBEN. Se il messaggio viene inviato successivamente, restituirà **FALSE.** Si supponga, ad esempio, che l'utente inizi a modificare il testo nella casella di modifica ma cambi lo stato attivo, generando una notifica \_ ENDEDIT CBEN. Se si invia quindi un **messaggio CBEM \_ HASEDITCHANGED,** verrà restituito **FALSE,** anche se il testo è stato modificato.

Lo [**stile \_ SIMPLE di CBS**](combo-box-styles.md) non funziona correttamente con **CBEM \_ HASEDITCHANGED.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





