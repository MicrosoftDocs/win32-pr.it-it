---
title: Messaggio TTM_GETTEXT (COMmctrl. h)
description: Recupera le informazioni gestite da un controllo ToolTip su uno strumento.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Controlli di Windows Message TTM_GETTEXT
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
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301653"
---
# <a name="ttm_gettext-message"></a>TTM \_ messaggio GETtext

Recupera le informazioni gestite da un controllo ToolTip su uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Il numero di **TCHARs**, incluso il **null** di terminazione, da copiare nel buffer a cui punta **lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Impostare il membro **cbSize** della struttura su `sizeof(TOOLINFO)` prima di inviare questo messaggio. Impostare i membri **HWND** e **UID** per identificare lo strumento per il quale recuperare le informazioni. Allocare un buffer di dimensioni specificato da *wParam*. Impostare il membro **lpszText** in modo che punti al buffer per ricevere il testo dello strumento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) e **TTM \_ gettexta** (ANSI)<br/>                   |



 

 





