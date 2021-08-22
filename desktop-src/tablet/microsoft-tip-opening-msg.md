---
description: Notifica la finestra all'apertura del Pannello input di testo.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: MICROSOFT_TIP_OPENING_MSG messaggio (Peninputpanel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e183cc426cd5d73e52c6aaef007bc5579ceb3eb0f4ceaf3f9f4084677b7a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335901"
---
# <a name="microsoft_tip_opening_msg-message"></a>MESSAGGIO \_ MICROSOFT TIP OPENING \_ \_ MSG

Notifica la finestra all'apertura del Pannello input di testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Attualmente non usato, deve essere **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Attualmente non usato, deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le applicazioni devono [**chiamare DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dopo la gestione di questo messaggio. Per informazioni sui valori restituiti, vedere **DefWindowProc.**

## <a name="remarks"></a>Commenti

Questa notifica indica quando si apre il pannello di input. Se si vuole eseguire un'azione in questo caso, gestire il messaggio, eseguire l'operazione nel gestore e quindi passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Questo messaggio viene inviato anche quando il Pannello input di testo è già visibile e l'utente passa dalla tastiera all'interfaccia della grafia.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista<br/>                                                                   |
| Intestazione<br/> | <dl> <dt>Peninputpanel.h</dt> </dl> |



 

