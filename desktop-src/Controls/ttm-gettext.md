---
title: TTM_GETTEXT messaggio (Commctrl.h)
description: Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9efe79105c705eba3dd25c124cf17ff0e4773618608bc7ef86ebbf3d0d9f715e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967891"
---
# <a name="ttm_gettext-message"></a>Messaggio \_ GETTEXT TTM

Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Numero di **TCHAR,** incluso il valore **NULL** di terminazione, da copiare nel buffer a cui **punta lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Impostare il **membro cbSize** di questa struttura su prima `sizeof(TOOLINFO)` di inviare questo messaggio. Impostare i **membri hwnd** **e uId** per identificare lo strumento per cui recuperare le informazioni. Allocare un buffer delle dimensioni specificato da *wParam*. Impostare il **membro lpszText** in modo che punti al buffer per ricevere il testo dello strumento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) e **TTM \_ GETTEXTA** (ANSI)<br/>                   |



 

 





