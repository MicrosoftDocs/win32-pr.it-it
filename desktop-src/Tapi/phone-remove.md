---
description: Il messaggio TAPI PHONE REMOVE viene inviato per informare un'applicazione della rimozione (eliminazione dal \_ sistema) di un dispositivo telefonico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: PHONE_REMOVE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26be60c55b16d0126d0b3be107a95af17dd490c9329343bb27ac6496403d46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773901"
---
# <a name="phone_remove-message"></a>MESSAGGIO DI \_ RIMOZIONE TELEFONO

Il messaggio TAPI **PHONE \_ REMOVE** viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo telefonico. In genere, non viene usato per rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non verrebbe più segnalato dal provider di servizi se TAPI fosse stato reinizializzato.


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

Identificatore del dispositivo telefonico che è stato rimosso.

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

Alle applicazioni TAPI versione 2.0 o successiva viene inviato un **messaggio PHONE \_ REMOVE.** Questo informa che il dispositivo è stato rimosso dal sistema. Il **messaggio PHONE \_ REMOVE** è preceduto da un messaggio [**PHONE \_ CLOSE**](phone-close.md) su ogni handle di telefono, se l'applicazione aveva il telefono aperto. Questo messaggio viene inviato a tutte le applicazioni che supportano TAPI versione 2.0 o successiva che hanno chiamato [**phoneInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)incluse quelle che non hanno dispositivi telefonici aperti al momento.

Alle applicazioni meno recenti (che negoziava TAPI versione 1.4 o precedenti) viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) che specifica PHONESTATE REMOVED, seguito da un messaggio \_ PHONE [**\_ CLOSE.**](phone-close.md) A differenza **del messaggio PHONE \_ REMOVE,** tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se il telefono è aperto quando viene rimosso. Se il telefono non è aperto, l'unica indicazione che il dispositivo è stato rimosso riceverà un MESSAGGIO PHONEERR NODEVICE quando tenta di \_ accedere al dispositivo.

Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo tramite il relativo identificatore di dispositivo comporta un errore PHONEERR \_ NODEVICE. Dopo l'arresto di tutte le applicazioni TAPI in modo che TAPI possa essere riavviato e quando TAPI viene reinizializzato, il dispositivo rimosso non occupa più un identificatore di dispositivo.

> [!Note]  
> Implementazione: è TAPI che restituisce questo messaggio NODEVICE PHONEERR dopo la ricezione di un messaggio PHONE REMOVE da un provider di servizi. Non vengono effettuate altre chiamate a tale provider di servizi usando tale identificatore del dispositivo \_ \_ telefonico.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHIUSURA \_ TELEFONO**](phone-close.md)
</dt> <dt>

[**STATO \_ DEL TELEFONO**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




