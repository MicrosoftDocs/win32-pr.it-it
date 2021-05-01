---
title: TTM_ENUMTOOLS messaggio (Commctrl.h)
description: Recupera le informazioni mantenute da un controllo descrizione comando sullo strumento corrente \ 8212, ovvero lo strumento per cui la descrizione comando visualizza attualmente il testo.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS di windows del messaggio
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
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327136"
---
# <a name="ttm_enumtools-message"></a>Messaggio TTM \_ ENUMTOOLS

Recupera le informazioni che un controllo descrizione comando gestisce sullo strumento corrente, ovvero lo strumento per cui la descrizione comando visualizza attualmente testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dello strumento per il quale recuperare informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento. Impostare il **membro cbSize** di questa struttura su sizeof(TOOLINFO) prima di inviare questo messaggio. Allocare un buffer. Impostare il **membro lpszText** in modo che punti al buffer per ricevere il testo dello strumento. Non è possibile determinare le dimensioni del buffer necessarie. Tuttavia, il testo dello strumento, come restituito nel membro **lpszText** della struttura **TOOLINFO,** ha una lunghezza massima di 80 **TCHAR,** inclusa la **terminazione NULL**. Se il testo supera questa lunghezza, viene troncato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE se** uno strumento è stato enumerato o meno.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non consente al destinatario del messaggio di conoscere le dimensioni del buffer o di specificare le dimensioni del buffer. Prima di continuare, [è consigliabile esaminare Considerazioni sulla sicurezza: Controlli di Microsoft Windows.](sec-comctls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





