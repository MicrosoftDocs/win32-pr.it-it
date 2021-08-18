---
title: TB_ADDSTRING messaggio (Commctrl.h)
description: Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0556add41addb4a58d5734ab900af4a43c2018b533723145ed4f9c8272e3890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078375"
---
# <a name="tb_addstring-message"></a>TB \_ ADDSTRING message

Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle all'istanza del modulo con un file eseguibile che contiene la risorsa stringa. Se *lParam punta* invece a una matrice di caratteri con una o più stringhe, impostare questo parametro su **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore di risorsa per la risorsa stringa o puntatore a una matrice TCHAR. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della prima nuova stringa in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Se *wParam* è **NULL,** *lParam* punta a una matrice di caratteri con una o più stringhe con terminazione Null. L'ultima stringa nella matrice deve essere terminata con due caratteri Null.

Se *wParam è* l'HINSTANCE dell'applicazione o di un altro modulo contenente una risorsa stringa, *lParam* è l'identificatore di risorsa della stringa. Ogni elemento nella stringa deve iniziare con un carattere separatore arbitrario e la stringa deve terminare con due caratteri di questo tipo. Ad esempio, il testo per tre pulsanti potrebbe essere visualizzato nella tabella delle stringhe come "/New/Open/Save//". Il messaggio restituisce l'indice di "New" nel pool di stringhe della barra degli strumenti e gli altri elementi sono in posizioni consecutive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) e **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





