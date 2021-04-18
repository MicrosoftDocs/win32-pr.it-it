---
description: Il messaggio di \_ chiusura telefono TAPI viene inviato quando un dispositivo telefonico aperto è stato chiuso forzatamente come parte del recupero delle risorse. L'handle del dispositivo non è più valido dopo l'invio del messaggio.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Messaggio di PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329209"
---
# <a name="phone_close-message"></a>\_Messaggio di chiusura telefono

Il messaggio **di \_ chiusura telefono** TAPI viene inviato quando un dispositivo telefonico aperto è stato chiuso forzatamente come parte del recupero delle risorse. L'handle del dispositivo non è più valido dopo l'invio del messaggio.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle per il dispositivo telefonico aperto che è stato chiuso. L'handle non è più valido dopo l'invio del messaggio.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback dell'applicazione fornita durante l'apertura del dispositivo telefonico.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **\_ chiusura del telefono** viene inviato a un'applicazione solo dopo la chiusura forzata di un telefono aperto. Questa operazione può essere eseguita per impedire a una singola applicazione di monopolizzare un dispositivo telefonico troppo a lungo. Se il telefono può essere riaperto immediatamente dopo una chiusura forzata è specifico del dispositivo.

Un dispositivo telefonico aperto può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione del telefono o del driver. Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (in contrapposizione al successivo riavvio del sistema) e tali modifiche influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo telefonico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




