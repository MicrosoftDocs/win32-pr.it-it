---
description: Imposta gli stati Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.
title: Messaggio ABM_SETSTATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977442"
---
# <a name="abm_setstate-message"></a>\_Messaggio di SESTATO ABM

Imposta gli stati Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . È necessario specificare i membri **cbSize** e **HWND** quando si invia questo messaggio. I dati per lo stato desiderato vengono inviati nel membro **lParam** utilizzando uno dei valori seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Nascondi automaticamente e sempre in primo piano

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**


</dt> <dd>

Always-on-top on, Nascondi automaticamente

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_Nascondi automaticamente ABS**


</dt> <dd>

Nascondi automaticamente on, always on-top off

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ Nascondi automaticamente \| ABS \_ ALWAYSONTOP**


</dt> <dd>

Nascondi automaticamente e always on-top entrambi in

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




