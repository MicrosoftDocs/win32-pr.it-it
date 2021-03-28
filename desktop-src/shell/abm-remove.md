---
description: Annulla la registrazione di un AppBar rimuovendo l'oggetto dall'elenco interno del sistema. Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar.
title: Messaggio ABM_REMOVE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878782"
---
# <a name="abm_remove-message"></a>\_Rimuovi messaggio da ABM

Annulla la registrazione di un AppBar rimuovendo l'oggetto dall'elenco interno del sistema. Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) contenente l'handle per il AppBar di cui annullare la registrazione. Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **HWND** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Questo messaggio consente al sistema di inviare il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) a tutti i AppBar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




