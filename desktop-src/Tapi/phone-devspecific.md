---
description: TAPI invia il \_ messaggio DEVSPECIFIC del telefono a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si verificano sul telefono. Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Messaggio di PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324128"
---
# <a name="phone_devspecific-message"></a>\_Messaggio DEVSPECIFIC telefono

TAPI invia il **messaggio \_ DEVSPECIFIC del telefono** a un'applicazione per notificare all'applicazione gli eventi specifici del dispositivo che si verificano sul telefono. Il significato del messaggio e l'interpretazione dei parametri sono definiti dall'implementazione.


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
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




