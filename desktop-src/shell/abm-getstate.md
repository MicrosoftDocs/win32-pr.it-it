---
description: Recupera gli stati di rilevamento automatico e sempre in primo piano della barra Windows barra delle applicazioni.
title: ABM_GETSTATE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466388"
---
# <a name="abm_getstate-message"></a>Messaggio ABM \_ GETSTATE

Recupera gli stati di rilevamento automatico e sempre in primo piano della barra Windows barra delle applicazioni.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a [**una struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) È necessario specificare il **membro cbSize** quando si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se la barra delle applicazioni non è nello stato di visualizzazione automatica né sempre attiva. In caso contrario, il valore restituito è uno o entrambi gli elementi seguenti:




| Codice restituito | Descrizione | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | La barra delle applicazioni è nello stato always-on-top. <br /><blockquote>[!Note]<br />A Windows 7, ABS_ALWAYSONTOP non viene più restituito perché la barra delle applicazioni si trova sempre in tale stato. Il codice meno recente deve essere aggiornato in modo da ignorare l'assenza di questo valore senza presupporre che il valore restituito significherebbe che la barra delle applicazioni non si trova nello stato always-on-top.</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | La barra delle applicazioni è nello stato nascondi automaticamente.<br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




