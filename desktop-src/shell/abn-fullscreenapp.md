---
description: Notifica a un AppBar quando un'applicazione a schermo intero è in fase di apertura o chiusura. Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal \_ nuovo messaggio ABM.
title: Messaggio ABN_FULLSCREENAPP (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128475"
---
# <a name="abn_fullscreenapp-message"></a>\_Messaggio FULLSCREENAPP di ABN

Notifica a un AppBar quando un'applicazione a schermo intero è in fase di apertura o chiusura. Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal [**\_ nuovo messaggio ABM**](abm-new.md) .


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fOpen* 
</dt> <dd>

Flag che specifica se un'applicazione a schermo intero è in apertura o in chiusura. Questo parametro è **true** se l'applicazione è in apertura o **false** se è in chiusura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando si apre un'applicazione a schermo intero, un AppBar deve essere rilasciato nella parte inferiore dell'ordine z. Quando viene chiuso, il AppBar deve ripristinare la posizione dell'ordine z.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




