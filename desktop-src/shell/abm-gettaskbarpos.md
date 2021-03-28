---
description: Recupera il rettangolo di delimitazione della barra delle applicazioni di Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Messaggio ABM_GETTASKBARPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525429"
---
# <a name="abm_gettaskbarpos-message"></a>\_Messaggio GETTASKBARPOS ABM

Recupera il rettangolo di delimitazione della barra delle applicazioni di Windows.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) il cui membro **RC** riceve il rettangolo di delimitazione, in coordinate dello schermo, della barra delle applicazioni. Quando si invia questo messaggio, è necessario specificare il **cbSize** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Si noti che questo vale solo per la barra delle applicazioni di sistema. Possono essere presenti anche altri oggetti, in particolare le barre degli strumenti forniti con software di terze parti. Di conseguenza, parte dell'area dello schermo non coperta dalla barra delle applicazioni di Windows potrebbe non essere visibile all'utente. Per recuperare l'area della schermata non coperta dalla barra delle applicazioni e da altre barre dell'app nell'area di lavoro disponibile per l'applicazione, usare la funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

