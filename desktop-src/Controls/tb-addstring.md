---
title: Messaggio TB_ADDSTRING (COMmctrl. h)
description: Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Controlli di Windows Message TB_ADDSTRING
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
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302788"
---
# <a name="tb_addstring-message"></a>TB \_ ADDSTRING messaggio

Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per l'istanza del modulo con un file eseguibile che contiene la risorsa di stringa. Se *lParam* punta invece a una matrice di caratteri con una o più stringhe, impostare questo parametro su **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore di risorsa per la risorsa di stringa o puntatore a una matrice TCHAR. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della prima nuova stringa se ha esito positivo oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Se *wParam* è **null**, *lParam* punta a una matrice di caratteri con una o più stringhe con terminazione null. L'ultima stringa della matrice deve terminare con due caratteri null.

Se *wParam* è il hInstance dell'applicazione o di un altro modulo contenente una risorsa di stringa, *lParam* è l'identificatore di risorsa della stringa. Ogni elemento nella stringa deve iniziare con un carattere separatore arbitrario e la stringa deve terminare con due caratteri di questo tipo. Ad esempio, il testo per tre pulsanti potrebbe essere visualizzato nella tabella delle stringhe come "/New/Open/Save//". Il messaggio restituisce l'indice di "New" nel pool di stringhe della barra degli strumenti e gli altri elementi si trovano in posizioni consecutive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) e **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





