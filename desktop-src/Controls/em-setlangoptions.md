---
title: EM_SETLANGOPTIONS messaggio (Richedit.h)
description: Imposta le opzioni per input method editor (IME) e supporto della lingua asiatica in un controllo Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5984c20273d2daa0a2e39fc6caf6dde88c8b274502a50e1a5e5eb3cca2b6f94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831202"
---
# <a name="em_setlangoptions-message"></a>Messaggio EM \_ SETLANGOPTIONS

Imposta le opzioni per input method editor (IME) e supporto della lingua asiatica in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica le opzioni della lingua. Per un elenco dei valori possibili, vedere [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il valore 1.

## <a name="remarks"></a>Commenti

Il **messaggio EM \_ SETLANGOPTIONS** controlla quanto segue:

-   Associazione automatica dei tipi di carattere.
-   Cambio automatico della tastiera.
-   Regolazione automatica delle dimensioni del carattere.
-   Uso dei tipi di carattere predefiniti dell'interfaccia utente anziché dei tipi di carattere predefiniti del documento.
-   Notifiche al client durante la composizione IME.
-   Modalità di interruzione della modalità di composizione da parte dell'IME.
-   Controllo ortografico, correzione automatica e previsione della tastiera virtuale.

Questo messaggio imposta i valori di tutti i flag di opzione del linguaggio. Per modificare un subset dei flag, inviare il messaggio [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) per ottenere i flag di opzione correnti, modificare i flag che è necessario modificare e quindi inviare il messaggio **EM \_ SETLANGOPTIONS** con il risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





