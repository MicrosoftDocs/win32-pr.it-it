---
title: ACM_OPEN messaggio (Commctrl.h)
description: Apre un clip AVI e visualizza il primo fotogramma in un controllo di animazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Animate Open o Animate \_ OpenEx. È consigliabile usare la versione Unicode di questo messaggio, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5af2bd996af159217c92d78102a97e5c530d34cf445d5ad34186cecb93ab85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922171"
---
# <a name="acm_open-message"></a>Messaggio ACM \_ OPEN

Apre un clip AVI e visualizza il primo fotogramma in un controllo di animazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Animate Open o**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) Animate [**\_ OpenEx.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) È consigliabile usare la versione Unicode di questo messaggio, ACM \_ OPENW.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[Versione 4.71 e](common-control-versions.md) successive. Handle di istanza per il modulo da cui deve essere caricata la risorsa. Impostare questo valore su **NULL per** fare in modo che il controllo usi il valore HINSTANCE usato per creare la finestra. Si noti che se la finestra viene creata da una DLL, il valore predefinito per *wParam* è il valore HINSTANCE della DLL, non dell'applicazione che chiama la DLL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che contiene il percorso del file AVI o il nome di una risorsa AVI. In alternativa, questo parametro può essere costituito dall'identificatore di risorsa AVI in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e da zero in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Per creare questo valore, usare la macro [**MAKEINTRESOURCE.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) Il controllo carica la risorsa AVI dal modulo specificato dall'handle di istanza passato alla funzione [**CreateWindow,**](/windows/desktop/api/winuser/nf-winuser-createwindowa) alla macro [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) o alla funzione di creazione della finestra di dialogo che ha creato il controllo. Nella [versione 4.71](common-control-versions.md) e successive la risorsa viene caricata dal modulo specificato da *wParam*. Una risorsa AVI deve avere il tipo "AVI". Se questo parametro è **NULL,** il sistema chiude il file AVI aperto in precedenza per il controllo animazione specificato, se presente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il file AVI o la risorsa specificata da *lpszName* non deve contenere audio.

È consigliabile usare la versione Unicode di questo messaggio, ACM \_ OPENW.

È possibile aprire solo clip AVI invisibile all'utente. ACM \_ OPEN e Animate Open [**\_ hanno**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) esito negativo *se lParam* specifica un clip AVI che contiene audio.

È possibile usare [**Animate \_ Close per**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) chiudere un file AVI o una risorsa AVI precedentemente aperta per il controllo animazione specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **ACM \_ OPENW** (Unicode) e **ACM \_ OPENA** (ANSI)<br/>                         |



 

