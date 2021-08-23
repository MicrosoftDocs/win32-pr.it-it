---
description: Il messaggio TAPI LINE REMOVE viene inviato per informare un'applicazione della rimozione (eliminazione dal \_ sistema) di un dispositivo line.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: LINE_REMOVE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13f36123cb8cb77bd2d4b78c3e69a2da1c027aef4dad1fc9dfd7f3c6a00399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335921"
---
# <a name="line_remove-message"></a>LINE \_ REMOVE message

Il messaggio TAPI **LINE \_ REMOVE** viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo line. In genere, non viene usato per rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non verrebbe più segnalato dal provider di servizi se TAPI fosse stato reinizializzato.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore del dispositivo line rimosso.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Alle applicazioni che supportano TAPI versione 2.0 o successiva viene inviato un **messaggio LINE \_ REMOVE.** Questo informa che il dispositivo è stato rimosso dal sistema. Il **messaggio LINE \_ REMOVE** è preceduto da un messaggio [**LINE \_ CLOSE**](line-close.md) in ogni handle di riga, se l'applicazione ha la riga aperta. Questo messaggio viene inviato a tutte le applicazioni che supportano TAPI versione 2.0 o successiva che hanno chiamato [**lineInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)incluse quelle che non hanno dispositivi line aperti al momento.

Alle applicazioni meno recenti viene [**inviato un messaggio LINE \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE \_ REMOVED, seguito da un messaggio LINE \_ CLOSE. A differenza **del messaggio LINE \_ REMOVE,** tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se la riga è aperta quando viene rimossa. Se la linea non è aperta, l'unica indicazione che il dispositivo è stato rimosso riceverà un errore LINEERR NODEVICE quando tentano di \_ accedere al dispositivo.

Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo tramite il relativo identificatore di dispositivo comporta un errore \_ LINEERR NODEVICE. Dopo l'arresto di tutte le applicazioni TAPI in modo che TAPI possa essere riavviato e quando TAPI viene reinizializzato, il dispositivo rimosso non occupa più un identificatore di dispositivo.

> [!Note]  
> Implementazione: è TAPI che restituisce questo LINEERR NODEVICE; dopo la ricezione di un messaggio LINE REMOVE da un provider di servizi. Non vengono effettuate altre chiamate a tale provider di servizi usando tale identificatore di dispositivo \_ di linea. **\_**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHIUSURA \_ RIGA**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




