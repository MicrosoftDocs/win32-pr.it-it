---
description: Notifica a una barra delle app quando un'applicazione a schermo intero si sta aprendo o chiudendo. Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal messaggio ABM \_ NEW.
title: ABN_FULLSCREENAPP messaggio (Shellapi.h)
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
ms.openlocfilehash: 55bba51153ff90dfa69b870468a1c5002121eaccf45559821c6031aba35d4b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090791"
---
# <a name="abn_fullscreenapp-message"></a>Messaggio ABN \_ FULLSCREENAPP

Notifica a una barra delle app quando un'applicazione a schermo intero si sta aprendo o chiudendo. Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal [**messaggio ABM \_ NEW.**](abm-new.md)


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Fopen* 
</dt> <dd>

Flag che specifica se un'applicazione a schermo intero si sta aprendo o chiudendo. Questo parametro è **TRUE se** l'applicazione si sta aprendo o **FALSE** se è in chiusura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando si apre un'applicazione a schermo intero, una barra delle app deve essere visualizzata nella parte inferiore dell'ordine Z. Quando viene chiusa, la barra dell'app dovrebbe ripristinare la posizione dell'ordine Z.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




