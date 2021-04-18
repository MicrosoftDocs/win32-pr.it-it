---
title: Messaggio TTM_ENUMTOOLS (COMmctrl. h)
description: Recupera le informazioni che un controllo ToolTip gestisce sullo strumento corrente \ 8212, ovvero lo strumento per il quale la descrizione comando sta visualizzando il testo.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Controlli di Windows Message TTM_ENUMTOOLS
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476792"
---
# <a name="ttm_enumtools-message"></a>\_Messaggio TTM ENUMTOOLS

Recupera le informazioni che un controllo ToolTip gestisce sullo strumento corrente, ovvero lo strumento per il quale la descrizione comando sta attualmente visualizzando il testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dello strumento per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento. Impostare il membro **cbSize** della struttura su sizeof (TOOLINFO) prima di inviare questo messaggio. Allocare un buffer. Impostare il membro **lpszText** in modo che punti al buffer per ricevere il testo dello strumento. Non è possibile determinare le dimensioni del buffer richieste. Tuttavia, il testo dello strumento, come restituito al membro **lpszText** della struttura **TOOLINFO** , ha una lunghezza massima di 80 **TCHARs**, incluso il **null** di terminazione. Se il testo supera questa lunghezza, viene troncato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se vengono enumerati gli strumenti o **false** in caso contrario.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non consente al destinatario del messaggio di conoscerne le dimensioni o di specificare le dimensioni del buffer. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





