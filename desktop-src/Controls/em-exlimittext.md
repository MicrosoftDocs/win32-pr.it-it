---
title: Messaggio di EM_EXLIMITTEXT (RichEdit. h)
description: Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Controlli di Windows Message EM_EXLIMITTEXT
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477597"
---
# <a name="em_exlimittext-message"></a>\_Messaggio EXLIMITTEXT em

Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la quantità massima di testo che è possibile immettere. Se questo parametro è zero, viene usato il valore massimo predefinito, ovvero i caratteri 64K. Un oggetto COM viene conteggiato come un singolo carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il limite di testo impostato dal **messaggio \_ EXLIMITTEXT em** non limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio [**\_ flusso em**](em-streamin.md) con *lParam* impostato sul \_ testo SF. Tuttavia, limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio **\_ flusso em** nel messaggio con *lParam* impostato sul formato SF \_ RTF.

Prima di chiamare **em \_ EXLIMITTEXT** , il limite predefinito per la quantità di testo che un utente può immettere è 32.767 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**flusso EMin \_**](em-streamin.md)
</dt> </dl>

 

 





