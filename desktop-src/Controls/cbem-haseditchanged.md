---
title: Messaggio CBEM_HASEDITCHANGED (COMmctrl. h)
description: Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Controlli di Windows Message CBEM_HASEDITCHANGED
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
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964944"
---
# <a name="cbem_haseditchanged-message"></a>\_Messaggio CBEM HASEDITCHANGED

Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il testo nella casella di modifica del controllo è stato modificato; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Un controllo ComboBoxEx usa un controllo casella di modifica quando è impostato sullo stile [**a \_ discesa CBS**](combo-box-styles.md) . È possibile recuperare l'handle di finestra del controllo casella di modifica inviando un messaggio [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .

Quando l'utente inizia a modificare, si riceverà una notifica [CBEN \_ BEGINEDIT](cben-beginedit.md) . Al termine della modifica, o se lo stato attivo cambia, si riceverà una notifica [CBEN \_ ENDEDIT](cben-endedit.md) . Il **messaggio \_ HASEDITCHANGED CBEM** è utile solo per determinare se il testo è stato modificato se viene inviato prima della notifica di CBEN \_ ENDEDIT. Se il messaggio viene inviato in seguito, restituirà **false**. Si supponga, ad esempio, che l'utente inizi a modificare il testo nella casella di modifica, ma modifichi lo stato attivo, generando una \_ notifica CBEN ENDEDIT. Se quindi si invia un messaggio **CBEM \_ HASEDITCHANGED** , viene restituito **false**, anche se il testo è stato modificato.

Lo [**stile \_ semplice CBS**](combo-box-styles.md) non funziona correttamente con **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





