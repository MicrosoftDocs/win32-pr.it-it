---
description: TAPI invia il messaggio PHONE DEVSPECIFIC a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si \_ verificano al telefono. Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072901"
---
# <a name="phone_devspecific-message"></a>PHONE \_ DEVSPECIFIC message

TAPI invia il **messaggio \_ PHONE DEVSPECIFIC** a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si verificano al telefono. Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle per il dispositivo telefonico.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback dell'applicazione fornita all'apertura del dispositivo telefonico.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifico del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




