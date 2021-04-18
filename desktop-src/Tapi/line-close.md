---
description: Il messaggio di chiusura della riga di TAPI \_ viene inviato quando il dispositivo a linee specificato è stato chiuso forzatamente. Quando il messaggio è stato inviato, l'handle di dispositivo linea o qualsiasi handle di chiamata per le chiamate sulla riga non sono più validi.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Messaggio di LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327497"
---
# <a name="line_close-message"></a>\_Messaggio di chiusura riga

Il messaggio **di \_ chiusura della riga** di TAPI viene inviato quando il dispositivo a linee specificato è stato chiuso forzatamente. Quando il messaggio è stato inviato, l'handle di dispositivo linea o qualsiasi handle di chiamata per le chiamate sulla riga non sono più validi.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il dispositivo della linea che è stato chiuso. Questo handle non è più valido.

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

Il messaggio di **\_ chiusura riga** viene inviato a qualsiasi applicazione solo dopo che il provider di servizi TAPI (TSP) ha chiuso forzatamente una linea aperta. Indica se la riga può essere riaperta immediatamente dopo una chiusura forzata è specifica del dispositivo.

La condizione che provoca la causa può essere una modifica significativa dello stato, un errore hardware, una perdita di connessione a un server o anche potenzialmente impedire a una singola applicazione di monopolizzare un dispositivo a linee troppo a lungo. Un dispositivo A linee può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione di tale riga o del relativo driver. Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (a differenza di dopo il successivo riavvio del sistema) e influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo della linea.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




