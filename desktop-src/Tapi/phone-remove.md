---
description: Il messaggio di rimozione del telefono TAPI \_ viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo telefonico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Messaggio di PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328047"
---
# <a name="phone_remove-message"></a>Messaggio di rimozione del telefono \_

Il messaggio **di \_ rimozione del telefono** TAPI viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo telefonico. In genere, questo non viene usato per le rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non viene più segnalato dal provider di servizi se TAPI è stato reinizializzato.


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

Per le applicazioni TAPI 2,0 o versioni successive viene inviato un messaggio di **\_ rimozione telefono** . In questo modo si informa che il dispositivo è stato rimosso dal sistema. Il messaggio di **\_ rimozione del telefono** è preceduto da un messaggio di [**\_ chiusura**](phone-close.md) del telefono su ogni handle telefonico, se l'applicazione ha aperto il telefono. Questo messaggio viene inviato a tutte le applicazioni che supportano la versione 2,0 o successiva di TAPI che hanno chiamato [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), inclusi quelli che non hanno dispositivi telefonici aperti al momento.

Alle applicazioni meno recenti (che hanno negoziato la versione 1,4 o precedente) viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) che specifica PHONESTATE \_ rimosso, seguito da un messaggio di [**\_ chiusura del telefono**](phone-close.md) . Diversamente dal messaggio **di \_ rimozione del telefono** , tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se hanno il telefono aperto al momento della rimozione. Se il telefono non è aperto, l'unica indicazione che indica che il dispositivo è stato rimosso è la ricezione di un PHONEERR \_ NODEVICE quando tentano di accedere al dispositivo.

Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo mediante il relativo identificatore del dispositivo restituisce un \_ errore PHONEERR nodevice. Dopo che tutte le applicazioni TAPI sono state arrestate in modo che TAPI possa essere riavviato e quando viene reinizializzata la funzione TAPI, il dispositivo rimosso non occupa più un identificatore del dispositivo.

> [!Note]  
> Implementazione: è TAPI che restituisce questo messaggio PHONEERR \_ NODEVICE dopo la ricezione di un \_ messaggio di rimozione del telefono da un provider di servizi. non vengono effettuate ulteriori chiamate a tale provider di servizi tramite tale identificatore del dispositivo telefonico.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura telefono**](phone-close.md)
</dt> <dt>

[**\_stato telefono**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




