---
description: Notifica alla finestra l'apertura del pannello input di testo.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Messaggio di MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333224"
---
# <a name="microsoft_tip_opening_msg-message"></a>\_Messaggio di \_ apertura \_ messaggio Microsoft Tip

Notifica alla finestra l'apertura del pannello input di testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Attualmente non utilizzato, deve essere **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Attualmente non utilizzato, deve essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le applicazioni devono chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dopo aver gestito questo messaggio. Per informazioni sui valori restituiti, vedere **DefWindowProc** .

## <a name="remarks"></a>Commenti

Questa notifica consente di stabilire quando il pannello di input viene aperto. Se si desidera eseguire un'azione quando si verifica questo problema, gestire il messaggio, eseguire l'operazione nel gestore e quindi passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Questo messaggio viene inviato anche quando il pannello input di testo è già visibile e l'utente passa dalla tastiera all'interfaccia della grafia.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista<br/>                                                                   |
| Intestazione<br/> | <dl> <dt>PenInputPanel. h</dt> </dl> |



 

