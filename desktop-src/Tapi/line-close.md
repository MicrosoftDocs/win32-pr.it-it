---
description: Il messaggio TAPI LINE \_ CLOSE viene inviato quando il dispositivo linea specificato è stato chiuso forzatamente. L'handle del dispositivo di linea o gli handle di chiamata per le chiamate sulla riga non sono più validi dopo l'invio del messaggio.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68fec993987bfc3ca36099d90eed2beadde9a749f965a36ebb6c513c210f387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682401"
---
# <a name="line_close-message"></a>Messaggio LINE \_ CLOSE

Il messaggio TAPI **LINE \_ CLOSE** viene inviato quando il dispositivo linea specificato è stato chiuso forzatamente. L'handle del dispositivo di linea o gli handle di chiamata per le chiamate sulla riga non sono più validi dopo l'invio del messaggio.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il dispositivo linea chiuso. Questo handle non è più valido.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

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

Il **messaggio LINE \_ CLOSE** viene inviato a qualsiasi applicazione solo dopo che il provider di servizi TAPI ha chiuso forzatamente una riga aperta. La riapertura della riga immediatamente dopo una chiusura forzata è specifica del dispositivo.

La condizione che causa può essere una modifica significativa dello stato, un errore hardware, una perdita di connessione a un server o anche potenzialmente impedire a una singola applicazione di minacciare un dispositivo a linee per troppo tempo. Un dispositivo line può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione della riga o del relativo driver. Se l'utente vuole che le modifiche di configurazione siano effettive immediatamente (anziché dopo il successivo riavvio del sistema) e influisce sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo linea.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




