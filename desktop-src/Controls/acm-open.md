---
title: Messaggio ACM_OPEN (COMmctrl. h)
description: Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro OpenEx, animate Open o animate \_ . Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Controlli di Windows Message ACM_OPEN
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
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400360"
---
# <a name="acm_open-message"></a>\_Messaggio aperto ACM

Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione. È possibile inviare questo messaggio in modo esplicito o usare la macro OpenEx, [**animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**\_ animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[Versione 4,71](common-control-versions.md) e successive. Handle di istanza per il modulo da cui deve essere caricata la risorsa. Impostare questo valore su **null** per fare in modo che il controllo usi il valore HINSTANCE usato per creare la finestra. Si noti che se la finestra viene creata da una DLL, il valore predefinito per *wParam* è il valore HINSTANCE della dll, non dell'applicazione che chiama la dll.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che contiene il percorso del file AVI o il nome di una risorsa AVI. In alternativa, questo parametro può essere costituito dall'identificatore di risorsa AVI in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e da zero in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Per creare questo valore, usare la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . Il controllo carica la risorsa AVI dal modulo specificato dall'handle di istanza passato alla funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , alla macro [**\_ create animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) o alla funzione di creazione della finestra di dialogo che ha creato il controllo. Nella [versione 4,71](common-control-versions.md) e successive la risorsa viene caricata dal modulo specificato da *wParam*. Una risorsa AVI deve avere il tipo "AVI". Se questo parametro è **null**, il sistema chiude il file AVI che è stato precedentemente aperto per il controllo di animazione specificato, se presente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il file o la risorsa AVI specificata da *lpszName* non deve contenere audio.

Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.

È possibile aprire solo clip AVI invisibile all'utente. \_L'apertura e l' [**animazione \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) di ACM Open hanno esito negativo se *lParam* specifica una clip AVI contenente un suono.

È possibile usare l' [**animazione \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) per chiudere un file AVI o una risorsa AVI precedentemente aperta per il controllo di animazione specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **ACM \_ OPENW** (Unicode) e **ACM \_ Opena** (ANSI)<br/>                         |



 

